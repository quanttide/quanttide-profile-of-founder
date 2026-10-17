---
name: think-audit
description: 核对 think/ 档案的守恒性（节点与边数相对基线提交不变）。当新增或重组 think/ 档案、修改 ttl/lino、或需要验证 think/README.md 的「守恒与核对」时使用。
---

# think-audit

调用 Skill 自带的脚本，对比基线提交与当前 `think/` 的节点数、边数；两者相等即守恒。

## 用法

在 profile 仓库根目录运行：

```bash
python3 .agents/skills/think-audit/scripts/check_think_conservation.py --repo .
```

- 脚本随 Skill 放在 `.agents/skills/think-audit/scripts/check_think_conservation.py`，只读，不改档案。
- 基线提交记录在 `think/README.md`，运行时以其为准；可用 `--baseline <commit>` 覆盖。
- 退出码：守恒为 0，不等为 1。

## 口径

| 项 | 基线 | 当前 |
|----|------|------|
| 节点 | 基线提交的 `think/` + `work/` 全部 `.ttl`：` a pf:` 行数减 `IssueGroup` | `think/*.ttl`：` a pf:` 行数减 `Matter` |
| 边 | 基线提交的 `think/` + `work/` 全部 `.lino`：含 `evokes` / `responds_to` / `serves` / `excludes` 的行数 | `think/*.lino`，同口径（跨组边记在 `index.lino`） |

当前节点数、边数分别等于基线提交的对应值即守恒。

## 不等时

1. 先看脚本输出的基线 / 当前差值，定位是多出还是少了；
2. 新增或删除条目时，同步检查对应组的 `.ttl` 节点、`pf:nodes` 计数与 `index.md` 一览表；
3. 边只写在 `.lino`（一行一条），跨组边只写在 `index.lino`，组内文件不重复；
4. 若本轮确实要改变守恒基线（例如策略性增删），先确认意图，再在 `think/README.md` 更新期望值与基线提交。

## 环境边界

脚本自带在 Skill 内，profile 仓库独立检出即可运行；只要求本地 git 历史包含基线提交。
