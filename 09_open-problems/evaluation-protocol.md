# OP-02 深入：Scientific Agent Evaluation Protocol

## 1. 为什么“一个总分”不够

开放科研任务同时包含多个目标：

```text
Can it finish?
→ Is the result correct?
→ Can others reproduce it?
→ Does the evidence support the claim?
→ Is it novel?
→ Is it scientifically important?
```

把这些压成一个分数，会掩盖系统究竟强在哪里、失败在哪里。

## 2. Protocol 应固定什么

### Information boundary
模型能看到哪些论文？知识截止日期是什么？目标论文是否可能泄漏？

### Action boundary
允许搜索网页、运行代码、调用数据库、访问模拟器吗？

### Resource budget
token、时间、API 成本、GPU/CPU、实验次数。

### Human intervention
人类能否修代码、选择结果、提供实验反馈？

### Output
只交最终答案，还是同时交代码、日志、实验轨迹和 provenance？

### Evaluation
objective metric、expert review、LLM judge、replication、rediscovery、real experiment 各测什么？

## 3. 关键原则

评测协议的价值不是让 benchmark 看起来更复杂，而是**控制混杂变量**。

如果 Agent A 能搜索互联网而 B 不能；A 运行 100 次实验而 B 只有 5 次；A 有人工修复而 B 完全自动，那么最终结果不能直接解释为“Agent A 的科研能力更强”。

## 4. 下一步值得研究

- cost-normalized evaluation；
- contamination-resistant tasks；
- stepwise / trace verification；
- evaluator agreement；
- claim-level verification；
- dynamic benchmarks；
- long-horizon evaluation。

这条线与实验设计基础知识直接相连：control、baseline、ablation、variance、statistical significance 都会成为理解 Agent evaluation 的工具。
