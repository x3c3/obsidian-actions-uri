---
# zco-627
title: "When creating a note during `/note/append`, Templater's watch-folder-and-apply-template may cause race condition"
status: completed
type: bug
parent: auri-14wv
tags:
  - from-linear
created_at: 2024-07-18T08:33:43.987Z
updated_at: 2024-07-23T16:09:06.634Z
---

## Linear Metadata

- **Linear**: [ZCO-627](https://linear.app/actionsdotwork/issue/ZCO-627)
- **Project**: Actions URI
- **Milestone**: 1.6.0
- **Branch**: \`feature/zco-627-when-creating-a-note-during-noteappend-templaters-watch\`

---

Via [Help Scout #553](https://secure.helpscout.net/conversation/2655031968/553):

> I'm using the "Append Text to Periodic Note" action with "Create note if necessary". I'm now using the Templater plugin for my daily notes--is it possible to configure this creation to use that plugin? At present, when I create on my phone, it creates the note with the raw templater code rather than executing it.

See ticket for more details, I've done some sleuthing already.

---

## Linked Commits
- [`c059bda`](https://github.com/czottmann/obsidian-actions-uri/commit/c059bda2254c890e0aaf8a51bb82e33fcc70f000) — [CHG] Increases post-create pause for Templater/Templates

---

## Progress

### 2024-07-23 (Carlo Zottmann)

> Added more time post-creation to give Templater more time. Closing.
