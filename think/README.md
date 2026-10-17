# think · 守恒与核对

核对由 Skill `think-audit` 自带脚本 `.agents/skills/think-audit/scripts/check_think_conservation.py` 完成。在档案仓库根目录运行：

```bash
python3 .agents/skills/think-audit/scripts/check_think_conservation.py --repo .
```

基线 `fe651c1` = 旧 `think/`（情境视图）与 `work/`（事件视图）的最后提交。脚本对比：

- 节点：期望 62 = 40 + 22
- 边：期望 39 = 26 + 13（其中跨组 1 条记在 `index.lino`）

2026-10-17 实测：62 = 62；39 = 39（跨组 1）。
