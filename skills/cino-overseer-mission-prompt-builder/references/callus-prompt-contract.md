# CALLUS launch prompt contract

The final prompt should use the following structure when relevant. Omit empty sections; do not invent content merely to fill a heading.

## Opening command
Tell CALLUS that it owns the mission end to end and should continue autonomously until the Definition of Done is satisfied, stopping only for the stated human-blocker conditions.

## Mission
A short, unambiguous statement of the desired end state.

## Current authoritative state
Identify the exact known starting point: repository/worktree/branch/SHA/version/environment/handoff or other authority, when known.

State what is already accepted so CALLUS does not restart completed work.

## Required outcomes
Concrete outputs and observable behaviors.

## Scope and no-touch boundaries
What CALLUS may change and what it must preserve or leave alone.

## Evidence / source-of-truth contract
Tell CALLUS where to look first, what source outranks what, and to retrieve narrowly rather than ingesting everything.

## Authority
State the highest authorised action level. Separate any actions that require later human approval.

## Planning instruction
Tell CALLUS to:
- use StarNet mission intake/planning rather than blindly following the wording as a task list;
- extract objectives, constraints and ambiguity;
- build the minimum sufficient dependency-aware plan;
- identify the critical path and immediately runnable lanes;
- choose the smallest safe crew using the live agent router;
- preserve ownership seams;
- define per-lane Definition of Done and evidence requirements;
- replan dynamically when evidence changes.

Do not precompute this plan inside the prompt unless the user explicitly wants a fixed plan.

## Execution policy
Include relevant requirements such as:
- focused tests first;
- reuse fresh authoritative green evidence;
- repeated-failure circuit breaker before a third blind rerun;
- recover stale agents rather than duplicate-dispatching;
- continue through recoverable tool failures;
- do not ask the Commander for information available to authorised tools/sources;
- keep context bounded through evidence pointers and the context funnel.

## Human-blocker policy
Define precisely what must return to the user. A common pattern is:
“Stop only when a decision, credential, approval, physical action, account-owner action or unavailable evidence genuinely requires the Commander. If the problem can be diagnosed, repaired, rerouted or worked around safely within authority, do that and continue.”

## Quality gates
State the required tests, independent review, runtime/rendered evidence, security checks, performance checks or acceptance matrices.

## Deliverables and handoff
State required artifacts, destinations, hashes, issue/PR updates and final evidence.

## Definition of Done
Use observable completion conditions. End with an explicit instruction to stop further engineering once all mandatory gates are green and package/report the final result.
