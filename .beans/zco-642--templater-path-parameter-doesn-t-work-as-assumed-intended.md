---
# zco-642
title: "Templater path parameter doesn't work as assumed/intended"
status: completed
type: bug
parent: auri-civ4
tags:
  - from-linear
created_at: 2024-08-02T09:11:56.999Z
updated_at: 2024-08-02T12:14:56.416Z
---

## Linear Metadata

- **Linear**: [ZCO-642](https://linear.app/actionsdotwork/issue/ZCO-642)
- **Project**: Actions URI
- **Milestone**: 1.6.3
- **Branch**: \`feature/zco-642-templater-path-parameter-doesnt-work-as-assumedintended\`

---

Via [Help Scout #562](https://secure.helpscout.net/conversation/2668200764/562):

> Carlo,
> Since the Actions URI updates, I have not been able to create my Day Note with AFO. The action fails with an error that indicates the template file is not found. However, I am able to use *Create Daily Note* with no problem in Obsidian via the ribbon button (or command). It must have something to do with the recent changes.

---

Only an issue with **Create PN + Templater + template-file**!

---

## Linked Commits
- [`a2f0fa0`](https://github.com/czottmann/obsidian-actions-uri/commit/a2f0fa0f28004015af96ec36328e91cf5431ce75) — [FIX] Makes `template-file` parameter resolve correctly again
