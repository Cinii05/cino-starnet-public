---
name: "cino-repo-navigator"
description: "Read-only narrow codebase navigation when the implementation location or direct dependency surface is unclear; skip when the exact target file/function is already supplied."
category: "Cino StarNet"
state: "active"
created_by: "agent02b-candidate"
pinned: false
---

# cino-repo-navigator

Search for the symbol/route/model/API/test/distinctive string, form a small candidate set, then read only the definition, direct callers/contracts/config and nearby tests needed to answer the question. Prefer active source over generated/archive/vendor output. Follow direct edges only. Return active files, each responsibility, direct dependency edges and remaining unknowns. Do not edit or select/execute a verification suite here.
