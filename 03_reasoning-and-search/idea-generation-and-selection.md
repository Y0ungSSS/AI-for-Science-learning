# Idea Generation → Evaluation → Selection

AI Scientist 的第一步并不是“想到越多 idea 越好”。真正的问题是如何从大量候选中识别**值得花实验预算验证的研究方向**。

## 1. 基本结构

```text
Generate hypotheses
      ↓
Critique / compare
      ↓
Rank / select
      ↓
Experiment
      ↓
Evidence
      ↓
Update hypothesis
```

如果 selection 不可靠，后面即使代码、实验和写作都完全自动化，也只是在高效验证低质量想法。

## 2. Pairwise comparison（两两比较）

相比一次给十个方案分别打绝对分，让 evaluator 比较 A 与 B 哪个更值得继续，有时更容易获得稳定相对判断。

但 pairwise comparison 会带来 O(n²) 的比较成本，因此需要 tournament / ranking 机制减少比较数量。

## 3. Swiss tournament（瑞士轮）

Swiss tournament 的思想是让表现相近的候选持续配对，而不是做所有 pairwise comparisons。

在 hypothesis ranking 中可以理解为：

```text
Round 1: random / seeded pairs
Round 2: similar-score pairs
Round 3: similar-score pairs
...
→ ranking
```

它解决的是**可扩展排序**，不是 scientific correctness 本身。

## 4. Cross-model review（跨模型评审）

使用不同模型家族/配置分别评价候选，希望减少单一 evaluator 的系统性偏差。

关键问题不是“模型数量越多越好”，而是：
- evaluator 是否真的独立；
- agreement 是否意味着正确；
- disagreement 如何处理；
- evaluator 是否共享相同知识盲区。

## 5. LLM-as-a-Judge

LLM judge 可以评价 novelty、clarity、plausibility、methodology 等开放属性，因此很适合无法用 accuracy 直接打分的研究 idea。

但必须区分：

```text
Looks plausible
≠ Methodologically sound
≠ Experimentally supported
≠ Scientifically novel
```

这正是后续 SoundnessBench 与 Verification Gap 出现的原因。

## 6. 与 strategy switching 的关系

Idea selection 发生在“选择研究路线”时；strategy switching 发生在“路线已经执行了一段时间”之后。

二者共同组成：

**生成路线 → 选择路线 → 执行 → 监测 → 判断失败 → 切换路线。**
