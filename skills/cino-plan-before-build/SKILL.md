---
name: "cino-plan-before-build"
description: "Generic coordinator for non-trivial authorised implementation when no stricter specialist/project workflow owns the work; skip for pure routing, read-only navigation, test-selection-only, and skill lifecycle work."
category: "Cino StarNet"
state: "active"
created_by: "agent02b-candidate"
pinned: false
---

# cino-plan-before-build

1. Define outcome, protected behavior, exact scope and stop condition.
2. Separate authority gates: inspect/plan; local edit; commit; push; merge; deploy/publish/shared/live mutation. Never infer a later gate.
3. Use source-of-truth only for a material unresolved authority question; repo-navigator only when the change surface is unclear.
4. Make the smallest implementation plan, then edit only within the authorised boundary.
5. Use test-router once verification selection is needed. Apply its focused-tests-first ladder and repeated-failure circuit breaker.
6. Verify actual result and side effects.
7. At completion load evidence-handoff once and stop.

A specialist/project procedure has precedence. Skill-layer lifecycle work belongs to cino-skill-governor.
