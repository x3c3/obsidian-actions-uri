---
# zco-1182
title: "Using `if-exists=skip` and `silent=false` in `/note/create` does not open the note in Obsidian"
status: completed
type: bug
parent: auri-7bdl
tags:
  - from-linear
created_at: 2025-04-30T10:58:31.209Z
updated_at: 2025-04-30T11:15:03.656Z
---

## Linear Metadata

- **Linear**: [ZCO-1182](https://linear.app/actionsdotwork/issue/ZCO-1182)
- **Project**: Actions URI
- **Milestone**: 1.7.3
- **Branch**: \`feature/zco-1182-using-if-existsskip-and-silentfalse-in-notecreate-does-not\`

---

Basically the issue is that if that note already exists, the plugin fails to resolve the parameter `file=abc` into the file path `abc.md`.

---

## Linked Commits
- [`2db7ad0`](https://github.com/czottmann/obsidian-actions-uri/commit/2db7ad0e1dc51a81e4d7cb21d7b853a5adf54b63) — [NEW] Adds 1.7.3
- [`0f05d58`](https://github.com/czottmann/obsidian-actions-uri/commit/0f05d584daa7e05d577b28b3cd6af30ef7d04821) — [FIX] Adds missing resolving of input file path
