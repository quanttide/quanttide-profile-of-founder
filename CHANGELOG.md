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
- `work/`：重建为**事项台账**——推动中事项的对象档案（现状 / 依据 / 下一步，一事项一 `md`，不配图谱），与 `think/` 分工（认知归 think、事实与决定归 work，`think/` 各卡「未决」的事实性行动项移入并留指针）；首批 4 档（founder-toolkit 重做 / 第二大脑专用化 / 产教融合与众包 / 写作分区与博客），蒸馏自日志 2026-10-17
- `write/index.md`、`write/index.ttl`：创作认知地图，自 `data/context/write/profile/` 迁入

### Changed

- 档案分区不再与 `data/context` 一一对应：`think/` 收认知档案（合并自原情境 / 事件两视图），`work/` 转为事项台账、`write/` 收创作档案

## [0.0.1] - 2026-10-17

初始版本。`data/context` 各分区的 `profile/` 迁入本仓，落为同名文件夹：`default/`、`work/`、`write/`、`media/`。
