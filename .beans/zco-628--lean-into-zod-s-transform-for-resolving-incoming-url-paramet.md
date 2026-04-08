---
# zco-628
title: "Lean into Zod's `.transform()` for resolving incoming URL parameters"
status: todo
type: task
tags:
  - from-linear
created_at: 2024-07-18T15:32:44.910Z
updated_at: 2025-05-21T13:44:38.256Z
---

## Linear Metadata

- **Linear**: [ZCO-628](https://linear.app/actionsdotwork/issue/ZCO-628)
- **Project**: Actions URI
- **Branch**: \`feature/zco-628-lean-into-zods-transform-for-resolving-incoming-url\`

---

Contemplate how s/th like `validateNoteTargetingAndResolvePath()` could work for anything incoming. I have a feeling this could make a lot of code redundant. When the handler gets the original zod-treated parameters plus a `_resolved` object (containing the actual requested file path etc.), that's a win. (It's partially what I did with `zodExistingFilePath` et al, but that's overwriting the incoming data, so… hmm.)

But having single transformers which could be tacked on as needed…?

```typescript
incomingBaseParams.extend({
  file: zodExistingFilePath,
  "new-filename": zodSanitizedFilePath,
  silent: zodOptionalBoolean,
})
  .transform(hardResolveFile) // resolve file or abort with error
  .transform(resolveWhatever)
  .transform(something)
```

---

## Progress

### 2025-05-21 (Carlo Zottmann)

> New zod v4 is out, look at that first.
