---
name: "cino-agent-router"
description: "StarNet fleet routing coordinator. Use only when work may benefit from delegation, role selection, stale-agent recovery, or explicit auxiliary/reviewer dispatch; skip for trivial direct work."
category: "Cino StarNet"
state: "active"
created_by: "agent02b-candidate"
pinned: false
---

# cino-agent-router

## Primary fleet
The ordinary StarNet crew is exactly: CALLUS (orchestrator), SOL (difficult/release-sensitive engineering), TERRA (bounded implementation/tests), RESEARCH (read-only research/evidence), QA (independent acceptance/adversarial verification), OPS (runtime/deployment/environment evidence).

OPUS is an isolated reviewer, not crew. GEMINI-SCOUT and GEMINI-SENIOR are explicit-dispatch auxiliaries, not crew and never automatic fallbacks.

## Deterministic precedence
Apply the first matching rule:
1. If OPUS or a Gemini auxiliary is explicitly requested, dispatch only that named auxiliary/reviewer and preserve its isolation. Never substitute or auto-enlist another auxiliary.
2. Malformed/empty/inaccessible request: do not delegate or guess. Ask for the minimum readable input unless a prior explicit task can be safely restated for confirmation.
3. A stale already-active agent is recovery, not new routing: inspect its run/chat/evidence; resume the existing sequence if safe; never duplicate-dispatch the same lane.
4. Runtime/deployment/environment/credential-availability evidence work -> OPS.
5. Research, source collection, issue/PR reconciliation, or multi-source evidence synthesis -> RESEARCH.
6. Independent acceptance, adversarial QA, rendered/regression verification -> QA.
7. Difficult, cross-repository, architecture-heavy, or release-sensitive engineering -> SOL.
8. Bounded implementation, focused tests, repetitive coding, narrow debugging -> TERRA.
9. Cross-lane orchestration/synthesis or tasks that must route several roles -> CALLUS.
10. Trivial work that the current agent can complete safely -> no delegation.

A specialist/project workflow may own how the task is performed; this router owns who should perform a delegated role. Routing never enlarges authority.

## Brief
A dispatch brief must carry objective, exact scope, authority/no-touch constraints, relevant current context/evidence pointers, required evidence, fallback/recovery rule, and stop condition. Avoid context dumps.

## Stop
Do not fan out for opinions. Do not ask the Commander to resolve information already available to the current run. Escalate only a genuine Human Authority decision/blocker or an evidence/access gap that no authorised route can resolve.
