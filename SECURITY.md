# Security Policy

This is the org-wide default security policy for every repository under
**Project-Arrakis** that doesn't define its own `SECURITY.md`. GitHub
falls back to this file automatically for any repo lacking one.

## Reporting a vulnerability

Please **do not** open a public GitHub issue for a security
vulnerability. Instead, use GitHub's private vulnerability reporting:

1. Go to the repository's **Security** tab.
2. Click **Report a vulnerability** under "Advisories".

If a repo has its own `SECURITY.md` with different instructions (for
example, an email address or a different disclosure process), follow
that repo's instructions instead — this file is the fallback for repos
that don't.

## Supported versions

Most repos in this org are pre-1.0 or track an upstream fork's own
version numbering. Unless a repo's own `SECURITY.md` or `README.md`
says otherwise, only the latest release and the `main` branch are
supported.

## Scanning

Every repo in this org runs (or is migrating to) a shared secret/SAST/
filesystem-vulnerability scan — see
[`workflows/reusable-security-scan.yml`](workflows/reusable-security-scan.yml)
— plus native GitHub secret scanning and push protection where enabled.
Findings are tracked as GitHub issues labeled `security` on the
relevant repo.
