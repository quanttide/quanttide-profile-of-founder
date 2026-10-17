# CHANGELOG

## [Unreleased]

### Removed

- `default/`：按情境重组进 `think/` 后清理，原文基线 `git show f4013d1:default/…`（条目原文已在 `think/*.md`）
- `work/`：五轴档案（`triggers.md` / `emotions.md` / `methods.md` / `values.md` / `expressions.md`）按事件重组进同目录各组后清理，原文基线 `git show 86e8532:work/…`
- `media/`：`肆季味.md` 迁回 `data/context/media/profile/`（媒体素材的对象档案与素材同住）

### Added

- `think/`：按**情境（触发点）**重组 `default/` 档案（原名 `meta/`，2026-10-17 改名）——8 组（睡醒时的千头万绪 / 战略失败 / 进度停滞 / AI 变成纯粹执行者 / 范围失控 / 不确定是否合规 / 自己不想看自己写的内容 / 不系于情境的条目），每组 `md` + `lino` + `ttl` 三格式，`index.*` 概括框架；守恒核对 40 节点、24 条目、26 条边全对（跨组边 4）
- `write/index.md`、`write/index.ttl`：创作认知地图，自 `data/context/write/profile/` 迁入
- `work/`：按**事件**重组——11 组（目标完成又冒出新需求 / 供需双方都卡住 / 文件成了垃圾堆 / AI 用得不顺手 / 大转型期 / 想法不断冒出 / 想法说不出来 / 面对高频易再生的素材 / 需要快速验证一个想法 / 维护场景要同时保质量与产出 / 不系于事件的条目），每组 `md` + `lino` + `ttl` 三格式，`index.*` 概括框架；21 节点、11 条态射 + 1 条 seeAlso（跨组边 1）

## [0.0.1] - 2026-10-17

初始版本。`data/context` 各分区的 `profile/` 迁入本仓，落为同名文件夹：`default/`、`work/`、`write/`、`media/`。
