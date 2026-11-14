# Architecture overview

This is an overview of the intended and offline-tested design, **not** a claim that a public executable plugin is available.

## Design priorities

- **Bounded scope:** repositories must be explicitly allowed, never inferred from the host or credentials.
- **Evidence over assertion:** separate observed facts, saved snapshots, user reports, unknowns, and verified results.
- **Persistent recovery:** retain enough task and goal context to resume work in a new conversation.
- **Manual control:** sensitive or state-changing actions remain subject to explicit permissions and verification.
- **Compatibility:** preserve historical state keys where necessary to avoid data loss.

## Conceptual components

| Component | Purpose |
| --- | --- |
| Repository configuration | Validates explicit repository allowlists and narrows all permitted reads |
| GitHub evidence adapter | Retrieves repository, issue, pull request, and commit information within configured scope |
| Snapshot store | Saves project status with clear freshness and verification limitations |
| Dashboard API | Presents filtered, read-only views without resurrecting removed repositories from stale snapshots |
| Task state and goal context | Records task identifiers, goals, advisory next actions, and completion claims |
| Task-cycle/checkpoint state | Captures progress and recovery context across sessions |
| Progression controller | Suggests next bounded actions and records evidence for outcomes |
| Integrity and policy checks | Detects missing prerequisites, unsafe transitions, and unsupported claims |

## Trust boundaries

Repository allowlists are a configuration boundary; they do **not** themselves grant or revoke filesystem, network, GitHub, or host-level permissions. Actual credentials and tool capabilities must be separately constrained.

A project dashboard may show saved information even when live access is unavailable. Such content must be labelled accordingly; a stale snapshot cannot certify the current repository state.

Offline compatibility fixtures can verify record parsing, but they do not demonstrate safe migration of production data or operational rollback.

## Delivery model

The intended release is a Hermes plugin with read-only project status, bounded task state, checkpoints, and reviewable progress. Autonomous worker dispatch is **not enabled or verified** by the public project-home setup. Any future delegation implementation must first show effective per-worker capability restrictions.

## Success criterion

A real task cycle must show **goal → scoped next action → authorised execution → evidence check → checkpoint → recoverable next step**. A dashboard alone is insufficient.
