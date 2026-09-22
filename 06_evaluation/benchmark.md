# Benchmark：到底在测什么？

## 1. Benchmark 不是“一个数据集”

科研 Agent benchmark 至少包含：

```text
Task distribution
+ data / environment
+ tool access
+ execution protocol
+ metric / evaluator
+ budget
```

因此比较两个 benchmark 时，不能只看题目数量。

## 2. 三层评价对象

### Capability
Agent 会不会检索、编码、分析数据、规划实验？

### Process
Agent 的中间步骤是否合理？错误发生在哪里？是否会恢复？

### Scientific outcome
最终 claim 是否正确、可复现、新颖且有意义？

很多 benchmark 主要测第一层，却容易被解读成第三层。

## 3. AstaBench

AstaBench 代表“标准化 scientific-agent tasks”路线。它的重要性在于将真实科研任务与可控工具环境、日志和成本结合，使不同 Agent 更可比较。

适合测：
- literature search；
- data analysis；
- coding / tool use；
- 多步 scientific tasks。

局限是：完成预定义任务与真正自主选择研究问题仍有距离。

## 4. SciAgentArena

SciAgentArena 代表 stepwise verification 思路：不只看最终输出，而是把科学任务拆成可检查步骤。

这种设计对 failure attribution 很重要，因为它开始回答“Agent 在哪一步坏掉”。

## 5. ResearchClawBench / rediscovery

Rediscovery benchmark 的基本思想：

```text
给 Agent 截止到 t0 的知识
→ 隐藏 t1 的目标发现
→ 让 Agent 独立研究
→ 比较是否重新发现目标方法
```

优点：现实历史中已经存在一个有价值的发现作为参照。

风险：contamination、目标论文信息泄漏，以及“历史上走过这条路”不等于“这是唯一正确研究路径”。

## 6. Benchmark 的核心学习方法

以后遇到 benchmark，固定问：

**任务是什么 → 信息边界是什么 → Agent 能做什么 → 预算多少 → 最终怎么判 → 这个分数究竟能支持什么结论。**
