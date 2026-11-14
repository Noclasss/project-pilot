# Project Pilot

**AI-powered project management for Hermes agents.**

> **Pre-release:** This public repository is the project home, not yet an installable plugin. The implementation and release artifacts have not been published. No live or production deployment is endorsed.

Project Pilot aims to help a Hermes agent turn project goals into trackable work, inspect evidence, maintain checkpoints, and decide the next safe action. The design prioritises **visible progress, recoverable state, bounded permissions, and explicit verification** rather than unbounded autonomous execution.

## Planned capabilities

- **Project overview:** repository-scoped status and dashboard snapshots.
- **Task and goal tracking:** durable task state, stable goal links, and next-action notes.
- **Checkpoints and recovery:** records that let a later session understand what happened and what remains.
- **Evidence-first GitHub integration:** read-only project discovery and verification where configured and authorised.
- **Integrity controls:** repository allowlists and clear distinctions between reported, verified, and unavailable information.
- **Managed progression:** propose work, carry out permitted actions, verify results, and record outcomes. Delegation is a future gated capability, not a claim of current production readiness.

The implementation is being prepared separately. These descriptions are project goals or offline-tested feature areas; they are **not** a promise that public releases already provide them.

## Status

The release candidate was reported locally committed and its **229 offline tests passed**. Those tests are not proof of a clean installation, safe upgrade, production recovery, security clearance, or permission to redistribute the implementation.

| Gate | Status |
| --- | --- |
| Public project home | Complete |
| Offline candidate test suite | Passed locally; code not published here |
| Redistribution rights and license decision | Pending |
| Security, privacy, and dependency review | Pending |
| Clean export and branding review | Pending |
| Fresh install, upgrade, recovery, and rollback | Pending |
| Public plugin release | Not approved |

See [release gates](docs/RELEASE-GATES.md) and the [roadmap](docs/ROADMAP.md).

## Safety and scope

Project Pilot is designed to use an **explicit repository allowlist**. It must not assume access to other repositories or silently infer permissions. Dashboard or task evidence can be stale or incomplete; it must not be described as verified live status without supporting checks.

Never publish secrets, personal data, private repository material, internal hostnames, or credentials in issues and pull requests. See [security guidance](SECURITY.md).

## Getting involved

The public [issue tracker](https://github.com/Noclasss/project-pilot/issues) is used for the sanitised development plan and release blockers. See [contributing](CONTRIBUTING.md).

## Licensing

**No license is granted at present.** Redistribution rights and third-party obligations are still being reviewed. Please do not assume the eventual license or copy in code from the private development history.

The project intends to make a separately reviewed and appropriately licensed public release when the gates are met.
