# Robin：真实实验进入 AI 科研闭环

## 1. Problem

生物学中的 AI 工具已经能做文献检索、数据分析或 hypothesis generation，但把这些认知步骤持续连接起来更困难。Robin 试图让系统根据实验结果继续形成新的科学假设。

## 2. System loop

```text
Literature search
→ Hypothesis generation
→ Proposed experiment
→ Human-performed wet-lab experiment
→ Data analysis
→ Interpretation
→ Updated hypothesis
→ next cycle
```

因此更准确的描述是 **semi-autonomous scientific discovery**：AI 自动化了大量认知环节，但物理实验仍需要实验人员完成。

## 3. Agent decomposition

Robin 组合文献检索 Agent 与数据分析 Agent。系统从文献证据形成候选 hypotheses，并使用评审/筛选过程选择后续实验方向；真实实验结果返回后，数据分析模块进行多条分析轨迹，再综合形成解释和下一轮假设。

## 4. 为什么它比“multi-agent”更重要

核心贡献应从闭环理解：

**Observation 改变了 Hypothesis。**

如果没有这一步，多 Agent 只是在自动执行预先确定的 workflow；有了 feedback，系统开始接近科学发现中的 iterative hypothesis revision。

## 5. 仍然要追问的问题

- hypothesis 的 novelty 如何独立验证？
- 失败实验如何影响下一轮 hypothesis？
- 不同分析轨迹冲突时，怎样判断哪条解释更可信？
- 人类实验者提供了多少隐含判断？
- 最终发现的贡献应归因于 Agent、已有文献还是实验反馈中的哪一部分？

这些问题把 Robin 与 Evaluation、Provenance 和 Failure Attribution 连接起来。
