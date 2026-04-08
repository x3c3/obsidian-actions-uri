---
# zco-976
title: "Fix wonky frontmatter parser"
status: completed
type: bug
parent: auri-48pt
tags:
  - from-linear
  - help-scout
created_at: 2025-01-29T18:03:47.109Z
updated_at: 2025-01-30T11:23:44.042Z
---

## Linear Metadata

- **Linear**: [ZCO-976](https://linear.app/actionsdotwork/issue/ZCO-976)
- **Project**: Actions URI
- **Milestone**: 1.7.0
- **Branch**: \`feature/zco-976-fix-wonky-frontmatter-parser\`

---

When the frontmatter block contains any string like `"---"`, the parser fails because it assumes this string is the end boundary of the FM.

See [https://secure.helpscout.net/conversation/2833345523/672?viewId=7423770](https://secure.helpscout.net/conversation/2833345523/672?viewId=7423770)

---

## Linked Commits
- [`3f7de7c`](https://github.com/czottmann/obsidian-actions-uri/commit/3f7de7cc567f0dd70de9b66f9e41d36a5510c780) — [CHG] Fixes triple hyphens in frontmatter strings breaking FM parsing
