# Reasoning & Search

科研不是线性链，而是带分支、失败、回退和重新规划的搜索。

最简单的自动循环“生成方案 → 评分 → 修改 → 再评分”容易陷入局部改进：如果 A 已到平台期，继续修改 A 不代表会想到结构不同的 B 或 C。

## Tree Search

```text
Idea
├─ A
│  ├─ A1
│  └─ A2
├─ B
└─ C
```

树搜索保留多个候选路线，可在分支停滞时回到祖先节点。ERA 是 empirical software 自动改进的重要实例：候选程序形成树，根据评分继续扩展，而不是只保留一条线性修改轨迹。

## 更深的问题：AI 的“耐心”

Tree search 本身仍未回答：什么叫 plateau？何时放弃？该回退、换 mutation 还是切换整个研究范式？如何区分“路线错了”和“实现还没优化好”？探索新路线应花多少预算？

因此要把 tree search 与 **failure attribution → strategy switching → meta-reasoning → exploration/exploitation** 连起来。

> 核心开放问题：能否让 AI Scientist 不只是搜索更多候选，而是识别当前研究策略为什么失效，并选择结构不同的下一种策略？
