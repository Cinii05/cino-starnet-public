---
name: "cino-overseer-mission-prompt-builder"
description: "Build the first high-fidelity mission prompt for a StarNet overseer/CALLUS from rough intent. Use when the user wants to prepare, refine, or be interviewed for the prompt that launches a new StarNet mission; resolve material ambiguity before producing the handoff. Do not execute, decompose, route, or manage the mission itself."
category: "Cino StarNet"
state: "active"
created_by: "cino-starnet-v1.1.0"
pinned: false
---

# Cino Overseer Mission Prompt Builder

Turn a rough mission idea into one authoritative launch prompt for the StarNet overseer.

This skill owns **mission elicitation and prompt compilation only**. CALLUS/the overseer owns live mission intake, decomposition, dependency planning, agent routing, dispatch, replanning, recovery, QA and completion after the prompt is sent.

## 1. Recover known context before asking

Use already-available conversation context and authorised connected/project sources when they can answer a question reliably. Do not make the user repeat known facts.

Load `references/intake-checklist.md` when the mission is materially underspecified or the user asks to be grilled in depth.

## 2. Interview only where decisions matter

For each unresolved material decision:

1. state what the decision controls;
2. give a recommended answer when a sensible default exists;
3. ask one clear question;
4. record the answer in a compact decision ledger;
5. challenge contradictions immediately.

Ask one question at a time when the user requests a full interview. Do not ask about details CALLUS can safely determine later from evidence or the StarNet planning/router layers.

Stop interviewing when every unresolved item is either:
- answered;
- explicitly delegated to CALLUS;
- safely left as an evidence-discovery task; or
- identified as a genuine human-authority gate.

## 3. Preserve the StarNet boundary

Do not pre-plan the full dependency DAG, assign every agent, or implement the mission.

The final prompt should tell CALLUS to use the existing StarNet planning/routing stack to determine the smallest safe plan and crew. Only hard-code an agent, tool, model, repo, environment or lane when the user explicitly requires it or an existing authority contract requires it.

Use the existing meanings:
- CALLUS: cross-lane orchestration and synthesis;
- SOL/TERRA/RESEARCH/QA/OPS: selected by the live router;
- OPUS or other auxiliaries: only when explicitly requested or permitted by governing policy.

Never enlarge mutation, publication, deployment, email, spending, credential or external-action authority.

## 4. Compile the launch prompt

Load `references/callus-prompt-contract.md`.

The final prompt must be self-contained enough that CALLUS can begin without another discovery interview, while still pointing to authoritative sources instead of copying huge context dumps.

It must preserve:
- exact desired outcome;
- starting state and known facts;
- scope and explicit non-scope;
- source-of-truth/evidence pointers;
- protected behavior and no-touch boundaries;
- authority granted and authority withheld;
- quality/acceptance requirements;
- constraints on tools, providers, environments, cost or tokens;
- requested reviewers/auxiliaries;
- autonomy, recovery and blocker policy;
- required artifacts/evidence;
- final Definition of Done and stop condition.

## 5. Quality check before delivery

Before returning the prompt, verify:

- no contradiction remains unresolved without being labelled;
- no material user constraint was dropped;
- no invented permission was added;
- no stale implementation detail is presented as current fact;
- CALLUS is free to choose the smallest safe decomposition;
- the prompt distinguishes evidence discovery from human-only decisions;
- the prompt says what completion means, not merely what work to attempt;
- context is bounded and references are preferred over pasted bulk;
- repeated-failure/stale-agent recovery expectations are included when relevant.

If a required human decision remains, ask it rather than fabricating an answer.

## Output

When the interview is complete, return:

1. **Decision ledger** — only the decisions that materially shape the mission.
2. **CALLUS launch prompt** — a directly copyable prompt, with no commentary inside it that is not intended for the overseer.
3. **Open assumptions** — only if any remain intentionally delegated or evidence-dependent.

If the user asks for “just the prompt”, output only the CALLUS launch prompt.
