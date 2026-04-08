---
# zco-617
title: "Implement zod magic to streamline targeting a note using `\"file\" | \"uid\" | \"periodic-note\"` parameters"
status: completed
type: task
parent: zco-30
tags:
  - from-linear
created_at: 2024-07-09T16:52:35.164Z
updated_at: 2024-07-23T15:13:06.553Z
---

## Linear Metadata

- **Linear**: [ZCO-617](https://linear.app/actionsdotwork/issue/ZCO-617)
- **Project**: Actions URI
- **Milestone**: 1.6.0
- **Branch**: \`feature/zco-617-implement-zod-magic-to-streamline-targeting-a-note-using\`

---

- [X] fix lookup by UID, metadataCache is unreliable after the first hit (because the file changes and its cached info is invalidated)
- [X] create on append: if targeted by UID, use UID as title
- [X] create on prepend: if targeted by UID, use UID as title
- [X] make frontmatter UID key configurable in Actions URI settings
- [X] implement new targeting in `/note-properties` routes
- [X] add explicit PN plugin check before checking file path, and throw on missing plugin or deactivated feature
- [X] ~~create: UID support?~~ Nope
- [X] create: explicitly create PN when requested instead of general note at right path
- [X] add UID to standard result parameters (if available)
- [X] update change log
- [X] update docs
- [X] check mobile compatibility

---

## Linked Commits
- [`52fd2b2`](https://github.com/czottmann/obsidian-actions-uri/commit/52fd2b2cd1783d20755ccca036d0fb756578b93a) — [NEW] Adds settings
