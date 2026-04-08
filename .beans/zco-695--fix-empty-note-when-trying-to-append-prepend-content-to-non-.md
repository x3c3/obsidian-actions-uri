---
# zco-695
title: "Fix empty note when trying to append/prepend content to non-existing periodic note which has to be created first"
status: completed
type: bug
tags:
  - from-linear
  - help-scout
created_at: 2024-09-23T09:23:29.780Z
updated_at: 2024-10-09T11:11:32.296Z
---

## Linear Metadata

- **Linear**: [ZCO-695](https://linear.app/actionsdotwork/issue/ZCO-695)
- **Project**: Actions URI
- **Branch**: \`feature/zco-695-fix-empty-note-when-trying-to-appendprepend-content-to-non\`

---

Via [Help Scout #589](https://secure.helpscout.net/conversation/2711901364/589):

> `obsidian://actions-uri/note/append/?vault=Full%20Life&create-if-not-found=true&periodic-note=daily&content=hello`
>
> This action does correctly create the daily note, if it doesn’t exist. It also correctly appends the content to the note.
>
> However, it does not apply the daily note template when creating the daily note. The result of this URI is that the daily note is created, but only contains the word “hello”.
>
> This means I can’t use the below headline option, because the headline is in the template, and the template doesn’t get applied. My shortcut has to contain a separate create daily note action, which does apply the template when creating the note.

💭  I think due to some internal changes in Obsidian itself the periodic note plugin(s) and Actions URI are now interfering with each other.

---

## Linked Commits
- [`f615958`](https://github.com/czottmann/obsidian-actions-uri/commit/f61595878dc547cc1f6ae39b6d335da7f7dd4b17) — [CHG] Updates note open/focus by path for Obsidian 1.7
- [`901b26b`](https://github.com/czottmann/obsidian-actions-uri/commit/901b26bbf18e5aaff596fca3d519c731b14233e4) — [NEW] Adds ZCO-695 to changelog
- [`c14ca8c`](https://github.com/czottmann/obsidian-actions-uri/commit/c14ca8c24282658188d195ac621769d8b7fcc7ea) — [FIX] Ensures append/prepend on periodic notes creates the right type of note if requested
