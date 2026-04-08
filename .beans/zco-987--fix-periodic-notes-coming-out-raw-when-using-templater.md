---
# zco-987
title: "Fix periodic notes coming out \"raw\" when using Templater"
status: completed
type: bug
parent: auri-plwy
tags:
  - from-linear
created_at: 2025-02-10T09:17:45.017Z
updated_at: 2025-02-10T09:38:26.270Z
---

## Linear Metadata

- **Linear**: [ZCO-987](https://linear.app/actionsdotwork/issue/ZCO-987)
- **Project**: Actions URI
- **Milestone**: 1.7.2
- **Branch**: \`feature/zco-987-fix-periodic-notes-coming-out-raw-when-using-templater\`

---

Reports:

* [https://secure.helpscout.net/conversation/2834156734/673?viewId=7423770](https://secure.helpscout.net/conversation/2834156734/673?viewId=7423770)
* [Creating Periodic Note doesn't apply Templater templates - Actions For Obsidian - ActionsDotWork Forum](https://forum.actions.work/t/creating-periodic-note-doesnt-apply-templater-templates/590/2)

Race condition just like the one with general notes. Need to apply a pause after creation here, too.
