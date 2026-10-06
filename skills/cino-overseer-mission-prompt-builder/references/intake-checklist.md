# Mission intake checklist

Use this as a coverage map, not a questionnaire to dump on the user. Skip categories already known or safely delegated to CALLUS.

## Mission identity
- What concrete end state should exist when the mission is finished?
- Why does this mission matter now?
- Is this a continuation/recovery of existing work or a fresh mission?
- What exact project/product/repository/workspace does it concern?

## Starting state
- What is already done, merged, deployed, sealed, accepted or known-good?
- What is currently broken, incomplete, blocked or stale?
- Which current SHA/version/environment/handoff is authoritative?
- Are there active agents/lanes that must be resumed rather than duplicated?

## Scope
- Required outcomes.
- Explicit exclusions and no-touch areas.
- Nice-to-have work that must not block completion.
- Whether discovery may expand scope automatically or only propose follow-up.

## Authority
Separate authority for:
- read/inspect/research;
- local edits;
- tests/builds;
- commits;
- pushes/PRs;
- merges;
- deploys/publication;
- external messages/email;
- secrets/credentials;
- spending/billing;
- destructive or irreversible actions.

Never infer a later authority gate from an earlier one.

## Evidence and source of truth
- Repos, branches, SHAs, handoffs, Drive folders, issues, docs, production/Pilot environments.
- Freshness requirements.
- Which sources outrank others if they conflict.
- Whether CALLUS may retrieve missing evidence autonomously.

## Execution constraints
- Deadlines or urgency.
- Token/cost/model constraints.
- Required/forbidden tools or providers.
- Environment constraints.
- Concurrency limits.
- Existing “no preview”, “read-only”, or similar operational rules.

## Delegation preferences
Only ask where the user cares about a specific assignment.
- Any required specialist/reviewer/auxiliary?
- Any agent that must not be used?
- May CALLUS decide all other routing dynamically?
- Is parallel execution preferred where dependencies permit it?

## Quality and acceptance
- Functional success criteria.
- Required regression/QA/rendered/runtime evidence.
- Performance/security/privacy requirements.
- Required independent reviewer.
- What constitutes an acceptable residual issue versus a blocker.

## Recovery
- What should happen after a tool failure?
- What counts as repeated failure?
- What makes an active agent stale?
- May CALLUS resume/reassign/recover autonomously?
- What specifically counts as a genuine human blocker?

## Deliverables
- Code, PRs, deploys, reports, ZIPs, screenshots, evidence indexes, handoffs.
- Required destination(s).
- Whether same artifact/hash must appear in multiple locations.
- Final summary format.

## Stop condition
- Exact Definition of Done.
- Conditions under which CALLUS must stop engineering.
- Whether follow-up findings should be recorded separately rather than absorbed.
