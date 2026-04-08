---
# zco-606
title: "Search and Replace string with special character"
status: completed
type: bug
parent: zco-531
tags:
  - from-linear
  - help-scout
created_at: 2024-06-27T16:42:41.084Z
updated_at: 2024-07-23T15:13:06.430Z
---

## Linear Metadata

- **Linear**: [ZCO-606](https://linear.app/actionsdotwork/issue/ZCO-606)
- **Project**: Actions URI
- **Milestone**: 1.6.0
- **Branch**: \`feature/zco-606-search-and-replace-string-with-special-character\`

---

S&R in text mode doesn't find the search terms when they contain unescaped special regex chars (`^`, `$`, etc.). If they are escaped, text replacement works, though.

Example, note contains the text *"Today is $Tuesday"*:

* Works: search for `\$Tuesday`
* Doesn't work: search for `$Tuesday`

---

## Linked Commits
- [`227c483`](https://github.com/czottmann/obsidian-actions-uri/commit/227c483cb5a11a5cc92ce3bc3c7418056bf1e79a) — [FIX] Makes search/replace strings containing regex chars work
