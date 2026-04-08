---
# zco-120
title: "Research Obsidian Sync behaviour re plugins and startup priority"
status: todo
type: task
tags:
  - from-linear
  - research
created_at: 2023-09-17T13:45:40.298Z
updated_at: 2025-05-19T10:41:29.198Z
---

## Linear Metadata

- **Linear**: [ZCO-120](https://linear.app/actionsdotwork/issue/ZCO-120)
- **Project**: Actions URI
- **Branch**: \`feature/zco-120-research-obsidian-sync-behaviour-re-plugins-and-startup\`

---

[https://discord.com/channels/686053708261228577/840286264964022302/1073620746888298577](https://discord.com/channels/686053708261228577/840286264964022302/1073620746888298577) ff.

Licat:

* Obsidian Sync doesn't run before other plugins
* `app.internalPlugins.getPluginById('sync').instance.getStatus()` gets you the following: `'synced' | 'syncing' | 'error' | 'paused'` (make sure that `getPluginById()` doesn't return you `null`)
* "Probably consider it working only when that gives you `'syncing' | 'error'`"
