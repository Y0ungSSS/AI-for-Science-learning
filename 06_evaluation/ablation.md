# Ablation：为什么“有效”还不够？

## 1. 基本问题

完整系统性能提高，只能说明：

> 整套系统在当前实验设置下表现更好。

它不能说明提升来自哪个组件。

Ablation（消融实验）通过删除、替换或固定某个组件来建立更清晰的因果证据。

## 2. 最简单形式

假设系统：

```text
RAG + Planning + Tree Search + Critic
→ Score 80
```

做：

```text
without RAG         → 73
without Planning    → 62
without Tree Search → 78
without Critic      → 69
```

这能帮助判断组件贡献，但不能机械地把差值理解成完全独立贡献，因为组件之间可能 interaction。

## 3. AI Scientist 中尤其需要 ablation 的地方

- multi-agent 是否真的优于 single-agent；
- tree search 是否优于增加相同 token budget 的普通 sampling；
- external literature 是否带来真正方法改进；
- critic 是否提高 correctness，还是只让输出更保守；
- memory 是否减少重复失败；
- strategy switching 是否优于简单增加实验次数。

## 4. 最需要强调的点

### 控制预算
如果“有 tree search”运行 100 次实验，而 baseline 只运行 10 次，那么性能提升可能来自额外 compute。

### 一次只改变关键变量
否则无法知道究竟是什么造成差异。

### 报告 variance
Agent 与 LLM 有随机性，单次运行不足以支撑稳定结论。

### Negative ablation 也有价值
一个看起来很复杂的组件删掉后性能几乎不变，说明系统可能被过度设计。

## 5. 与科研思维的关系

Ablation 本质上是在问：

**“我声称这个设计重要，有什么实验能排除其他解释？”**

这比记住“消融=删模块”重要得多。
