---
# zco-918
title: "Make Dataview LIST result consistent"
status: completed
type: bug
parent: zco-919
tags:
  - from-linear
created_at: 2024-11-25T14:26:48.381Z
updated_at: 2025-02-04T11:58:55.693Z
---

## Linear Metadata

- **Linear**: [ZCO-918](https://linear.app/actionsdotwork/issue/ZCO-918)
- **Project**: Actions URI
- **Milestone**: 1.7.0
- **Branch**: \`feature/zco-918-make-dataview-list-result-consistent\`

---

[Get DV list without ID + inline → Json string couldn't be decoded](https://forum.actions.work/t/get-dv-list-without-id-inline-json-string-couldnt-be-decoded/554/4)

For LIST queries, DV will return a two-dimensional array instead of a one-dimensional one *if* one of the queried files returns more than one hit.

Example: If you query for an inline field (`whatever::`), and one file contains of it, e.g. `whatever:: something 1` and `whatever:: something 2`, while another file contains `whatever:: something 3`, DV will return:

```
[
  ["something 1", "something 2"],
  "something 3"
]
```

This is inconsistent, and AFO will nope out. So we'll make it consistent.

---

## Linked Commits
- [`6a3d653`](https://github.com/czottmann/obsidian-actions-uri/commit/6a3d6535b9e7cc7386d4f8013d091346f7d0df6e) — [CHG] Rewrote inline docs
- [`7f25a90`](https://github.com/czottmann/obsidian-actions-uri/commit/7f25a902988cc1674d4435d7c3b855c58f9dcbe2) — [FIX] Fixes inconsistencies in `LIST` query results
