# Setting up an Anthropic credential for CI

The [`reusable-docs-review.yml`](../.github/workflows/reusable-docs-review.yml) shared workflow (the "tech writer" documentation review, run on PRs touching docs) needs one of two credentials to actually run. Without either, the job is skipped (not failed) — see that workflow's own `check-auth` job.

Set the secret at the **organization level** so every repo gets it without repeating this setup per repo.

## Option A — Anthropic API key (billed per use)

1. Go to [console.anthropic.com](https://console.anthropic.com) → **Settings → API Keys → Create Key**.
2. In GitHub: the `Project-Arrakis` org → **Settings → Secrets and variables → Actions → New organization secret**.
3. Name: `ANTHROPIC_API_KEY`. Value: the key from step 1.
4. Under **Repository access**, choose which repos can use it, or select "All repositories."

## Option B — Claude Code OAuth token (uses an existing Pro/Max plan's included usage instead of separate API billing)

1. Run `claude setup-token` (locally, or in a Claude Code session) — this opens a browser authorization flow and prints a token.
2. Same org-secret steps as Option A, but name it `CLAUDE_CODE_OAUTH_TOKEN`.

## Notes

- Only one of the two is needed. If both are set, `ANTHROPIC_API_KEY` is checked first by convention in the calling workflow, but either alone is sufficient.
- No workflow file changes are needed after adding the secret — `reusable-docs-review.yml` detects it automatically and starts running on the next PR.
- To scope cost/usage, use Option B (an existing Pro/Max plan's included usage) rather than Option A if you're already paying for a Claude Code plan.
- See [`reusable-docs-review.yml`](../.github/workflows/reusable-docs-review.yml)'s own header comment for what the review actually checks (accuracy, staleness, clarity, completeness — not style).
