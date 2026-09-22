# SoundnessBench：AI Scientist 能否在实验前识别坏研究想法？

- **Status**: 🟡🟣
- **Year**: 2026
- **Node**: Evaluation / Critic / Idea Selection

## 1. Motivation

AI Scientist 可以快速生成大量 research proposals，但实验预算有限，因此第一道关卡是：

> 在真正运行昂贵实验之前，模型能否判断一个 proposal 在方法学上是否 sound？

SoundnessBench 专门测这一点，而不是完整论文 acceptance。

## 2. Task boundary

数据集由 1,099 个 machine-learning research proposals 构成，从 ICLR submissions 重建，并使用 reviewer soundness sub-scores 形成标签。

最重要的边界：

**它测试 recoverable proposal-stage methodological soundness，不等于预测完整论文审稿结果，也不等于判断普遍意义上的“科学真理”。**

## 3. Reconstruction

论文不是简单截取 abstract，而是重建 proposal，使 evaluator 在没有最终实验结果的条件下判断研究设计。

这使任务更接近 AI Scientist 在“是否值得执行”阶段面对的问题。

## 4. Main result：optimism bias

12 个 frontier LLM 在标准 prompting 下普遍存在 optimism bias：大量 low-soundness proposals 被判断为 sound。

把 prompt 写得更严格并没有真正解决问题，而主要会把错误从 false positive 推向 false negative。

## 5. 为什么 confusion matrix 比 accuracy 更重要

在 first-gate critic 中，两类错误含义不同：

- **False positive**：坏 idea 被放行，浪费实验预算，甚至进入错误研究链。
- **False negative**：好 idea 被拒绝，可能错失发现。

因此阈值选择本身就是 research policy。

## 6. Controls

论文还检查 public-corpus contamination、paper-identifying phrases、surface features 与 human audit quality 等潜在混杂因素，说明观察到的问题不能简单归因于单一 confounder。

## 7. 对 AI Scientist 的含义

```text
Idea Generator
      ↓
Critic  ← SoundnessBench 暴露这里仍不可靠
      ↓
Experiment
      ↓
Evidence
```

所以仅靠“让 LLM 更严格地反思”不够。更可靠的 Critic 应尽量把抽象判断转成可验证步骤：

**evidence collection → falsifiability check → minimal change → controlled experiment → objective metric → validation → keep/reject**

## 8. 与当前研究地图连接

SoundnessBench 连接了：
- idea selection；
- LLM-as-a-Judge；
- evaluation protocol；
- failure attribution；
- compute allocation。

它说明 autonomous research 的瓶颈不只在 generator，也在**是否知道哪些 idea 不该继续**。
