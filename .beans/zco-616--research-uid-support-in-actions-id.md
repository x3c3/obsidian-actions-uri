---
# zco-616
title: "Research UID support in Actions ID"
status: completed
type: task
parent: zco-30
tags:
  - from-linear
  - research
created_at: 2024-07-09T15:41:42.567Z
updated_at: 2024-09-12T17:44:26.872Z
---

## Linear Metadata

- **Linear**: [ZCO-616](https://linear.app/actionsdotwork/issue/ZCO-616)
- **Project**: Actions URI
- **Milestone**: 1.6.0
- **Branch**: \`feature/zco-616-research-uid-support-in-actions-id\`

---

By querying the `metadataCache` I can find all cached objects which contain a particular key (e.g., "uuid"), and then use their metadata cache key to find the related file:

```typescript
const uid = Object.entries(app.metadataCache.metadataCache)
  .find(([key, cached]) => cached.frontmatter?.uuid && [cached.frontmatter.uuid].flat().includes(123))
  ?.first()
// → '002f3dfa59410f7cdd90519680cac1097d00473c7dcc4b15b1d7948e1b786e38'

const filePath = Object.entries(app.metadataCache.fileCache)
  .find(([filePath, cache]) => cache.hash === uid)
  ?.first()
```

(It's possible to have more than one UID per file, for example when files have been merged, hence the array-based check.)

---

*Idea: Lookup of* `"file" | "uid" | "periodic-note"` *via *[*zod preprocessor*](https://zod.dev/?id=preprocess)*, so that only the* `file`  *parameter remains? This way, I could remove even more complexity from the routes, i.e. only have* `/note` *which would take care of both general notes and periodic notes, and support UIDs to boot?*

---

## Progress

### 2024-07-09 (Carlo Zottmann)

> Follow-up: [ZCO-617](https://linear.app/actionsdotwork/issue/ZCO-617/implement-zod-preprocessor-to-streamline-targeting-a-note-using-file)
