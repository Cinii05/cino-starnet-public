---
name: "cino-skill-governor-approval-model"
description: "Internal StarNet reference used only after cino-skill-governor reaches install/update/promotion/rollback/retirement; never activate directly from a normal task."
category: "Cino StarNet"
state: "active"
created_by: "agent02b-candidate"
pinned: false
---

# cino-skill-governor-approval-model

Keep lifecycle state separate from the requested change. Global install, update or promotion requires Human Authority. Reviewer recommendation is evidence, never approval. Missing candidate bytes/version/digest/provenance stay explicitly unavailable. Pending/rejected/cancelled actions leave the active installed state unchanged. A separately authorised local isolated trial is evidence for a later decision, not promotion.
