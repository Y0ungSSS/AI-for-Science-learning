# 学习与研究路线

> 目标：从理解 AI Scientist 的科研闭环，逐步具备**读论文、复现、识别前作冲突、设计可证伪实验**的能力。当前研究判断以[问题树](调研/问题树.md)和[研究树](调研/研究树.md)为准。

## 阶段 1：理解研究对象

阅读 [Scientific Discovery Loop](01_foundations/scientific-discovery-loop.md) 和 [AI Scientist 与 Scientific Agent](01_foundations/ai-scientist-vs-scientific-agent.md)，区分 hypothesis、experiment、observation、belief、claim 与 evidence。

**验收**：能够画出一个系统的科研状态转移，并指出哪一步产生可独立核验的科学证据。

## 阶段 2：理解代表系统与机制

阅读 [端到端科研](02_ai-scientist/end-to-end-research.md)、[论文索引](papers/index.md)，再沿[研究树 A–I](调研/研究树.md)对照至少三篇机制相近的工作。

**验收**：写出 Problem、Core mechanism、最近 anchor、独立增量、Evidence limitation；不要只复述架构图。

## 阶段 3：学习可靠性与评测

阅读 [Evaluation](06_evaluation/overview.md)、[Verification Gap](07_reliability/verification-gap.md) 和 [Ablation](11_learning-notes/ablation.md)。重点理解 oracle、数据泄漏、反事实、预算归因、置信区间、模型与 scaffold 的交互。

**验收**：能够为一项科研 Agent 声称的改进设计公平 baseline、消融和否证条件。

## 阶段 4：从问题树到预实验

在[问题树 Q1–Q9](调研/问题树.md)选一个具体问题，按下列关口推进：

| 关口 | 必须完成 |
|---|---|
| G0 前作 | 最近 3–5 篇直接前作，明确不能重复声称的机制 |
| G1 环境 | 小型可执行任务、独立 oracle、可复现种子 |
| G2 缺陷 | 简单基线确有稳定、可解释的失败 |
| G3 贡献 | 固定预算下机制有独立收益，消融支持归因 |
| G4 泛化 | 未见任务/故障/环境下仍有效，并报告负结果 |

**验收**：形成可复现实验记录，而不只是一个 Agent 原型或 prompt。

## 当前推荐研究顺序

Reliability / Evaluation → Failure Attribution & Intervention → Strategy Switching → Research State & Provenance → Scientific Coding / Simulation → Closed-loop Discovery。

这是一条**学习与低资源实验路径**，不是声称后面的方向不重要。最新饱和度、优先级和前作冲突以问题树为准。
