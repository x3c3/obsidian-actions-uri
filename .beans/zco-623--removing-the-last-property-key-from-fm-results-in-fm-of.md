---
# zco-623
title: "Removing the last property key from FM results in FM of `{}`"
status: completed
type: bug
parent: auri-14wv
tags:
  - from-linear
created_at: 2024-07-16T14:49:58.051Z
updated_at: 2024-07-23T15:13:06.505Z
---

## Linear Metadata

- **Linear**: [ZCO-623](https://linear.app/actionsdotwork/issue/ZCO-623)
- **Project**: Actions URI
- **Milestone**: 1.6.0
- **Branch**: \`feature/zco-623-removing-the-last-property-key-from-fm-results-in-fm-of\`

---

Instead of a blank FM block (or no FM block), there's an empty JSON object now.

---

## Linked Commits
- [`9fedd5f`](https://github.com/czottmann/obsidian-actions-uri/commit/9fedd5f43e954f44e63dd864ecf339f5964fd4a4) — [FIX] Sanitizes YAML FM generation to avoid faulty FM
