# 贡献指南

欢迎贡献本项目！本文档提供贡献相关指南。

## 贡献方式

- 报告问题：通过 GitHub Issues 反馈
- 提交修改：通过 Pull Request 贡献代码或文档

## 开发环境

### 构建命令

```bash
# 构建 HTML（单文件）
jupyter-book build index.md --site

# 构建并预览
jupyter-book start .

# 清理构建文件
jupyter-book clean .
```

### 验证清单

- [ ] 所有内部链接指向已存在的文件
- [ ] `_toc.yml` 中引用的文件均已创建
- [ ] YAML 文件语法正确
- [ ] 新增文件已添加到 `_toc.yml`
- [ ] 构建无错误

## 提交流规范

### 文件命名

- 使用小写字母
- 单词间用下划线 `_` 分隔
- 示例：`agent.md`、`product_roadmap.md`

### Markdown 风格

- 标题使用中文或英文，保持一致性
- 列表使用 `-` 或 `1.` ，保持统一
- 代码块标注语言：` ```python `, ` ```bash ` 等
- 链接使用相对路径，内部引用用 `[文字](目录/文件.md)`

### 目录结构

```
板块名/
├── index.md        # 板块入口，内容摘要
├── README.md       # 板块说明（可选）
├── 子1.md
└── 子目录主题/
    ├── index.md
    └── 内容.md
```

### 提交信息规范

- 使用中文或英文，保持一致性
- 提交应包含完整且独立的变更

## 提交流程

1. **Fork 仓库**
2. **创建分支**：`git checkout -b feature/xxx` 或 `git checkout -b fix/xxx`
3. **进行修改**
4. **验证构建**：`jupyter-book build index.md --site`
5. **提交更改**
6. **推送分支**：`git push origin branch-name`
7. **创建 Pull Request**

## 常见任务

### 添加新文档

1. 在对应目录下创建 `.md` 文件
2. 更新该目录的 `index.md`
3. 在 `_toc.yml` 中注册文件
4. 运行 `jupyter-book build index.md --site` 验证

### 添加新板块

1. 创建目录（遵循命名规范：小写、复数）
2. 创建 `index.md` 介绍板块内容
3. 在根目录 `index.md` 板块边界部分添加说明
4. 在 `_toc.yml` 中注册
5. 运行构建验证

## 注意事项

- 本项目为文档项目，无需 lint/test 流程
- 更新目录结构后需同步更新 index.md、README.md、_toc.yml 三处

## 联系方式

如有疑问，可通过 GitHub Issues 联系维护者。
