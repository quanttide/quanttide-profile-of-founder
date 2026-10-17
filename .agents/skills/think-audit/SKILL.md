---
name: think-audit
description: 核对 think/ 档案的守恒性（节点与边数相对基线 fe651c1 不变）。当新增或重组 think/ 档案、修改 ttl/lino、或需要验证 think/README.md 的「守恒与核对」时使用。
---

# think-audit

调用实验室仓库的脚本，对比基线提交与当前 `think/` 的节点数、边数；两者相等即守恒。

## 用法

在 profile 仓库根目录运行：

```bash
python3 ../../examples/quanttide-founder-lab/scripts/check_think_conservation.py --repo .
```

- 脚本在 lab 仓库 `scripts/check_think_conservation.py`，只读，不改档案。
- 默认基线 `fe651c1`（旧 `think/` 情境视图与 `work/` 事件视图的最后提交），可加 `--baseline <commit>` 换基线。
- 退出码：守恒为 0，不等为 1。

## 口径

| 项 | 基线 | 当前 |
|----|------|------|
| 节点 | `fe651c1` 的 `think/` + `work/` 全部 `.ttl`：` a pf:` 行数减 `IssueGroup` | `think/*.ttl`：` a pf:` 行数减 `Matter` |
| 边 | `fe651c1` 的 `think/` + `work/` 全部 `.lino`：含 `evokes` / `responds_to` / `serves` / `excludes` 的行数 | `think/*.lino`，同口径（跨组边记在 `index.lino`） |

期望：节点 62（基线 40 + 22），边 39（基线 26 + 13，其中跨组 1 条）。

## 不等时

1. 先看脚本输出的基线 / 当前差值，定位是多出还是少了；
2. 新增或删除条目时，同步检查对应组的 `.ttl` 节点、`pf:nodes` 计数与 `index.md` 一览表；
3. 边只写在 `.lino`（一行一条），跨组边只写在 `index.lino`，组内文件不重复；
4. 若本轮确实要改变守恒基线（例如策略性增删），先确认意图，再在 `index.md` 更新期望值与基线提交。

## 环境边界

脚本位于 monorepo 的 `examples/quanttide-founder-lab/` 下。profile 单独检出（没有同级 `examples/`）时，路径不存在，需在完整 monorepo 工作区运行。
