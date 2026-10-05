---
name: "cino-source-of-truth"
description: "Use when explicit sources conflict or the governing authority for a consequential claim must be resolved. If breadth is uncertain first use cino-context-funnel; if the conflict is already narrow start here."
category: "Cino StarNet"
state: "active"
created_by: "agent02b-candidate"
pinned: false
---

# cino-source-of-truth

1. State the exact claim and classify it: code, deployed runtime, tests, commercial/product policy, legal/compliance, release authority, or history.
2. Match the claim to evidence that can actually prove it. Code identity does not prove deployment; runtime behavior does not invent business policy; historical summaries do not outrank current governing authority.
3. Verify the source was actually readable and record exact version/SHA/environment/timestamp where material.
4. Compare currentness and scope. Never silently choose the convenient side of a conflict.
5. Return GOVERNING AUTHORITY FOUND, CONFLICT, or UNKNOWN / EVIDENCE MISSING, with the precise source and remaining gap.

Read-only unless an outer workflow separately grants mutation authority.
