# Scientific Discovery Loop：AI4S 的主骨架

## 1. 为什么先学“科研循环”

AI for Science 很容易被看成一堆模型、Agent 和论文。更稳定的理解方式是先看科学研究本身的信息流：

```text
已有知识 / Observation
        ↓
Research Question
        ↓
Hypothesis
        ↓
Experiment / Simulation
        ↓
Data
        ↓
Analysis
        ↓
Scientific Claim
        ↓
Verification / Revision
        └────────────↺
```

AI4S 的不同工作，本质上是在自动化或增强其中一个或多个环节。

## 2. 三个层次

### 2.1 单点能力
例如预测蛋白质结构、生成分子、分析显微图像。AI 提高某一步能力，但研究决策主要仍由人完成。

### 2.2 Scientific Agent
Agent 可以检索文献、写代码、调用数据库/模拟器并完成多步任务。关键变化是 AI 开始**行动**，而不只是一次性预测。

### 2.3 AI Scientist / Autonomous Discovery
系统还要根据实验结果改变下一步研究决策。真正的难点从“能不能调用很多工具”变成：

- 如何提出值得验证的 hypothesis；
- 如何选择下一次 experiment；
- 如何判断结果支持还是反驳 hypothesis；
- 失败后改哪一层；
- 如何证明最后的 scientific claim 可信。

## 3. 闭环与 workflow 的区别

```text
Workflow:
检索 → 写代码 → 跑实验 → 写报告

Closed loop:
假设 → 实验 → 结果 → 更新研究状态
 ↑                         ↓
 └────── 下一轮决策 ────────┘
```

因此“模块很多”并不等于“自动科学发现”。判断一篇论文是否真正推进 autonomous science 时，应寻找**反馈是否改变后续决策**的证据。

## 4. 与仓库其他章节的关系

- Reasoning & Search：决定下一步做什么；
- Scientific Coding：把想法变成可执行实验；
- Evaluation：判断研究是否真的进步；
- Reliability：判断错误发生在哪里；
- Research State / Provenance：保存长期证据与决策历史；
- Closed-loop Discovery：把上述组件连接成循环。

这张 loop 是以后读论文时的第一张定位图。
