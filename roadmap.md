# Roadmap

## Phase 1：建立共同语言
先掌握 scientific discovery loop、AI Scientist、Scientific Agent、benchmark、evaluation protocol、ablation、reproducibility、provenance。目标不是背模型名，而是能把论文放进科研流程。

## Phase 2：理解系统为什么会失败
从“能否完成任务”转向：失败发生在哪一步？是知识、检索、推理、工具、代码、数据还是评价器？系统能否发现当前路线收益已经很低并回退、换策略？对应 reliability、failure attribution、strategy switching。

## Phase 3：理解科学发现如何被证明
Evaluation Protocol（评测协议）应明确：可见数据、可用工具、允许修改对象、预算、运行方式、指标、baseline、重复实验、人工/自动评审和复现材料。

## Phase 4：收敛研究问题
优先选择：多篇论文反复暴露；可明确测量；不依赖无法获得的实验条件；可设计 baseline 与 ablation；贡献不只是“换更强模型”的问题。

**当前优先：Evaluation / Reliability → Strategy Switching → Research State & Provenance → Scientific Coding / Simulation → Closed-loop Discovery。**
