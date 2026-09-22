# Robin — A multi-agent system for automating scientific discovery

- **Status**: 🟢🟣
- **Venue**: Nature, 2026
- **Node**: Scientific Agents / Closed-loop Discovery

## Problem
能否把文献研究、hypothesis generation、实验建议、数据分析与 hypothesis update 连成持续的科学发现循环？

## Core idea
Robin 组合 literature-search agents 与 data-analysis agents。真实实验结果返回后，系统解释数据并产生更新后的 hypothesis。

## Why it matters
重要点不是“用了 multi-agent”，而是**新 observation 会改变下一轮 scientific reasoning**。

## Automation boundary
真实 wet-lab 实验仍由人类执行，因此应理解为 semi-autonomous / lab-in-the-loop，而不是完全无人实验室。

## Open questions
hypothesis novelty、分析冲突、失败实验、人工隐含判断以及 claim provenance 仍需要更严格的评价与追踪。
