---
# zco-1156
title: "Change appending below headline to redefine \"headline section\" as, say, H2 to next H2"
status: in-progress
type: task
parent: auri-b61p
tags:
  - from-linear
created_at: 2025-04-17T14:34:01.592Z
updated_at: 2025-05-19T16:45:38.570Z
---

## Linear Metadata

- **Linear**: [ZCO-1156](https://linear.app/actionsdotwork/issue/ZCO-1156)
- **Project**: Actions URI
- **Milestone**: 1.9.0
- **Branch**: \`feature/zco-1156-change-appending-below-headline-to-redefine-headline-section\`

---

Currently, appending below a headline assumes a "headline section" goes from the start of that headline right up to the beginning of the next headline – **any** headline. So if you have a H3 which is immediately followed by a H4, the H3 "section" goes from the beginning of the H3 right up to the following H4. There is no semantic analysis like *"H4 follows H3 therefore it's part of the H3 section"*. I've opted for the simple rule *"from headline to next headline"* which is easily explained.

Some customers are confused because they expect a "H2 section" to go from that H2 to the next H2 (or EOF, whatever comes first), and right now it doesn't.

If you implement that, mark it as "breaking change".
