---
# zco-1496
title: "Research user report about `/note/get`diverging wrongly when fetching current and most recent PN"
status: todo
type: bug
parent: auri-b61p
tags:
  - from-linear
  - forum
created_at: 2025-09-24T09:15:03.636Z
updated_at: 2025-10-07T15:34:11.035Z
---

## Linear Metadata

- **Linear**: [ZCO-1496](https://linear.app/actionsdotwork/issue/ZCO-1496)
- **Project**: Actions URI
- **Milestone**: 1.9.0
- **Branch**: \`feature/zco-1496-research-user-report-about-notegetdiverging-wrongly-when\`

---

Customer has issues with correctly (?) configured weekly PN – sounds like \[`/note/get`\]([https://zottmann.dev/obsidian-actions-uri/routes/note/#noteget](https://zottmann.dev/obsidian-actions-uri/routes/note/#noteget)) is returning different results:

The "most recent" is fetched by calling `getAllWeeklyNotes()` in Liam's plugin, then [returning the most recent one from that list](https://github.com/czottmann/obsidian-actions-uri/blob/release/1.8.x/src/utils/periodic-notes-handling.ts#L94-L102). The "current", too, is calling `getAllWeeklyNotes()` but additionally specifying a timestamp for which a note should be returned ([Actions URI is passing the current time, there](https://github.com/czottmann/obsidian-actions-uri/blob/release/1.8.x/src/utils/periodic-notes-handling.ts#L112-L113)). So both are querying the same data source (good) but one is returning faulty results (bad).

I don't see anything in the **obsidian-daily-notes-interface** plugin that'd cause such a discrepancy, tho: 

[obsidian-daily-notes-interface/src/weekly.ts at main · liamcain/obsidian-daily-notes-interface](https://github.com/liamcain/obsidian-daily-notes-interface/blob/main/src/weekly.ts#L87-L92)

---

## Progress

### 2025-10-07 (Carlo Zottmann)

> The syntax `MM-DD` works differently in the Periodic Notes plugin and the aforementioned package that Actions URI is using to resolve the periodic notes. In the Periodic Note plugin, it means *“first day of the week (Sunday or Monday, depending on your settings)”*.
> 
> In the the [**liamcain/obsidian-daily-notes-interface** npm package](https://github.com/liamcain/obsidian-daily-notes-interface) (again: same author as Periodic Notes itself!) the format is parsed [in the “correct” way, i.e. the same way it works anywhere in Obsidian and everywhere else](https://momentjs.com/docs/#/displaying/format/): `DD` is the current day of the month.
> 
> That means the “current weekly note” request in AFO worked well for me yesterday (a Monday, i.e. start of the week), and both Periodic Notes and the developer-focussed obsidian-daily-notes-interface resolved `YYYY/MM/gggg-[W]ww (MM-DD)` to `2025/10/2025-W41 (10-06).md`. But today it’s broken again, since Periodic Notes still returns the same computed path as yesterday while obsidian-daily-notes-interface resolves it to `2025/10/2025-W41 (10-07).md`.
> 
> Might need to fork and fix [liamcain/obsidian-daily-notes-interface: Package to create, open, and find daily notes from your Obsidian plugin](https://github.com/liamcain/obsidian-daily-notes-interface). 🫤
