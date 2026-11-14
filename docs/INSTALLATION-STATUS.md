# Installation status

**There is no supported public installation procedure yet.**

The public repository does not currently contain the Hermes plugin package. Do not use `git clone` of this repository as an installation step expecting working project-management tools.

The separately prepared local candidate passed 229 offline tests according to the maintainer's report. A clean installation, upgrade from existing state, fresh-session recovery, and rollback have **not** been demonstrated in an approved isolated Hermes runtime.

## Required before publishing installation instructions

- Exact tested Hermes version compatibility.
- Verified plugin manifest and install command in a disposable environment.
- Documented repository allowlist configuration using synthetic examples.
- Safe handling of existing project/task/checkpoint state.
- Verified rollback procedure.
- Clear warnings for unavailable GitHub access, stale snapshots, and optional integrations.

No production installation, credential configuration, or background agents should be changed based only on this document.
