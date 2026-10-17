# think · 守恒与核对

核对由 Skill `think-audit` 自带脚本 `.agents/skills/think-audit/scripts/check_think_conservation.py` 完成。基线提交记录在本文件，在档案仓库根目录显式传入：

```bash
python3 .agents/skills/think-audit/scripts/check_think_conservation.py --repo . --baseline 55c45b8
```

基线 `55c45b8` = 移除 `ai-collaboration` 组后的提交（原基线 `fe651c1` 用于核对按事情重组时的 62 节点 / 39 边）。脚本对比：

- 节点：期望 57
- 边：期望 35

2026-10-17 实测：57 = 57；35 = 35。
