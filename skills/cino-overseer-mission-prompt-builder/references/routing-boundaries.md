# Routing boundaries

## This skill owns
- eliciting a new StarNet mission from the Commander;
- resolving user-level ambiguity before launch;
- compiling one self-contained first prompt for CALLUS/the overseer;
- preserving user constraints, authority and Definition of Done.

## This skill does not own
- executing the mission;
- decomposing the live mission into the final dependency DAG;
- choosing or dispatching the live agent fleet;
- monitoring stale agents after launch;
- repository implementation;
- testing;
- evidence reconciliation;
- release/deployment actions.

## Neighbouring skills
- `grill-me`: generic plan/design interrogation. Prefer this StarNet skill when the desired artifact is specifically a CALLUS/overseer launch prompt.
- `cino-agent-router`: chooses who performs delegated work after/within mission planning.
- `cino-plan-before-build`: coordinates authorised implementation after a concrete execution objective exists.
- `cino-context-funnel`: narrows evidence needed to prove a material claim.
- `cino-source-of-truth`: resolves genuine source-authority conflicts.
- `cino-evidence-handoff`: packages execution evidence at completion.

If a user merely says “route this task,” use the agent router, not this skill. If they say “help me work out exactly what I should send to StarNet/CALLUS first,” use this skill.
