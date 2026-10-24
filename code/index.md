# code 分区：AI 协作需求档案

> `code/` 收**与 AI 协作时出现的需求差**：回答「我以为 AI 知道什么、它实际做了什么、下次该用什么话把它拉回来」。与 `think/`（认知：怎么想）、`work/`（台账：做了什么决定）分工——这里只收协作层面的需求与对应话术，不记业务事实、不记情绪。

## 口径

`requirement/` 是这类差的**持久存储**，来源是 `qtfounder-lab` 的本地账本（`clarify.json` 与 `rules.md`）：账本只是缓存，逐条记录、随归档清空，档案才是留下的一份。记录整理进档案后，本地缓存即可删除。

一主题一档，按出现次数分三档，取已到的最高档：

1. **观察**：只出现过 1 次，先记形态，不急着下判断；
2. **类型**：同一类差出现 ≥2 次，说清「原以为 X，实际 Y」并配上一句该用的提示词；
3. **规则**：用户点头落进 `rules.md` 的那句原话，档里只引用不重写。

档案保留 `clr_` id 与原始措辞的摘要；缓存删除后，id 只在这份档案里有意义，用于回溯归档批次。

## 主题档一览

| 主题 | 状态 | 档 |
|:--|:--|:--|
| 澄清的形态 | 观察 | [`requirement/clarification-shape.md`](requirement/clarification-shape.md) |
| 默认值的取舍 | 观察 | [`requirement/default-values.md`](requirement/default-values.md) |
| 归档的收法 | 观察 | [`requirement/archival-scope.md`](requirement/archival-scope.md) |
| 规格与案例的取舍 | 观察 | [`requirement/spec-and-case-scope.md`](requirement/spec-and-case-scope.md) |

## 边界

- 主题来自「实际做了什么」这一列，不按日期、不按命令切档。
- 每条记录都要进档案，单次出现进「观察」，不留缓存。
- 不生成规则文本；`rules.md` 只读。
- 归档与缓存清理的步骤见创始人仓的 `code-requirement` Skill。
