---
name: "cino-context-funnel"
description: "Use when a task depends on multiple uncertain evidence classes and the minimum proving set is not yet clear; do not use for a supplied exact file, known symbol, or already-explicit narrow authority conflict."
category: "Cino StarNet"
state: "active"
created_by: "agent02b-candidate"
pinned: false
---

# cino-context-funnel

1. State the exact claim/decision.
2. List candidate evidence classes, not files.
3. Choose the smallest evidence set that can prove the claim and define the stop condition before retrieval.
4. Reuse fresh verified evidence when identity/version is unchanged.
5. Retrieve narrowly; never recursively ingest a repo/vault/archive/transcript by default.
6. Preserve source identity, timestamp/freshness, environment and immutable IDs.
7. If narrowed sources conflict, invoke cino-source-of-truth.
8. Stop when the claim is supportable or the precise missing evidence is identified.

Read-only. Never enlarges authority and never outranks a stricter specialist/project procedure.
