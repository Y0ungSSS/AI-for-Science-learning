# Evaluation：AI Scientist 到底有没有做出科学进步？

Evaluation 是独立研究主线，不只是论文最后的一张性能表。

AI Scientist 的输出可能是假设、实验、研究代码、新算法、分析结论或论文。“写得像论文”与“科学结论正确”不是同一目标。

## Evaluation Protocol

```text
Task
├─ Input / hidden information
├─ Available tools
├─ Compute / token / monetary budget
├─ Human intervention
├─ Number of attempts
└─ Output artifacts

Evaluation
├─ Objective metric
├─ Human expert
├─ LLM judge
├─ Re-execution / replication
├─ Rediscovery
└─ Real-world experiment
```

如果条件不同，两个 Agent 的分数可能不可比。

## 代表性路线

**固定任务 benchmark**：适合检索、代码、数据分析等标准化能力，AstaBench 属于这一类。

**Target-paper rediscovery**：让 Agent 从较早知识状态重新发现已有方法；有现实参考，但需防信息泄漏与历史路径依赖。

**LLM-as-a-Judge / multi-model review**：适合开放输出，但要测 judge bias 与 agreement。

**Human expert review**：更接近真实科研评价，但昂贵且存在专家分歧。

**Real experiment**：证据直接，但实验成立仍不自动等于研究有新意。

未来应区分：**task completion → correctness → reproducibility → claim verification → novelty → scientific significance**。
