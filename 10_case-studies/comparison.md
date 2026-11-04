# 四个核心案例放在同一张图里

> 教学用途的代表系统比较，不是最新排名。机制和反证请查看 [研究树](../调研/研究树.md)；选题请查看 [问题树](../调研/问题树.md)。

> 这是教学用途的代表系统比较，不是最新系统排名。更近的机制和反证请查看 [研究树](../调研/研究树.md)；从案例寻找研究问题时查看 [问题树](../调研/问题树.md)。

| 系统 | 主要自动化对象 | 反馈来源 | 最值得学的机制 | 暴露的问题 |
|---|---|---|---|---|
| AI Co-Scientist | hypothesis / proposal | evaluator / ranking | pairwise debate、ranking、idea evolution | 执行前评价是否可信 |
| The AI Scientist | ML research lifecycle | experiment + reviewer | end-to-end、tree search、journal、review | 可靠性、实验错误、verification |
| ERA | empirical scientific software | objective score | LLM + tree search + external ideas | scorable task 与真实 discovery 的差距 |
| Robin | experimental biology loop | wet-lab results | literature + hypothesis + experiment + update | 人类实验边界、claim verification |

## 共同主线

```text
Task / Baseline
      ↓
Evidence / Literature
      ↓
Hypothesis / Idea
      ↓
Evaluate & Select
      ↓
Implement
      ↓
Controlled Experiment
      ↓
Analyze
      ↓
Keep / Modify / Reject
      ↓
Iterate
```

这张图比“单 Agent / 多 Agent”分类更适合当前学习阶段，因为它直接展示每个系统自动化了科研闭环的哪一段。

## 一个正在变得清晰的核心矛盾

当前系统越来越擅长**生成候选研究并执行流程**，但“判断哪个想法值得执行”“失败后为什么失败”“最终 claim 是否可信”仍明显困难。

因此仓库当前主线自然收敛到：

**Evaluation → Critic/Verification → Failure Attribution → Strategy Switching → Research State/Provenance。**
