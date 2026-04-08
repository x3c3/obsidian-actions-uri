---
# zco-429
title: "Revamp the returning of errors to pick from a fixed list of possible errors"
status: completed
type: task
parent: auri-ujej
tags:
  - from-linear
created_at: 2024-02-20T14:20:38.107Z
updated_at: 2025-05-22T11:40:10.356Z
---

## Linear Metadata

- **Linear**: [ZCO-429](https://linear.app/actionsdotwork/issue/ZCO-429)
- **Project**: Actions URI
- **Milestone**: 1.8.1
- **Branch**: \`feature/zco-429-revamp-the-returning-of-errors-to-pick-from-a-fixed-list-of\`

---

Introduce a fixed list of error states so it's easier for AFO to interact with returned Actions URI errors. Changing all numeric error codes on failure will be a **breaking** **change.**

```ts
enum Failure {
  fileNotFound,
  noteNotFound,
}
type FailureDetails = { errorCode: number; errorMessage: string };

const failureDetails: { [key in Failure]: FailureDetails } = {
  [Failure.fileNotFound]: { errorCode: 1, errorMessage: "File not found" },
  [Failure.noteNotFound]: { errorCode: 3, errorMessage: "Note not found" },
};

function failure(f: Failure): ErrorObject {
  return { isSuccess: false, ...failureDetails[f] };
}

// Later
return failure(Failure.fileNotFound)
```

Prep work for [ZCO-419](https://linear.app/actionsdotwork/issue/ZCO-419/return-nicer-error-messages-than-the-raw-actions-uri-errors) – having a 

---

## Linked Commits
- [`38fcafa`](https://github.com/czottmann/obsidian-actions-uri/commit/38fcafa4f6f0b4a3b039a9fd31b750ebd386ffc8) — [CHG] Renames `ErrorCode` enum cases to lowercase
