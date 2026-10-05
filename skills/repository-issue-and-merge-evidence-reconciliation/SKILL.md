---
name: "Repository Issue and Merge Evidence Reconciliation"
description: "Read-only workflow for verifying repository issue authority, implementation PR evidence, and inclusion in a designated current branch or release."
category: "Software development"
state: "active"
created_by: "background-review"
source_run_id: "8cf71d17-6dd3-4142-a59b-5a3b8f3bda38_skill_review"
pinned: false
---

# Repository Issue and Merge Evidence Reconciliation

Use this procedure when asked to determine whether repository issues are already implemented and included in a named current branch/release, especially when an issue may be ready to close. Keep the review within the requested repository and tickets, and make no mutations unless separately authorized.

## Procedure

1. **Establish scope and evidence sources.** Identify the exact repository, issue numbers, candidate PRs, and the named current branch/release or source commit. Read the supplied work order if accessible. Do not inspect unrelated project lanes. Treat a supplied snapshot as a lead, not as independent verification.
2. **Check access before asserting findings.** Use only available authorized repository sources. If a credentialed request or connector is unavailable or blocked, stop trying that route unless the required fresh authorization is explicitly provided. Do not represent an attempted/blocked request as successful network access. Do not treat general web search as a substitute for authoritative issue, PR, or commit records.
3. **Read each issue's authority and history.** Capture current state and the operative acceptance criteria. Review comments and identify the latest authoritative scope clarification; distinguish it from older or superseded wording. Record the exact URL/path read and relevant facts.
4. **Verify candidate implementation PRs.** Independently inspect PR state, merge status, merge commit, issue linkage, and the PR's implementation/test evidence. A merged PR or passing checks alone does not prove every authoritative requirement is satisfied; compare evidence against the operative issue criteria.
5. **Verify current inclusion.** Obtain the named current source branch/release SHA from an authoritative source and verify that the relevant merge commit(s) are ancestors/included. If this relationship cannot be checked, report it as unverified rather than inferring from a supplied claim.
6. **Reach a per-ticket verdict.** Use **stale-open/close-ready** only when authoritative issue criteria are matched by implementation evidence and the implementation is included in the named current source. Otherwise use **evidence gap**, naming exactly what is missing or unverifiable. Do not close or edit issues during a read-only review.
7. **Report with provenance.** For each ticket, state source-specific facts and exact URLs or paths successfully read. Separate independently observed facts from supplied-but-unverified claims. Include unknowns/capability limits and explicit attestations: whether network access succeeded, and whether any mutations occurred.

## Safety and accuracy

- A blocked request means no evidence was retrieved from that request. State that plainly; do not imply a successful read.
- If an external-content safety boundary requires fresh confirmation, do not retry blindly or bypass it through another route. Finish only what authorized local evidence supports and identify the exact missing access.
- Never claim a branch ancestry result, test result, comment, or merge fact based solely on a work-order snapshot when the task requests independent verification.
- Keep evidence and verdicts scoped to the named tickets and repository.
