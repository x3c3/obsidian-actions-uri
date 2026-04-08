---
# zco-423
title: "Add feature to auto-install new version (?)"
status: todo
type: task
tags:
  - from-linear
created_at: 2024-02-17T18:25:03.473Z
updated_at: 2024-02-19T15:11:30.495Z
---

## Linear Metadata

- **Linear**: [ZCO-423](https://linear.app/actionsdotwork/issue/ZCO-423)
- **Project**: Actions URI
- **Branch**: \`feature/zco-423-add-feature-to-auto-install-new-version\`

---

```
const i = {repo: 'czottmann/obsidian-actions-uri', version: '1.4.2', manifest: app.plugins.manifests["actions-uri"]}
app.plugins.installPlugin(i.repo, i.version, i.manifest)
```

Not sure if clever or feasible, needs proper planning.
