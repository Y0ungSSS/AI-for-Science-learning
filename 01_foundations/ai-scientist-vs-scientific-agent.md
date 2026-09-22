# AI Scientist vs Scientific Agent vs AI Co-Scientist

这三个词经常混用，但理解它们的差异能避免“看到 Agent 就等于自动科研”的误区。

## 1. Scientific Agent

Scientific Agent 是面向科学任务的 Agent。它可能只负责科研流程中的一个局部，例如文献检索、数据分析、代码执行或实验规划。

```text
LLM
 + state
 + tools
 + action loop
 = Agent

Agent
 + scientific task
 + scientific constraints
 = Scientific Agent
```

因此 Scientific Agent 不要求覆盖完整科研生命周期。

## 2. AI Co-Scientist

Co-Scientist 强调**协作关系**。AI 帮助人类研究者生成、比较、改进和评估 hypotheses / proposals，但人仍然处于研究决策链中。

Google 的 AI co-scientist 是这一范式的代表案例。它把候选 scientific hypotheses 的生成与多 Agent 的评价、排序和演化连接起来。

## 3. AI Scientist

AI Scientist 更强调**研究过程自主性**：

```text
Research Question
→ Idea / Hypothesis
→ Literature
→ Method
→ Experiment
→ Analysis
→ Revision
→ Scientific Output
```

The AI Scientist 是端到端计算研究的代表；Robin 则展示了实验生物学中 human/lab-in-the-loop 的闭环。

## 4. 不要把 autonomy 当成单一开关

更合理的理解是二维：

| 维度 | 问题 |
|---|---|
| Coverage | 系统覆盖科研流程多少阶段？ |
| Autonomy | 每一步需要多少人类决策？ |
| Reliability | 自动完成的步骤是否可信？ |
| Verification | 结论能否被独立验证？ |

因此“更自动”不必然意味着“更像优秀科学家”。

## 5. 阅读论文时的定位法

看到一个新系统，先问：

1. 它自动化科研 loop 的哪几步？
2. 哪些步骤仍由人完成？
3. 新 observation 会不会改变下一步决策？
4. 它评价的是最终任务、研究过程，还是 scientific claim？
5. 它留下了什么可复现证据？

这五问比先判断它属于“single-agent / multi-agent”更有用。
