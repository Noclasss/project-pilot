# Release readiness and evidence

**Status: NOT READY for publication of implementation code.**

This document records an independently understandable summary of the release gates. No public code release is authorised by this checklist.

## Candidate baseline

The maintainer's local report describes:

- A clean local, independent root commit: `8308fffaad7174832cf550e20788e0efb499fa95`.
- Tree hash: `7fafa6aa4f27abbfab984f5f595773ba057ea2aa`.
- File count: 40.
- Offline test result: **229 passed, 0 failures, 0 errors, 0 skipped**.
- An `origin` pointing at this public repository, with **no candidate push performed**.

Those values describe a **local** candidate. They are not a public Git commit here and were not rechecked by this repository.

## Gate status

| Gate | Status | Evidence required |
| --- | --- | --- |
| Independent clean candidate tree | Reported complete | Verify exact tree, file inventory, and commit parents |
| Offline test coverage | Reported passed | Re-run on exact releasable tree |
| Explicit repository allowlist | Offline tested | Verify all live access paths and stale dashboard responses |
| Sensitive data and secret review | Incomplete | Complete file and history scans on exact proposed export |
| Third-party dependencies | Incomplete | Inventory imports, versions, licences, vulnerability advisories, notices |
| Source rights and redistribution | **Blocked** | Establish ownership, provenance, and compatible licensing terms |
| Branding and public documentation | Incomplete | Consistent public product name, installation and upgrade docs |
| Checkpoint/auth recovery reconciliation | Incomplete | Review relevant unmerged changes and document disposition |
| Fresh supported Hermes installation | Not demonstrated | Disposable runtime installation evidence |
| Upgrade, recover, rollback | Not demonstrated | Evidence using non-production fixtures and supported methods |
| Final signed-off public source and license | **Blocked** | Release review and explicit maintainer approval |

## Non-negotiable release rules

- **Never push or merge private Git history** into this repository.
- Do not treat an offline test pass as proof of runtime isolation, credential boundaries, or install compatibility.
- Do not copy secrets, internal IPs, host paths, account identifiers, private repository URLs, or user data.
- Do not add an open-source licence until rights and compatibility are confirmed.
- Do not enable GitHub Actions or external scanners on unpublished private candidate code without a separate review.
- Do not present a planned behaviour as a tested production capability.

## Publication sequence

1. Review and fix the local candidate; record a new exact commit if changed.
2. Approve the source and third-party licensing/notice decision.
3. Run all required audits, offline tests, and disposable-runtime checks on that exact source.
4. Create a new public history containing **only reviewed export files**.
5. Check the public Git tree against the approved inventory and checksums.
6. Tag and document a release only after sign-off.

The public repository may host general documentation and non-sensitive planning issues before these gates pass.
