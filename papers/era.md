# ERA — An AI system to help scientists write expert-level empirical software

- **Status**: 🟢🟣
- **Venue**: Nature, 2026
- **Node**: Scientific Coding / Reasoning & Search

## Problem
科学计算经常受限于高质量 empirical software 的人工开发速度。能否让 AI 围绕明确的科学质量指标自动创造和改进软件？

## Core idea
ERA 把 LLM 生成代码、sandbox execution、objective scoring 与 tree search 连接起来，并允许系统吸收论文/教材等外部 research ideas。

## Why tree search
线性修改容易被当前方案限制。搜索树保留历史候选，使系统可以从不同节点继续探索和重组研究思想。

## What it teaches us
ERA 是“AI 写代码”向“AI 搜索经验科学方法”的跨越：代码是实验对象，score 是反馈，tree 是研究轨迹。

## Limitation / open question
客观指标提供了很强的反馈，但真实科研往往没有如此清晰的单一 reward。即使有 tree search，系统也未必理解“为什么当前路线失败”。

因此它直接引出：plateau detection、failure attribution、strategy switching、meta-reasoning。
