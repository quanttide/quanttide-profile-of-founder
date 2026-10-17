# meta 议题档案 · 框架

> 从 `default/` 的五类档案按**个人议题**重组：一议题一组，每组三种格式——`.md` 条目原文、`.lino` 链接记法（一行一条边）、`.ttl` 图谱节点与态射；本组 `index.*` 概括框架。

## 议题组一览

| 文件 | 议题 | md 条目 | 图谱节点 | 组内边 |
|:--|:--|--:|--:|--:|
| `紧张与高压.md` | 紧张与高压 | 3 | 5 | 4 |
| `战略失败.md` | 战略失败 | 2 | 3 | 2 |
| `AI 关系.md` | AI 关系 | 2 | 3 | 3 |
| `规模的拉扯.md` | 规模的拉扯 | 4 | 6 | 6 |
| `疏离.md` | 疏离 | 4 | 6 | 6 |
| `厌倦.md` | 厌倦 | 3 | 4 | 2 |
| `价值线.md` | 价值线 | 1 | 3 | 2 |
| `还散着的条目.md` | 还散着的条目 | 9 | 10 | 0 |

合计：8 组 / 图谱节点 40（与 `default/index.ttl` 的节点数一致）/ 组内边 25 + 跨组边 1。

## 守恒与核对

```bash
# 1 节点（期望 40 = 40）
grep -c ' a pf:' default/index.ttl
grep -h ' a pf:' meta/*.ttl | grep -vc 'IssueGroup'

# 2 条目（期望 24 行、下面的循环无输出）
grep -h '^## ' default/{triggers,emotions,methods,values,expressions}.md | wc -l
for t in $(grep -h '^## ' default/{triggers,emotions,methods,values,expressions}.md | sed 's/^## //'); do grep -qF "$t" meta/*.md || echo "丢失: $t"; done

# 3 边（期望 26 = 26）
grep -h -E 'pf:(evokes|responds_to|serves|excludes) pf:' default/index.ttl | wc -l
grep -h -E -- '--(evokes|responds_to|serves|excludes)-->' meta/*.lino | wc -l
```

三条 2026-10-17 实测：40 = 40；24 行、无丢失；26 = 26。

## 未接边与待填充

- 「还散着的条目」一组的 10 个节点没有出边，暂不成链。
- 跨组的边只记在 `index.lino` 与 `index.ttl`，组内文件不重复。
- 方法容器（`思维框架` / `应对策略` 两个小节标题）随重组打散，不再作为条目。
