# Shared security scan, v2

`.github/workflows/reusable-security-scan-v2.yml` is the hardened successor of
`reusable-security-scan.yml`. The v1 file is unchanged and keeps working for every repo that calls
it (several do, some at `@main`); a repo opts in to v2 by changing one `uses:` line.

The interface is the same: inputs `run-gitleaks`, `run-semgrep`, `run-trivy`,
`gitleaks-config-path`, the optional secret `SEMGREP_APP_TOKEN`, and the jobs `gitleaks`,
`semgrep` and `trivy`. A calling job named `security-scan` therefore keeps the status check names
`security-scan / gitleaks`, `security-scan / semgrep` and `security-scan / trivy`.

## What v2 changes

| Area | v1 | v2 |
| --- | --- | --- |
| Token permissions | none declared (the caller's default) | `permissions: contents: read` at workflow level; no job asks for more |
| gitleaks configuration | `.gitleaks.toml` read from the checkout, i.e. from the pull request under test, which can weaken or delete it | read from the **default branch** of the calling repo (`origin/<default branch>`); never from the pull request |
| `.gitleaksignore` | read from the checkout (gitleaks always loads it) | replaced by the default branch's copy before the scan; none if the default branch has none |
| No config on the default branch | gitleaks auto-loads `.gitleaks.toml` from the checkout if present, else built-in rules | built-in rules, forced with an explicit stub config so the checkout's file is never picked up |
| `gitleaks-config-path` input | interpolated into the shell script | passed through an environment variable and validated: relative, no `..`, letters/digits/`._-/` only |
| semgrep rules | `p/default` and `p/secrets` fetched live from the registry | the committed snapshot in `security-scan/semgrep-rules/` when the caller passes `tools-ref` and that commit has it; otherwise the registry sets as before. Always `--metrics off` |
| semgrep install | `pip install semgrep==1.170.0`, no hashes | `pip install --require-hashes -r requirements-semgrep.txt` when the caller passes `tools-ref` and that commit has the file; otherwise the same pinned install |
| Python | whatever the runner image ships | 3.12 via `actions/setup-python` (pinned by SHA) |
| Checkout | token kept in `.git/config` | `persist-credentials: false` |
| trivy and gitleaks installs | checksum-verified downloads | unchanged |

Every `uses:` is pinned by full commit SHA.

### Consequences of reading gitleaks configuration from the default branch

* A pull request that changes `.gitleaks.toml` or `.gitleaksignore` is scanned with the **old**
  version. If a legitimate change is needed to make the scan pass (a new allow-listed path, a new
  fingerprint), merge it first in its own change; a maintainer can merge that one deliberately.
  The scan prints a notice when the checkout's config differs from the default branch's.
* The first pull request that adds a config to a repo that has none is scanned with the built-in rules.
* Inline `gitleaks:allow` comments, `.semgrepignore` and `# nosemgrep` comments, and trivy's
  `.trivyignore` / `trivy.yaml` still come from the code under test. They show up in the diff of the
  pull request, which is where review happens.

## Semgrep snapshot and hash lock (opt-in by `tools-ref`)

`tools-ref` is an optional input that takes a **full 40-hex commit SHA** of this repository (anything
else is rejected). The semgrep job downloads `security-scan/requirements-semgrep.txt` and
`security-scan/semgrep-rules/p-default.yml` + `p-secrets.yml` from that exact commit. Because the
commit is immutable, nothing the scan depends on can change underneath a pinned caller.

* No `tools-ref`, or a commit without those files: the previous behaviour (pinned pip install, registry
  rule sets), now with `--metrics off`.
* An incomplete snapshot (only one of the two rule files) fails the job.

The files are created by two maintainer-run workflows (`workflow_dispatch`, run on `main`). They
download in CI, never on a developer machine, and propose their result by pull request:

* **Update semgrep rule snapshot** (`.github/workflows/update-semgrep-rules.yml`) downloads the two
  registry sets, validates them with `semgrep --validate`, and proposes `security-scan/semgrep-rules/`
  with a dated `SNAPSHOT.txt` (date, semgrep version, sha256 of each file).
* **Propose semgrep hash lock** (`.github/workflows/propose-semgrep-hash-lock.yml`) resolves
  `security-scan/requirements-semgrep.in` with `pip-compile --generate-hashes`, proves that
  `pip install --require-hashes` works from the result, and proposes
  `security-scan/requirements-semgrep.txt`. Optional input: `semgrep-version`.

If the repository setting "Allow GitHub Actions to create and approve pull requests" is off, the jobs
push their branch and print the compare link in the job summary; open the pull request from there.

Licence note: the registry rules are published under the Semgrep Rules License. Check that committing
a copy to this public repository is permitted for you before the first run of the snapshot workflow.

Refresh the snapshot periodically (run the workflow, review, merge), then bump the callers.

## Migrating a repo

1. Allow the v2 path in the repo's Actions policy if it is set to "selected actions": add
   `Project-Arrakis/.github/.github/workflows/reusable-security-scan-v2.yml@*` to the allowed patterns
   (the v1 pattern does not match the v2 file name). If the repo requires SHA pinning, keep the pin.
2. In the repo's workflow, change the `uses:` of the job to the v2 file, pinned by the SHA of the commit
   that added or last changed it. Keep the job name `security-scan`, the `permissions:` block and the
   explicit `secrets:` mapping. Do not use `secrets: inherit`.

   ```yaml
   security-scan:
     name: security-scan
     uses: Project-Arrakis/.github/.github/workflows/reusable-security-scan-v2.yml@<40-hex-sha>
     permissions:
       contents: read
     secrets:
       SEMGREP_APP_TOKEN: ${{ secrets.SEMGREP_APP_TOKEN }}
   ```
3. Once the snapshot and the hash lock are merged here, bump the `uses:` SHA to a commit that
   contains them and add `with: tools-ref: <the same SHA>`.
4. Check on the pull request that `security-scan / gitleaks`, `security-scan / semgrep` and
   `security-scan / trivy` ran and passed.
5. Keep the gitleaks config (if any) on the default branch, and change it in its own change.
