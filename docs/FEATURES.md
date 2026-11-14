# Feature catalogue and verification status

The listed tools and design areas are taken from the private project's documented interface and release-candidate reports. **No implementation code is published in this repository yet.** Claims below distinguish offline checks from verified live Hermes operation.

## Plugin interface planned for public release

| Hermes tool | Intended responsibility | Public/runtime status |
| --- | --- | --- |
| `project_status` | Show project state and bounded evidence | Implementation not public; runtime unverified |
| `project_verify` | Check whether stated project progress has evidence | Implementation not public; runtime unverified |
| `project_next` | Recommend a next bounded action | Implementation not public; runtime unverified |
| `project_integrity` | Detect integrity and readiness problems | Implementation not public; runtime unverified |
| `project_task_state` | Maintain/retrieve task and goal context | Offline compatibility tested; runtime unverified |
| `project_task_cycle` | Record and recover task cycle/checkpoint context | Offline compatibility tested; runtime unverified |

The product's intention is to turn repository observations into reliable next actions. Tools must not claim that work was completed simply because a stored record or AI response says so.

## Project and GitHub scope

- The repository allowlist must be explicit.
- Missing, malformed, repeated, oversized, or unsafe repository entries must be rejected.
- Narrowing an allowlist must remove previously allowed repositories from live reads, snapshots served by the dashboard, and recommendations.
- Credential failure must never be treated as permission to read outside the configured scope.

The local release candidate reportedly passed **229 offline tests**, including relevant allowlist, dashboard, task and checkpoint tests. Live runtime checks remain open.

## State compatibility

The implementation historically used an internal persistent-storage identifier, `jarvis-project-manager`. A public-facing rename must preserve compatibility with relevant existing records, not blindly rename the state location.

## Delegation and autonomous dispatch

These are goals subject to explicit isolation, credential, and per-worker capability boundaries. They are **not** included in the initial verified public project state. A successful planning demo cannot stand in for a secure delegation demonstration.

## Definition of a useful milestone

A feature is useful when it helps the agent complete the sequence:

**goal → task selection → permitted action → independent check → durable checkpoint → accurate recovery**.

See [the acceptance issue](https://github.com/Noclasss/project-pilot/issues/6).
