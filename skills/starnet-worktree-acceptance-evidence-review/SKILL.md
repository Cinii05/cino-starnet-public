---
name: "StarNet Worktree Acceptance Evidence Review"
description: "A repeatable, evidence-led workflow for assessing implementation acceptance criteria in a bounded worktree, separating static source/test evidence from executed verification and preserving explicit unknowns."
category: "engineering"
state: "active"
created_by: "background-review"
source_run_id: "36b32089-85f8-45be-8470-1fad5004cb28_skill_review"
pinned: false
---

# StarNet Worktree Acceptance Evidence Review

Use this procedure for a scoped, read-only review of issue or pilot acceptance criteria in a named StarNet worktree. The goal is an honest evidence assessment, not a substitute for CI or a browser journey. Do not modify the worktree unless the user separately authorizes implementation.

## 1. Establish the review boundary

1. Identify the exact worktree path, requested issue(s), acceptance contract, and target commit if supplied.
2. Read the worktree's local contributor instructions and environment notes before interpreting or running project checks.
3. Keep inspection within the named worktree. Do not inspect another lane, worktree, preview, or shared system unless explicitly authorized.
4. Treat requested non-actions (for example, no edits, no Preview, or no network) as hard boundaries.
5. Separate acceptance criteria into individually assessable claims. Avoid rolling several distinct behaviors into one broad pass/fail statement.

## 2. Verify identity and capability before claiming execution

1. Verify the checked-out revision using an allowed method. If protected metadata prevents reading Git state, state that exact HEAD is unverified; do not infer identity from directory names or source contents.
2. Inventory available execution capability and dependencies before proposing or reporting tests. Running no command means tests, typecheck, lint, and build are unverified, even if scripts exist.
3. Run only checks permitted by the contract and environment instructions. Record exactly which commands/checks ran and their outcomes; never fabricate results.
4. If execution is unavailable, continue with source/test inspection when useful, but label the result as static evidence and name the smallest safe next validation step.

## 3. Build an evidence map

For each acceptance claim, inspect the most direct implementation and focused tests. Prefer narrow searches and then read complete relevant sections. Record paths and the specific behavior each source or test supports.

Classify evidence precisely:

- **Source evidence:** implementation appears to provide the behavior.
- **Focused test evidence:** a test asserts the behavior, but this is not proof the test passed unless it was run.
- **Executed evidence:** named check actually ran and passed in the reviewed worktree.
- **Rendered/manual evidence:** an app journey or browser interaction was actually exercised.
- **Unverified:** no adequate evidence was gathered, or a relevant tool/check was unavailable.

Do not turn absence from a narrow text search into proof of absence throughout the app. For negative requirements (for example, “no separate button”), use a sufficiently broad rendered or structural check; otherwise state that absence was not established. Likewise, source-level accessibility attributes or styles do not prove keyboard usability, responsive behavior, or assistive-technology behavior without exercising those outcomes.

## 4. Check boundaries and regressions

1. For presentation-only changes, verify that governed identifiers, payload shapes, saved-value round-trips, and downstream semantics are unchanged where relevant. Treat comments asserting “presentation only” as intent, not proof.
2. For jurisdiction, eligibility, or conditional visibility, inspect both the current-state path and transitions/clearing or historical-data paths. Look for unintended submission of stale answers.
3. For protected navigation or focus behavior, inspect the decision logic and focused tests; do not claim end-to-end usability without an actual journey.
4. Distinguish requirements that are demonstrated from those that remain missing, especially conditional guidance or “where relevant” behavior.

## 5. Report a calibrated verdict

Use a verdict such as **PASS**, **PARTIAL**, or **UNVERIFIED**, and explain its scope. Summarize:

- worktree/revision identity status;
- evidence reviewed, with relevant paths;
- criteria supported by source, tests, executed checks, and rendered checks separately;
- residual acceptance gaps and limitations;
- commands/checks not run and why;
- any requested mutation/network boundaries honored;
- the smallest safe next action to close the highest-value gap.

Do not repeat transient tool failures as durable lessons. Capture only the reusable recovery pattern: use an allowed verification path, report unavailable evidence as unverified, and avoid substituting inference for execution.

## 6. Finish without unauthorized changes

A verification-only review leaves files and shared state untouched. Do not fix gaps during the audit unless explicitly asked to implement. The report should make it possible for another authorized session to perform the next check without mistaking static inspection for completed acceptance.
