# LLM-as-a-Judge / Cross-model Review

## 1. 为什么 AI Scientist 需要 Judge

科研输出通常没有唯一标准答案。idea、proposal、analysis 和 paper 需要评价 novelty、rigor、clarity、significance 等开放属性，因此自然会使用 LLM evaluator。

## 2. Judge 的三种典型用途

**Absolute scoring**：单个候选按 rubric 打分。

**Pairwise comparison**：比较 A/B。

**Tournament / ensemble**：多轮比较或多个 evaluator 汇总。

## 3. Cross-model review

让不同模型参与评价可以减少对单一模型的依赖，但不能假设“多数票 = 真理”。

必须测：
- inter-rater agreement；
- 与 human expert 的一致性；
- 不同模型家族的系统偏差；
- prompt sensitivity；
- position/order bias；
- 是否偏好自己模型生成的文本。

## 4. 最危险的混淆

LLM 很擅长判断“像不像一篇合理研究”，但 scientific evaluation 还需要：

```text
proposal plausibility
        ↓
methodological soundness
        ↓
execution correctness
        ↓
evidence supports claim
        ↓
novelty
        ↓
scientific significance
```

每一层都不是下一层的充分条件。

## 5. 因此怎么用

LLM judge 更适合：
- 大规模初筛；
- 生成 critique；
- 比较候选；
- 辅助专家。

如果把它作为唯一 scientific gate，就必须专门验证 judge 本身。
