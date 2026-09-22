# AI for Science Learning

> 从“我看过哪些论文”升级为“AI for Science 在解决什么问题、为什么这样设计、证据是否充分、还缺什么”。

本仓库是长期维护的 **AI for Science research map + learning notes + living survey**。内容按研究问题与科学发现流程组织，而不是逐篇堆论文。

## 一张总图

```text
                         AI for Science
                               │
              ┌────────────────┼────────────────┐
              │                │                │
            MODEL            REASON          INTERACT
              │                │                │
      scientific models   hypothesis       code / data
                          search / plan     simulator / lab
                               │                │
                               └──────┬─────────┘
                                      ↓
                                    UPDATE
                         evidence → research state
                                      │
                                      ↺
```

当 **MODEL → REASON → INTERACT → UPDATE** 真正形成反馈循环时，系统才逐渐从 AI tool / Scientific Agent 走向 AI Scientist / autonomous scientific discovery。

## 当前研究地图

### 01 Foundations
- [Scientific Discovery Loop](01_foundations/scientific-discovery-loop.md)
- [AI Scientist vs Scientific Agent vs AI Co-Scientist](01_foundations/ai-scientist-vs-scientific-agent.md)

### 02 AI Scientist
- [Overview](02_ai-scientist/overview.md)
- [End-to-End Research / The AI Scientist](02_ai-scientist/end-to-end-research.md)

### 03 Reasoning & Search
- [Overview：Tree Search → Strategy Switching](03_reasoning-and-search/overview.md)
- [Idea Generation → Evaluation → Selection](03_reasoning-and-search/idea-generation-and-selection.md)
- [Strategy Switching / Meta-reasoning](09_open-problems/strategy-switching.md)

### 04 Scientific Agents
- [Scientific Agents](04_scientific-agents/overview.md)

### 05 Scientific Coding
- [Scientific Coding / ERA](05_scientific-coding/overview.md)

### 06 Evaluation
- [Evaluation Overview](06_evaluation/overview.md)
- [Benchmark](06_evaluation/benchmark.md)
- [Ablation](06_evaluation/ablation.md)
- [LLM-as-a-Judge / Cross-model Review](06_evaluation/llm-as-judge.md)
- [SoundnessBench](06_evaluation/soundnessbench.md)
- [Evaluation Protocol 深入](09_open-problems/evaluation-protocol.md)

### 07 Reliability
- [Reliability Overview](07_reliability/overview.md)
- [Critic & Executable Verification](07_reliability/critic-and-verification.md)
- [Verification Gap](07_reliability/verification-gap.md)
- [Research State / Memory / Provenance](07_reliability/research-state-and-provenance.md)

### 08 Closed-loop Discovery
- [Overview](08_closed-loop-discovery/overview.md)
- [Robin](08_closed-loop-discovery/robin.md)

### 09 Open Problems
- [Research Map](09_open-problems/research-map.md)
- [Strategy Switching](09_open-problems/strategy-switching.md)
- [Evaluation Protocol](09_open-problems/evaluation-protocol.md)

### 10 Case Studies
- [AI Co-Scientist](10_case-studies/co-scientist.md)
- [Co-Scientist / The AI Scientist / ERA / Robin 对照](10_case-studies/comparison.md)

### 11 Learning Notes
- [Evaluation Protocol](11_learning-notes/evaluation-protocol.md)
- [Ablation](11_learning-notes/ablation.md)

### Papers & Radar
- [Paper Index](papers/index.md)
- [Paper Template](papers/paper-template.md)
- [The AI Scientist](papers/the-ai-scientist.md)
- [ERA](papers/era.md)
- [Robin](papers/robin.md)
- [Paper Radar](radar/README.md)
- [2026-09 Radar](radar/2026-09.md)
- [Deferred / Rejected](radar/rejected.md)

## 已迁入的学习主线

过去的学习内容现在被重新组织成一条连续链，而不是聊天碎片：

```text
Scientific Discovery Loop
        ↓
AI Co-Scientist：生成/比较 hypothesis
        ↓
The AI Scientist：端到端执行
        ↓
ERA：scorable scientific coding + tree search
        ↓
Robin：真实实验反馈 + hypothesis update
        ↓
问题开始暴露
        ├─ 执行前判断可靠吗？ → SoundnessBench
        ├─ Judge 可靠吗？ → LLM-as-a-Judge
        ├─ 为什么失败？ → Failure Attribution
        ├─ 何时换路线？ → Strategy Switching
        ├─ 长期如何记住研究？ → Research State
        └─ Claim 为什么可信？ → Verification / Provenance
```

## 当前最值得继续收敛的方向

仓库暂不急于选最终研究题目。优先积累五个彼此相连的问题：

1. **Scientific Agent Evaluation / Reliability**
2. **Strategy Switching / Meta-reasoning**
3. **Failure Attribution / Executable Critic**
4. **Research State / Memory / Provenance**
5. **Scientific Coding / Simulation as a reproducible AI-Scientist sandbox**

它们共同围绕一个核心问题：

> **怎样让 AI Scientist 不只是更快地产生研究，而是知道自己为什么这样做、什么时候做错、该怎样改变路线，以及我们凭什么相信最终结论。**

## 阅读标记

🟢 已学习 · 🟡 已粗读 · ⚪ 待读 · 🔵 基础/代表性 · 🟣 前沿

## 新论文准入原则

新论文先进入 `radar/`。优先进入正式地图的工作应至少带来一种变化：**新的研究问题、新的方法机制、新 evaluation protocol / benchmark、新的真实闭环，或对已有结论的重要修正。**

普通“LLM + RAG + multi-agent + tool use”组合，如果没有上述变化，不因为论文新就扩展主地图。

## 使用方法

学习时固定沿着：

**为什么出现 → 解决什么问题 → 在科研闭环哪里 → 方法为什么这样设计 → 如何验证 → Ablation 排除了什么解释 → 哪里仍失败 → 下一步能怎么改。**

从这里开始：[Roadmap](roadmap.md) · [Glossary](glossary.md) · [Open Problems](09_open-problems/research-map.md)
