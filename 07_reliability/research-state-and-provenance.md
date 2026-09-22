# Research State / Memory / Provenance

## 1. 为什么聊天历史不是 Research State

长上下文能保存文字，但科研状态需要结构化回答：

- 当前有哪些 hypotheses？
- 哪些 evidence 支持/反驳它们？
- 哪些实验已经做过？
- 哪些失败不能重复？
- 当前代码和数据版本是什么？
- 为什么上次决定放弃路线 A？
- 某个 claim 来自哪次实验？

## 2. 三层记忆

### Working state
当前任务、当前实验、下一步计划。

### Episodic research memory
过去尝试、失败、策略切换和实验历史。

### Provenance graph
claim 与 evidence、code、data、literature、decision 的来源关系。

## 3. 一个简单表示

```text
Hypothesis H2
├─ supports: R4, Paper P7
├─ contradicts: R6
├─ derived_from: H1
├─ tested_by: E3, E5
└─ status: uncertain

Experiment E5
├─ code: commit C12
├─ data: D3
├─ seed: 42
├─ metric: M2
└─ result: R6
```

## 4. 为什么这会影响 reasoning

没有结构化 state，Agent 可能：
- 重复失败实验；
- 忘记反例；
- 只记住成功结果；
- 在长任务中发生 semantic drift；
- 无法解释策略切换原因。

因此 memory 不只是“上下文不够长”的工程问题，而是 scientific reasoning 的组成部分。

## 5. 与未来研究的连接

Research state 是 strategy switching、failure attribution、verification 和 reproducibility 的共同基础。没有状态记录，就很难判断“Agent 为什么做了这个决定”。
