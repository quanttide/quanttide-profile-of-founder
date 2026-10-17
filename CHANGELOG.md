# CHANGELOG

## [Unreleased]

### Removed

- `default/`：按情境重组进 `think/` 后清理，原文基线 `git show f4013d1:default/…`（条目原文已在 `think/*.md`）
- `media/`：`肆季味.md` 迁回 `data/context/media/profile/`（媒体素材的对象档案与素材同住）

### Added

- `think/`：按**情境（触发点）**重组 `default/` 档案（原名 `meta/`，2026-10-17 改名）——8 组（睡醒时的千头万绪 / 战略失败 / 进度停滞 / AI 变成纯粹执行者 / 范围失控 / 不确定是否合规 / 自己不想看自己写的内容 / 不系于情境的条目），每组 `md` + `lino` + `ttl` 三格式，`index.*` 概括框架；守恒核对 40 节点、24 条目、26 条边全对（跨组边 4）

## [0.0.1] - 2026-10-17

初始版本。`data/context` 各分区的 `profile/` 迁入本仓，落为同名文件夹：`default/`、`work/`、`write/`、`media/`。
