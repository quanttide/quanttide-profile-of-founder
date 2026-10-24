# CHANGELOG

## [Unreleased]

### Changed

- `code/intent/` → `code/requirement/`：明确为**持久存储**——本地账本是缓存，整理进档案后可清空；口径改为「每条记录都进档案，单次出现进观察档」，不再把单次差留在账本；归档与清理步骤收在创始人仓的 `code-requirement` Skill

### Removed

- `think/*.lino`、`think/*.ttl`、`think/README.md`、`.agents/skills/think-audit`：图谱层停用，认知归档只保留 Markdown 事情卡与 `index.md` 组列表
- `think/ai-collaboration.*`（md / lino / ttl / html）：认知内容已整理为手册《人机协作》，本组从 think 移出；`index.*` 同步删除该事情节点与注释，守恒基线随之前移
- `think/`（情境视图）与 `work/`（事件视图）：一并按**事情**重组进新 `think/` 后清理，条目原文基线 `git show fe651c1:think/…`、`git show fe651c1:work/…`
- `matters/`：当天实验的事情卡视图，转正为 `think/` 各事情组（未发布即并入）
- `default/`：按情境重组进 `think/` 后清理，原文基线 `git show f4013d1:default/…`（条目原文已在 `think/` 各组）
- `work/` 五轴档案（`triggers.md` / `emotions.md` / `methods.md` / `values.md` / `expressions.md`）：按事件重组后清理，原文基线 `git show 86e8532:work/…`
- `media/`：`肆季味.md` 迁回 `data/context/media/profile/`（媒体素材的对象档案与素材同住）

### Added

- `execute/`：新增分区「任务清单」——只列可执行的任务与状态，任务背后的决定与依据仍留在 `work/`；首批两笔（创建 `quanttide-wechat`、`quanttide-create` 第二大脑），自 `data/context/work/TODO.md` 迁入
- `code/`：新增分区「AI 协作档案」——收与 AI 协作中反复出现的差，一主题一档；口径按出现次数分观察（1 次）/ 类型（≥2 次）/ 规则（已落 `rules.md`），原始条目以 `clr_` id 指回澄清账本不复制原文。首批两档：`code/intent/clarification-shape.md`（澄清的形态）、`code/intent/default-values.md`（默认值的取舍），均处「观察」档，来源 `int_1Z8G` 的 `clr_NHCX`、`clr_M58A`
- `think/`：按**事情**重组（合并原情境视图与事件视图）——8 组（第二大脑与档案体系 / 带人与标准化 / 平台与生态 / 产教融合与需求众包 / 写作与创作 / 合规与平台设计 / 注意力与范围 / 状态与恢复），每组 `md`（事情卡 + 条目原文）；事情卡记蒸馏程度（想法 → 情境 → 方法 → 价值），只在日志、未入档案的事情也立组（产教融合与需求众包）。
- `work/`：重建为**事项台账**——推动中事项的对象档案（现状 / 依据 / 下一步，一事项一 `md`，不配图谱），与 `think/` 分工（认知归 think、事实与决定归 work，`think/` 各卡「未决」的事实性行动项移入并留指针）；首批 4 档（founder-toolkit 重做 / 第二大脑专用化 / 产教融合与众包 / 写作分区与博客），蒸馏自日志 2026-10-17
- `write/index.md`、`write/index.ttl`：创作认知地图，自 `data/context/write/profile/` 迁入
- `media/`：肆季味探店文案与 9 张配图（`images/sijiwei_1.jpg`～`sijiwei_9.jpg`）

### Changed

- 档案分区不再与 `data/context` 一一对应：`think/` 收认知档案（合并自原情境 / 事件视图），`work/` 转为事项台账、`write/` 收创作档案
- `media/sijiwei.md`：重写为最终发布版（标题、正文、标签、图片顺序）
- `media/sijiwei.md`：补充发布平台与标签数量限制

## [0.0.1] - 2026-10-17

初始版本。`data/context` 各分区的 `profile/` 迁入本仓，落为同名文件夹：`default/`、`work/`、`write/`、`media/`。
