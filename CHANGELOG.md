# CHANGELOG

## [Unreleased]

## [0.1.0] - 2026-02-22

### 探索期

新增内容组织和构建规范。

- 新增项目概述：明确基于 Jupyter Book 构建的文档项目性质
- 新增构建命令：jb build、jupyter-book build、增量构建、本地预览
- 新增文档编写规范：Markdown 风格、文件命名、目录结构
- 重构 think 目录结构：从 think/*.md 迁移至 think/content/*.md
- 新增 write/content/handbook_code.md：软件工程手册占位

## [0.0.2] - 2026-02-17

### 探索期

AGENTS 和文档组成框架的完善。

- 新增 ROADMAP.md：产品路线图，明确三期目标
- AGENTS.md 新增版本规范：版本号语义、阶段目标、更新规范、发布节奏
- AGENTS.md 新增 ROADMAP 使用方法：核心原则、校准方法、阶段检查
- 更新版本规范：0.0.x（探索期）、0.x.y（验证期）、x.y.z（正式期）三层定义

## [0.0.1] - 2026-02-17

### 探索期

快速验证文档结构。

- 完善目录结构：新增 acad/、agent/、brand/、code/、knowl/、learn/、product/、stdn/、think/、write/ 等板块
- 新增文件夹 index.md：每个文件夹的内容摘要，包含主题分类和板块关联
- 新增 Jupyter Book 配置：完善的 _toc.yml 和 _config.yml
- 新增 AGENTS.md：Agent 工作指南，涵盖人机协作范式
- README.md 改为 index.md：内容从格式介绍改为内容摘要
- 完善 README：新增格式规范说明、构建命令、质量检查
- 更新首页 index.md：新增内容体系介绍与板块边界说明
