---
# zco-166
title: "Set up a testing framework"
status: completed
type: task
priority: normal
parent: auri-ujej
tags:
  - from-linear
created_at: 2023-09-18T17:24:26.604Z
updated_at: 2025-05-22T11:40:10.366Z
---

## Linear Metadata

- **Linear**: [ZCO-166](https://linear.app/actionsdotwork/issue/ZCO-166)
- **Project**: Actions URI
- **Milestone**: 1.8.1
- **Branch**: \`feature/zco-166-set-up-a-testing-framework\`

---

## Linked Commits
- [`41cfdec`](https://github.com/czottmann/obsidian-actions-uri/commit/41cfdecfebf03bc9919a1f8d56c29e486fcab1b6) — Merge pull request #100 from czottmann/feature/zco-166-jest

---

## Progress

### 2025-05-15 (Carlo Zottmann)

> Working with Cline & [Gemini 2.5 Flash Preview](https://openrouter.ai/google/gemini-2.5-flash-preview), I was able to cobble together an E2E testing setup which contains a pre-configured "blueprint" vault folder, which is copied to the right folder prior to Jest starting, then opens it in Obsidian, and sends out XCU calls. So far, so good, but the callbacks are opened by `window.open()` (in Obsidian) which hands them over to the OS which passes them on … to the browser.
> 
> Need to figure out a way to set up a URL scheme for the test script.

### 2025-05-15 (Carlo Zottmann)

> Started, thought about it for a few hours, stopped again. I don't know where to start. I'd love to test the routes which are the most important thing but they use so much Obsidian code which would need to be mocked … oof.
> 
> What about E2E calls? That'd require an actual test vault, and a HTTP server as a receiver, so Jest could make XCU calls to that vault and listen for the return values…?
