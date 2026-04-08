---
# zco-588
title: "Fix API calls not reaching Actions URI when vault needs to open first"
status: completed
type: bug
parent: auri-2nvq
tags:
  - from-linear
created_at: 2024-06-14T08:32:34.590Z
updated_at: 2024-06-18T14:43:12.669Z
---

## Linear Metadata

- **Linear**: [ZCO-588](https://linear.app/actionsdotwork/issue/ZCO-588)
- **Project**: Actions URI
- **Milestone**: 1.5.3
- **Branch**: \`feature/zco-588-fix-api-calls-not-reaching-actions-uri-when-vault-needs-to\`

---

When launching Obsidian, or switching to a closed, the API call will open the vault but the call itself won't be handled. Weirdly, this works fine for Omnisearch (e.g. [obsidian://omnisearch?query=foo&vault=Workbench](obsidian://omnisearch?query=foo&vault=Workbench)) and other plugins, but not for Actions URI.

Find the problem and fix it.

---

## Linked Commits
- [`161caf2`](https://github.com/czottmann/obsidian-actions-uri/commit/161caf241d5c062a041332e2b37b4219701d29fc) — [REL] Release 1.5.3 · czottmann/obsidian-actions-uri@161caf2
