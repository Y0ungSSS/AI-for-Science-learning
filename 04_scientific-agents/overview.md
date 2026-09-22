# Scientific Agents

## 1. 从 LLM 到 Agent

LLM 主要完成一次输入到输出的映射；Agent 则维护状态、选择行动并与外部环境反复交互。

```text
State
 ↓
Reason / Plan
 ↓
Action → Tool / Database / Code / Simulator / Lab
 ↑                                      ↓
 └──────────── Observation ─────────────┘
```

Scientific Agent 的特殊之处是：最终目标不是“把任务做完”，而是得到有证据支撑的科学结论。

## 2. 为什么 multi-agent 不是核心贡献本身

把 literature、coding、analysis 分给多个 Agent 可以帮助模块化，但“用了多个 Agent”并不自动产生科学价值。

真正应问：

- 信息怎样在 Agent 间传递？
- 是否保存证据来源？
- 谁决定下一步研究行动？
- Agent 之间的 disagreement 如何解决？
- 最终 claim 如何验证？
- 多 Agent 相比单 Agent 到底贡献了什么？

因此本仓库不会把普通“LLM + RAG + multi-agent + tools”组合自动视为重要前沿。

## 3. Robin 的意义

Robin 的关键不是“multi-agent”这个标签，而是 literature search、hypothesis、实验建议、真实实验结果分析和 updated hypothesis 被连接起来。

这使它成为理解 **lab-in-the-loop scientific discovery** 的案例。

## 4. 后续学习方向

Scientific Agents 后续与四条线交叉：

**Agent architecture**：planning、tool use、memory、multi-agent coordination。

**Scientific reasoning**：hypothesis、causal reasoning、strategy switching。

**Environment**：code、simulator、database、real laboratory。

**Reliability**：evaluation、verification、provenance、failure attribution。
