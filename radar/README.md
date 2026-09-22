# Paper Radar

Radar 是候选区，不是所有新论文都进入正式研究地图。

## A / B / C

**A：进入研究地图。** 新研究问题、关键新机制、新 evaluation protocol / benchmark、新真实科学闭环，或对已有结论的重要修正。

**B：留在 Radar。** 有参考价值，但主要是已有机制的新组合、领域应用或增量改进。

**C：Deferred / Rejected。** 普通“LLM + RAG + multi-agent + tool use”组合，缺少新的科学问题、机制或可信评测，或与已有节点高度重复。

## 定时任务流程

```text
过去 24–72h 广搜 → 去重 → A/B/C
→ 映射 research node → 与已有工作比较
→ A 更新主题与 Open Problems
→ B 写入当月 Radar
→ C 记录淘汰原因
```

更稳妥的写入方式：自动任务创建 `bot/radar-YYYY-MM-DD` 分支并提交 PR，经检查后合并到 main，避免低质量候选污染稳定知识地图。

每篇候选最少记录 title/date/venue、problem、mechanism、evaluation、related node、difference、A/B/C 与 reason。
