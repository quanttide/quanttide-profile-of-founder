# 量潮创始人档案

本项目是创始人工作实录的文档库，以 Markdown 格式编写，使用 Jupyter Book 构建。

## 格式规范

### 文件命名

- 使用小写字母
- 单词之间用连字符 `-` 分隔
- 示例：`agent.md`、`product-roadmap.md`、`think-process.md`

### 目录结构

```
.
├── index.md           # 首页（内容总览）
├── _config.yml        # Jupyter Book 配置
├── _toc.yml           # 目录结构
├── AGENTS.md          # Agent 操作指南
├── 板块名/            # 按主题划分的目录
│   ├── README.md      # 板块介绍
│   └── *.md           # 具体文档
└── _static/           # 静态资源（图片等）
```

### 目录命名

- 使用小写字母
- 使用复数形式
- 示例：`think/`、`write/`、`learn/`

### Markdown 规范

- 标题使用 ATX 风格（`#`、`##`、`###`）
- 代码块使用 fenced code（\`\`\`）
- 列表使用 `-` 或 `1.`
- 链接使用 `[文字](路径)` 格式
- 区块之间保留空行

### 板块划分

| 目录 | 含义 |
|------|------|
| `think/` | 思考 |
| `agent/` | 智能体工程 |
| `knowl/` | 知识工程 |
| `learn/` | 学习 |
| `stdn/` | 标准化 |
| `write/` | 写作 |
| `code/` | 编程 |
| `brand/` | 品牌管理 |
| `acad/` | 学术研究 |
| `product/` | 产品研发 |
