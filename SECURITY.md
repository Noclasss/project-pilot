# Security policy

## Current status

This repository is a **pre-release project home**. No executable version of Project Pilot is published here yet, so there is no supported public release or security-fix schedule.

## Reporting a vulnerability

Please **do not** put credentials, tokens, internal addresses, user data, exploit details, or private repository contents in a public issue or pull request.

If GitHub's private vulnerability reporting is available for this repository, use **Security → Report a vulnerability**. Otherwise contact the repository maintainer through an existing private channel before sharing sensitive details. Do not assume a private reporting feature is enabled.

Public issues may be used for non-sensitive, general security design improvements.

## Security expectations for future releases

- Explicit repository allowlist on every access path, including cached/dashboard views.
- Minimum necessary GitHub and host permissions.
- No implicit background execution or secret access.
- Distinguish live verification from stale, offline, or self-reported state.
- Keep production project data and credentials out of tests and public fixtures.
- Validate recovery and rollback without overwriting live state.
- Review external dependencies and source provenance before publication.

No public audit, certification, or vulnerability-free guarantee is claimed.
