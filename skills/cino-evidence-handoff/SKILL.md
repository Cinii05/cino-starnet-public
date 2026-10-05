---
name: "cino-evidence-handoff"
description: "Use once at a worker/task completion boundary to emit a compact evidence-grade handoff; do not preload during implementation."
category: "Cino StarNet"
state: "active"
created_by: "agent02b-candidate"
pinned: false
---

# cino-evidence-handoff

Emit one handoff with: task status; verification status; exact repo/project/branch/SHA/version where relevant; scope; concrete evidence pointers; changes; persistent side effects; unknowns/conflicts; and one smallest safe next action (or none if complete). Preserve authority/no-touch constraints and provenance. Distinguish supplied claims from independently checked evidence. Never dump a transcript, invent a PASS, omit side effects, expose secrets, or create a successor task merely to keep working.
