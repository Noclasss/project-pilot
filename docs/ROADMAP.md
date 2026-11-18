# Project Pilot roadmap

This is a **public, sanitised plan**. It does not copy the private source repository, issue discussion, or Git history.

## Next milestone

Run the [disposable Hermes recovery test](https://github.com/Noclasss/project-pilot/issues/3) on one identified candidate. Use that installation to [exercise repository scope](https://github.com/Noclasss/project-pilot/issues/7) and [resume a project goal from a checkpoint](https://github.com/Noclasss/project-pilot/issues/6). Record the candidate revision, Hermes version, observed results and outstanding checks together so another session can reproduce them. The demonstration can run before public release.

## Phase 0 — Establish a public project home

- [x] Create the public repository.
- [x] Publish an honest pre-release README.
- [x] Establish the [public issue backlog](https://github.com/Noclasss/project-pilot/issues).
- [ ] Confirm contribution and licensing policy.

## Phase 1 — Make a release candidate eligible for publication

- [ ] Establish code ownership and permission to redistribute each component.
- [ ] Resolve third-party dependency and licence obligations.
- [ ] Complete secret, sensitive-data, privacy, and provenance review of the **exact** candidate tree.
- [ ] Use consistent Project Pilot user-facing branding; preserve the legacy storage key if compatibility requires it.
- [ ] Reconcile relevant checkpoint and authentication recovery work, without copying unrelated private history.
- [ ] Produce a reproducible inventory, source archive, and checksums.
- [ ] Re-run offline tests after any candidate changes.

## Phase 2 — Prove installation and recovery

- [ ] Install in a disposable, supported Hermes environment.
- [ ] Demonstrate an initial project setup using an explicit repository allowlist.
- [ ] Verify upgrades can read legacy snapshots, task records, and checkpoints.
- [ ] Demonstrate recovery after a failed or interrupted task cycle.
- [ ] Demonstrate rollback with no mutation of production state.
- [ ] Confirm the plugin does not grant unapproved tool access or background execution.

## Phase 3 — First code release

Only after the publication gates pass and the maintainer explicitly approves:

- [ ] Publish a **clean, reviewed source snapshot**, not the private development history.
- [ ] Include a suitable licence and required third-party notices.
- [ ] Tag an initial pre-release with the tested commit and checksums.
- [ ] Publish verified installation, upgrade, and rollback instructions.
- [ ] Clearly document unsupported integrations and unverified runtime properties.

## Phase 4 — Prove the project manager improves outcomes

A useful Project Pilot must progress a real project, not only report status:

1. A user selects a project and objective.
2. The agent identifies the next bounded task and records the reason.
3. The agent performs an authorised action, or identifies the exact missing permission.
4. The agent checks evidence, records the outcome, and updates the checkpoint.
5. A new session can recover context and continue without inventing previous success.

Delegation and autonomous dispatch require their own tool boundaries and verification. They must not be enabled merely because offline planning tests pass.

## Planned feature — cost-aware model selection

The [Smart Model Router](https://github.com/Noclasss/project-pilot/issues/8) starts with an offline preview. For a bounded task, recommend the cheapest eligible configured model and explain the capability, privacy and cost checks behind the choice. Default additional paid API spend is £0. Fixtures should cover a local model outage, exhausted free quota and unknown pricing. Each case must produce an eligible route or an explicit reason to stop, with zero provider calls.

Live routing and paid escalation require separate verification and owner authorisation. The preview can be developed independently of the first release.

See [release gates](RELEASE-GATES.md) and [architecture](ARCHITECTURE.md).
