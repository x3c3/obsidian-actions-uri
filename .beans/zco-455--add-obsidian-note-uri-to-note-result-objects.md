---
# zco-455
title: "Add Obsidian note URI to note result objects"
status: completed
type: task
parent: auri-ujej
tags:
  - from-linear
created_at: 2024-02-29T13:53:18.594Z
updated_at: 2025-05-22T11:40:10.841Z
---

## Linear Metadata

- **Linear**: [ZCO-455](https://linear.app/actionsdotwork/issue/ZCO-455)
- **Project**: Actions URI
- **Milestone**: 1.8.1
- **Branch**: \`feature/zco-455-add-obsidian-note-uri-to-note-result-objects\`

---

Add `result-link` to `HandlerFileSuccess`. Also, `export async function getNoteDetails(filepath:)` in `src/utils/file-handling.ts`.

- [X] implementation
- [X] adjust `/note/create` so it returns UID and both URIs
- [X] add infos about new `result-` keys to all applicable docs
- [X] add info to changelog

---

## Linked Commits
- [`1872c36`](https://github.com/czottmann/obsidian-actions-uri/commit/1872c367c362184b75b3c2d67324e3c883791d7b) — [FIX] Adds missing `await` to `propertiesForFile()` call
- [`730ee6e`](https://github.com/czottmann/obsidian-actions-uri/commit/730ee6ed3a56a18c0fa818e3b699b3452c3548c5) — [NEW] Adds info re `result-uri-*` return values in `/note/*`
- [`4ef19ea`](https://github.com/czottmann/obsidian-actions-uri/commit/4ef19eaf845d703649e7c8cd6b0b662379b816d2) — [NEW] Adds `result-uri-*` to docs
- [`3868dac`](https://github.com/czottmann/obsidian-actions-uri/commit/3868dacb8b4bf8a1a6681bd970777984fb183ca0) — [NEW] Adds note URIs to note return values
- [`f040fba`](https://github.com/czottmann/obsidian-actions-uri/commit/f040fba88ac7f2e9f9423f3d95fd1e2b3cbc33d9) — [NEW] Adds note URIs to note return values
