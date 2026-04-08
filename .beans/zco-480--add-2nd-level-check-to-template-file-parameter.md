---
# zco-480
title: "Add 2nd-level check to `template-file` parameter"
status: completed
type: task
parent: auri-14wv
tags:
  - from-linear
created_at: 2024-03-26T11:40:28.746Z
updated_at: 2024-07-23T15:13:07.972Z
---

## Linear Metadata

- **Linear**: [ZCO-480](https://linear.app/actionsdotwork/issue/ZCO-480)
- **Project**: Actions URI
- **Milestone**: 1.6.0
- **Branch**: \`feature/zco-480-add-2nd-level-check-to-template-file-parameter\`

---

Change the Actions URI-internal handling of template parameters to prepend the template folder set in the Obsidian configuration as a fallback, as in: first check the original parameter, if not valid, prepend the template path, if still not valid, complain.

See:

* [/note/create | Actions URI](https://zottmann.dev/obsidian-actions-uri/routes/note/#notecreate)
* [Create Note apply Templater template - Template Path - Actions For Obsidian - ActionsDotWork Forum](https://forum.actions.work/t/create-note-apply-templater-template-template-path/328/2)

---

## Linked Commits
- [`4e94c35`](https://github.com/czottmann/obsidian-actions-uri/commit/4e94c35d59df587cc3190fc584d589581bf78365) — [NEW] Adds 1.6 stuff
- [`fb758ef`](https://github.com/czottmann/obsidian-actions-uri/commit/fb758eff78d503fdcd5956452cdbe7566235174b) — [NEW] Adds fallback for when `template-file` parameter contains template folder
