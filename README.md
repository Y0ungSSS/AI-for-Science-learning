# AI for Science Learning

> 目标：把“看过哪些论文”升级为“AI for Science 领域在解决什么问题、用了什么机制、证据是否充分、还缺什么”。

本仓库用于长期构建 AI for Science（AI4S）研究地图。内容按**研究问题与科学发现流程**组织，而不是按论文逐篇堆叠。

## 总地图

```text
AI for Science
├─ Foundations：AI4S 与 scientific discovery loop
├─ AI Scientist：从辅助工具到端到端科研系统
├─ Reasoning & Search：搜索、规划、回退、策略切换
├─ Scientific Agents：Agent、工具、环境、记忆
├─ Scientific Coding：代码、仿真、实验迭代
├─ Evaluation：Benchmark、Protocol、Judge、复现、Ablation
├─ Reliability：失败归因、幻觉、Provenance、可验证性
├─ Closed-loop Discovery：虚拟实验、真实实验、自动实验室
└─ Open Problems：尚未解决的问题与可能研究方向
```

简化理解：**MODEL → REASON → INTERACT → UPDATE**。当模型能够提出假设、与科学环境交互，并依据新证据更新研究状态时，才逐渐接近 AI Scientist / autonomous scientific discovery。

## 当前优先主线

1. Scientific Agent evaluation / reliability
2. Strategy switching / meta-reasoning / failure recovery
3. Failure attribution / verification
4. Research state / memory / provenance
5. Scientific coding / simulation
6. Benchmark / evaluation protocol

这些不是六个孤立方向：可靠的科研 Agent 必须保存研究状态，在搜索空间中选择策略，执行实验，识别失败，并通过严格的评测协议证明它确实取得了进展。

## 阅读标记

🟢 已学习 · 🟡 已粗读 · ⚪ 待读 · 🔵 基础/代表性 · 🟣 前沿

## 使用原则

新论文先进入 `radar/`。只有当它引入新的研究问题、方法机制、评测协议、真实科学闭环，或对现有结论形成重要修正时，才进入正式研究地图。

学习一篇论文时始终追问：

**为什么出现 → 解决什么问题 → 在科研闭环哪里 → 方法为什么这样设计 → 如何验证 → 哪里仍然失败 → 下一步可以怎么改。**

## 入口

- [Roadmap](roadmap.md)
- [术语表](glossary.md)
- [论文索引](papers/index.md)
- [Reasoning & Search](03_reasoning-and-search/overview.md)
- [Evaluation](06_evaluation/overview.md)
- [Reliability](07_reliability/overview.md)
- [Closed-loop Discovery](08_closed-loop-discovery/overview.md)
- [Open Problems](09_open-problems/research-map.md)
- [Paper Radar](radar/README.md)
