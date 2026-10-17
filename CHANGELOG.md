# CHANGELOG

## [Unreleased]

### Removed

- `think/`（情境视图）与 `work/`（事件视图）：一并按**事情**重组进新 `think/` 后清理，条目原文基线 `git show fe651c1:think/…`、`git show fe651c1:work/…`
- `matters/`：当天实验的事情卡视图，转正为 `think/` 各事情组（未发布即并入）
- `default/`：按情境重组进 `think/` 后清理，原文基线 `git show f4013d1:default/…`（条目原文已在 `think/` 各组）
- `work/` 五轴档案（`triggers.md` / `emotions.md` / `methods.md` / `values.md` / `expressions.md`）：按事件重组后清理，原文基线 `git show 86e8532:work/…`
- `media/`：`肆季味.md` 迁回 `data/context/media/profile/`（媒体素材的对象档案与素材同住）

### Added

- `think/`：按**事情**重组（合并原情境视图与事件视图）——9 组（第二大脑与档案体系 / 与 AI 协作 / 带人与标准化 / 平台与生态 / 产教融合与需求众包 / 写作与创作 / 合规与平台设计 / 注意力与范围 / 状态与恢复），每组 `md`（事情卡 + 条目原文）+ `lino` + `ttl` 三格式，本体、事情节点与跨组边集中在 `index.*`；事情卡记蒸馏程度（想法 → 情境 → 方法 → 价值），只在日志、未入档案的事情也立组（产教融合与需求众包）；守恒核对 62 节点（40 + 22）、39 条边（组内 38 + 跨组 1）全对（基线 fe651c1）
- `write/index.md`、`write/index.ttl`：创作认知地图，自 `data/context/write/profile/` 迁入

### Changed

- 档案分区不再与 `data/context` 一一对应：profile 收敛为 `think/`（事情）与 `write/`（创作）两视图

## [0.0.1] - 2026-10-17

初始版本。`data/context` 各分区的 `profile/` 迁入本仓，落为同名文件夹：`default/`、`work/`、`write/`、`media/`。
