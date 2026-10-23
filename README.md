# .github

Org-wide defaults for every repo under Project-Arrakis:

- [`SECURITY.md`](SECURITY.md) — fallback vulnerability-reporting policy for any repo without its own.
- [`.github/workflows/reusable-security-scan.yml`](.github/workflows/reusable-security-scan.yml) — shared gitleaks + semgrep + trivy scan, callable via `workflow_call` so a fix here propagates everywhere instead of drifting per repo.
- [`.github/workflows/reusable-security-scan-v2.yml`](.github/workflows/reusable-security-scan-v2.yml) — hardened successor of the shared scan (default-branch gitleaks config, least-privilege token, hash-locked semgrep option); opt-in per repo, pinned by commit SHA. See [`security-scan/README.md`](security-scan/README.md).
- [`.github/workflow-templates/security-scan.yml`](.github/workflow-templates/security-scan.yml) — starter workflow (shows up under Actions → New workflow → Organization templates) that wires a repo up to the shared scan above.
- [`profile/README.md`](profile/README.md) — the public org profile page.