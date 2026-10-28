# qtgame-war 分区：游戏设计档案

> `qtgame-war/` 收这款游戏蒸馏出的稳定设计决策：核心机制、架构约束、分层结构。与代码仓分工——这里存「为什么这么设计、哪些是不能破的约束」，实现细节与版本执行计划留在代码仓 `assets/qtgame-war/`（`src/studio/doc/` 模块规格、`src/studio/ROADMAP.md` 版本计划），互链不复制。

## 收录范围

收跨版本稳定的设计共识，即被两个以上版本引用、不随单次迭代变化的决策。单版本的实现方案、待办与验收不进这里。

## 设计档案

| 主题 | 档 |
|:--|:--|
| 核心机制：玩家是指挥官，不是棋手 | [`core-mechanism.md`](core-mechanism.md) |
| 架构约束：通用核心加剧本注入、红蓝语义、模型签名 | [`constraints.md`](constraints.md) |
| 分层结构：指挥官层、执行核心、剧本层 | [`layering.md`](layering.md) |

## 边界

- 这里存设计决策与约束（为什么、不能破什么），代码仓存实现（怎么构建、做到哪）。
- 核心 / 剧本边界清单在 [`constraints.md`](constraints.md)，剥离或新增代码时以此为准。
