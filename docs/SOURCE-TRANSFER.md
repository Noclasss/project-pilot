# Safe source-transfer plan

Project Pilot is intended to be published as a **new, reviewed export**. Do not transfer the old private repository's commits, branches, tags, pull-request metadata or Git history.

## What is already public

This repository contains only independently written public-safe documentation, contribution guidance, and sanitised issues. It contains no copied private implementation source.

## What can be transferred next

After exact-tree review and authorisation:

1. Establish the candidate commit, tree, inventory and checksums.
2. Review every proposed file for secrets, private identifiers, internal paths, personal metadata, and licence restrictions.
3. Include only needed plugin code, required manifests, generic example configuration, relevant tests, and release documentation.
4. Fix Project Pilot branding without renaming persistent data identifiers in a way that loses state.
5. Re-run full tests and supported disposable runtime installation/recovery checks.
6. Record the final approved file inventory and provenance decisions.
7. Add the reviewed files as **new public commits**, rather than importing private commit ancestry.
8. Verify public Git contents against the approved source archive before tagging.

## Not transferable without independent review

- Existing private Git history or author-email metadata.
- Private repository issue descriptions, links, conversations, and credential troubleshooting.
- Local `.env`, tokens, service endpoints, machine paths, or production state.
- Development artifacts, diagnostics, or datasets containing identifying information.
- Third-party code with unclear redistribution rights.

## Preserving progress

The public [roadmap](ROADMAP.md), [feature catalogue](FEATURES.md), and [issues](https://github.com/Noclasss/project-pilot/issues) capture the generic goals, acceptance criteria, feature areas and release blockers without leaking private history.

The local candidate reportedly passed 229 offline tests. That result must be re-established on the exact code ultimately uploaded.
