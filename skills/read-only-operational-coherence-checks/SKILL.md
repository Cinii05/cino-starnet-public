---
name: "Read-only operational coherence checks"
description: "A repeatable procedure for narrowly scoped, evidence-bounded operational checks, especially supplied-Pilot identity and merge-inclusion reviews."
category: "operations"
state: "active"
created_by: "background-review"
source_run_id: "9ef89b04-b206-48dd-ba81-185156e18d4f_skill_review"
pinned: false
platforms: ["any"]
---

## Setup
No special setup. Follow the user's supplied evidence and explicit scope constraints; do not independently inspect unless authorized.

# Read-only operational coherence checks

Use this procedure when asked to assess whether supplied repository/commit facts coherently support a narrowly scoped operational conclusion, while avoiding independent inspection or actions not authorized by the work order.

## 1. Parse the boundary before assessing evidence
- Extract the exact requested subtask and the explicit exclusions (repositories, lanes, systems, environments, or people not to inspect).
- Identify whether the task is supplied-evidence-only or permits independent verification. Do not silently upgrade a supplied snapshot into verified facts.
- Record access and action constraints: read-only, network restrictions, whether issue closure or other workflow actions are prohibited.
- Keep conclusions confined to the requested scope; do not take ownership of adjacent workstreams.

## 2. Normalize the supplied identity and provenance facts
Write down the exact repository/project identity and immutable identifiers as provided, including full source/Pilot SHA where available. Distinguish:
- a commit mentioned in a report from one independently inspected;
- a stated ancestry relationship from verified Git ancestry;
- a stated worktree HEAD from an observed HEAD;
- a merged PR/commit fact from a runtime deployment fact.

For a merge-inclusion check, enumerate every required merge commit and the exact target/source identity it is claimed to be included in. Only assess inclusion if the supplied evidence explicitly states the ancestry relationship or otherwise gives adequate provenance. Report the result as supported by the snapshot, not independently verified, unless actual verification was authorized and performed.

## 3. Check scope coherence and prohibited dependencies
- Compare the requested operational identity with the exact supplied source identity; call out mismatches or missing links rather than filling them in.
- Respect explicit prohibitions such as a forbidden Preview deployment. State that the assessment did not rely on that source.
- Do not infer that an entire workflow or system is independent of a prohibited service merely because this particular check did not use it. Phrase the conclusion narrowly: this check used the supplied identity and did not rely on the prohibited dependency.
- Do not inspect excluded lanes, systems, or repositories, even to resolve uncertainty.

## 4. Enforce claim boundaries
Separate the conclusion into what the supplied evidence supports, what it does not establish, and what remains unknown. Merge inclusion or source identity does not by itself establish runtime health, deployment identity, release readiness, or production behavior. Do not make such claims unless specifically evidenced and within scope.

## 5. Report evidence and limitations transparently
Use a concise structure:
1. Exact evidence inspected (enumerated, using supplied identifiers verbatim).
2. Assessment of merge inclusion and scope coherence, explicitly labeling source-reported versus independently verified facts.
3. Unknowns and capability/inspection limits.
4. Explicit network and mutation attestations, plus any required workflow-action attestation (for example, no issue closure).

Never claim no network activity or no mutations unless that is true for the run. If a tool was used, describe its actual scope accurately. A read-only task may still involve external reads; report what happened rather than assuming otherwise.

## 6. Stop at the requested subtask
Do not close issues, publish a release, deploy, alter repository state, or perform adjacent work unless explicitly authorized. Avoid a broad “done” claim when only a narrow coherence check was completed.
