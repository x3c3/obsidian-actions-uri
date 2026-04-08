---
# zco-1348
title: "Check reports of `/note-properties/set` overwriting existing keys"
status: completed
type: bug
parent: auri-qz7a
tags:
  - from-linear
created_at: 2025-08-04T08:10:05.209Z
updated_at: 2025-08-05T10:00:12.450Z
---

## Linear Metadata

- **Linear**: [ZCO-1348](https://linear.app/actionsdotwork/issue/ZCO-1348)
- **Project**: Actions URI
- **Milestone**: 1.8.3
- **Branch**: \`feature/zco-1348-check-reports-of-note-propertiesset-overwriting-existing\`

---

[https://phanpy.social/#/norden.social/s/114964623532850832?view=full](https://phanpy.social/#/norden.social/s/114964623532850832?view=full)  > Moin, ich glaube, ich bin ggf. über einen Bug in AFO gestolpert. Obwohl bei der Aktion "Set properties" "add new keys, update existing" ausgewählt ist, löscht er bestehende, andere properties. > > ![image.png](assets/zco-1348-image.png) > > Vorher: > > ![image.png](assets/zco-1348-image.png) > > Nachher:  > > ![image.png](assets/zco-1348-image.png) > > Frontmatter: > > ``` > --- > tags: >   - journal/daily > datum: 2025-08-04  > arbeitstag: true > weekly: "[[2025-W32]]" > monthly: "[[2025-08-M]]" > yearly: "[[2025-Y]]" > titel: "%%titel%%" > mood: "%%laune%%" > ort: >   - Gießen > --- > ```

---

## Linked Commits
- [`dfe5c80`](https://github.com/czottmann/obsidian-actions-uri/commit/dfe5c805b0d6d7fd56a58c72e312718c3eda636b) — [FIX] Update FM using Obs' own `processFrontMatter()` now

---

## Progress

### 2025-08-05 (Carlo Zottmann)

> I've replaced my own naïve implementation with Obsidian's own `processFrontMatter()` ([processFrontMatter - Developer Documentation](https://docs.obsidian.md/Reference/TypeScript+API/FileManager/processFrontMatter)).
