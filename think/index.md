# think 档案框架（按情境重组）

> 从 `default/` 的五类档案按**情境**（触发点）重组——一个情境一组，情绪 / 方法 / 价值挂在它所处的情境下，挂不上情境的进 `loose-entries`（`default/` 已清理，基线 `git show f4013d1:…`）：一议题一组，每组三种格式——`.md` 条目原文、`.lino` 链接记法（一行一条边）、`.ttl` 图谱节点与态射；本组 `index.*` 概括框架。

## 情境组一览

| 文件 | 情境 | md 条目 | 图谱节点 | 组内边 |
|:--|:--|--:|--:|--:|
| `waking-thoughts.md` | 睡醒时的千头万绪 | 2 | 4 | 3 |
| `strategic-failure.md` | 战略失败 | 2 | 3 | 2 |
| `stalled-progress.md` | 进度停滞 | 1 | 1 | 0 |
| `ai-as-executor.md` | AI 变成纯粹执行者 | 2 | 3 | 3 |
| `scope-overrun.md` | 范围失控 | 4 | 6 | 6 |
| `compliance-doubt.md` | 不确定是否合规 | 3 | 4 | 3 |
| `unread-own-content.md` | 自己不想看自己写的内容 | 1 | 2 | 1 |
| `loose-entries.md` | 不系于情境的条目 | 13 | 17 | 4 |

合计：8 组 / 图谱节点 40（与 `default/index.ttl` 的节点数一致）/ 组内边 22 + 跨组边 4。

## 守恒与核对

```bash
# 基线 f4013d1 = default/ 清理前的最后一个提交（原文从 git 取）
# 1 节点（期望 40 = 40）
git show f4013d1:default/index.ttl | grep -c ' a pf:'
grep -h ' a pf:' think/*.ttl | grep -vc 'IssueGroup'

# 2 条目（期望 24 行、下面的循环无输出）
for f in triggers emotions methods values expressions; do git show f4013d1:default/$f.md; done | grep -c '^## '
for t in $(for f in triggers emotions methods values expressions; do git show f4013d1:default/$f.md; done | grep "^## " | sed "s/^## //"); do grep -qF "$t" think/*.md || echo "丢失: $t"; done

# 3 边（期望 26 = 26）
git show f4013d1:default/index.ttl | grep -c -E 'pf:(evokes|responds_to|serves|excludes) pf:'
grep -h -E -- '--(evokes|responds_to|serves|excludes)-->' think/*.lino | wc -l
```

2026-10-17 实测：40 = 40；24 行、无丢失；26 = 26（基线 f4013d1）。

## 未接边与待填充

- 「还散着的条目」一组的 10 个节点没有出边，暂不成链。
- 跨组的边只记在 `index.lino` 与 `index.ttl`，组内文件不重复。
- 方法容器（`思维框架` / `应对策略` 两个小节标题）随重组打散，不再作为条目。
