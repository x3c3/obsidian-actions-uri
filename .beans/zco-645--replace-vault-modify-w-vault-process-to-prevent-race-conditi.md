---
# zco-645
title: "Replace `vault.modify()` w/ `vault.process()` to prevent race conditions"
status: scrapped
type: bug
tags:
  - from-linear
created_at: 2024-08-05T13:10:03.596Z
updated_at: 2024-08-06T10:57:19.442Z
---

## Linear Metadata

- **Linear**: [ZCO-645](https://linear.app/actionsdotwork/issue/ZCO-645)
- **Project**: Actions URI
- **Branch**: \`feature/zco-645-replace-vaultmodify-w-vaultprocess-to-prevent-race\`

---

[Vault - Developer Documentation](https://docs.obsidian.md/Plugins/Vault#Modify+files)

When appending text a non-focussed note, e.g. under a headline in the weekly note, the last modification before the update seems to be rolled back before the current modification is applied. Not sure yet it's an AURI issue, though.

**UPDATE: Not an AURI issue.** The plugin "Check Please!" misbehaves.
