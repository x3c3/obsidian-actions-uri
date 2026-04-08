---
# zco-634
title: "Fix headline block append/prepend"
status: completed
type: bug
parent: auri-slfp
tags:
  - from-linear
created_at: 2024-07-26T09:25:11.951Z
updated_at: 2024-07-29T15:51:13.445Z
---

## Linear Metadata

- **Linear**: [ZCO-634](https://linear.app/actionsdotwork/issue/ZCO-634)
- **Project**: Actions URI
- **Milestone**: 1.6.2
- **Branch**: \`feature/zco-634-fix-headline-block-appendprepend\`

---

Request:

[Marco :prami: (@esamecar@social.lol)](https://social.lol/@esamecar/112851925966484997)

Both `prependNoteBelowHeadline()` and `appendNoteBelowHeadline()` use a sloppy "does this section start with this headline" check:

```
const newContent = res.result
    .split(/(?=^#+ )/m)
    .map((section) => {
      if (!section.startsWith(belowHeadline)) {
        return section;
      }
```

If `belowHeadline` is "## A", then this would check `true` if the section starts with "## ABC", too. Also, if `belowHeadline` ending in whitespace might fail the check.

Make the check use a regex: `/^## Mittwoch\s*\n/.test(section)`

---

## Linked Commits
- [`d9eac50`](https://github.com/czottmann/obsidian-actions-uri/commit/d9eac50736ec1f13ab0084aaaddea413bc9512e5) — [FIX] Fixes sloppy "below headline" matching and appending/prepending
