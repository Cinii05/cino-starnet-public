---
name: "cino-test-router"
description: "Use when choosing the smallest sufficient verification set or after an authorised change needs verification; do not activate merely because tests exist."
category: "Cino StarNet"
state: "active"
created_by: "agent02b-candidate"
pinned: false
---

# cino-test-router

1. State the claim and known change surface.
2. Classify environment: LOCAL / ISOLATED / SHARED / LIVE and effect: PURE / READ-ONLY / MUTATING.
3. Choose the lowest rung that proves the claim: focused unit/static -> targeted integration -> broader regression/build -> isolated rendered/E2E -> shared/live only when necessary.
4. Reuse fresh passing evidence only when code/config/environment identity is unchanged.
5. Escalate after a meaningful failure/coverage gap, not automatically.
6. If the same substantive failure occurs twice without a meaningful change, stop rerunning it and diagnose the signature before any broader retry.
7. Shared/live mutating verification requires exact authority for its side effect.
8. Report what ran, exact result, scope it proves, and what remains unverified.
