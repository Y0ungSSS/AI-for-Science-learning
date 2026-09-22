# Google AI Co-Scientist：Hypothesis Generation 与 Selection

- **Status**: 🟡🔵
- **Node**: Scientific Agents / Idea Generation / Evaluation

## 1. 定位

AI Co-Scientist 的重点不是完全替代科学家，而是作为 virtual scientific collaborator 帮助生成和改进 novel hypotheses / research proposals。

## 2. 为什么值得学

它把“生成 idea”从单次 prompt 变成一个搜索与评价过程：

```text
Generate
→ Critique
→ Compare
→ Rank
→ Improve
→ repeat
```

其中 pairwise comparison、tournament-style ranking 和多 Agent 角色让候选 ideas 可以持续演化。

## 3. 与 The AI Scientist 的差别

The AI Scientist 更强调 **idea → code → experiment → paper** 的端到端执行。

Co-Scientist 更强调 **idea/hypothesis space 的生成、比较和优化**。

所以二者不是简单的“谁更强”，而是自动化科研链上的重点不同。

## 4. 最关键的研究缺口

执行前 evaluator 认为一个 hypothesis 很好，并不能保证实际实验成功。

因此存在：

```text
pre-execution judgment
        ↕ gap
post-execution evidence
```

这个 gap 后续自然连接到 SoundnessBench、Critic、Evaluation Protocol 与 Closed-loop Discovery。

## 5. 应学到什么

Co-Scientist 最值得迁入知识图的不是“多 Agent”，而是：

**科学 idea 也可以被组织成一个生成—竞争—筛选—改进的 search process。**
