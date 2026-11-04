> **历史研究地图（保留原文）**：OP-01–OP-05 是早期探索笔记，不是当前完整分类。最新开放问题和实验以 [问题树 Q1–Q9](../调研/问题树.md) 为准；机制证据见 [研究树 A–I](../调研/研究树.md)。

> **历史研究地图（保留原文）**：本文件的 OP-01–OP-05 是早期探索笔记，不是当前维护的完整问题分类。最新开放问题、饱和度与可证伪实验请以 [问题树 Q1–Q9](../调研/问题树.md) 为准；对应机制证据见 [研究树 A–I](../调研/研究树.md)。下文保留用于追溯思路演化。

# Open Problems / Research Map

这个目录比论文收藏夹更重要。每个问题随新论文持续更新。

## OP-01：AI Scientist 如何知道当前路线不值得继续？
已有 iterative refinement、best-of-N、tree search、evaluator-guided search，但评分停滞并不说明“为什么失败”。需要连接 **plateau detection → failure attribution → strategy switching → meta-reasoning → exploration/exploitation**。

研究问题：能否根据实验轨迹决定继续优化、回退、增加验证、换策略或停止？

## OP-02：如何判断 AI Scientist 是否真的产生科学发现？
benchmark score、LLM judge、human review、rediscovery、real experiment 测的是不同对象。需要分层 protocol：
```text
task completion → correctness → reproducibility
→ claim verification → novelty → scientific significance
```

## OP-03：AI Scientist 如何保存长期 Research State？
聊天上下文不是严格科研记录。需要显式维护 hypotheses、支持/反对证据、experiment state、failed attempts、code/data versions、decision rationale、provenance。

研究问题：怎样的 state representation 能避免重复失败，并支持审计和恢复？

## OP-04：失败后应该改哪一层？
失败可能来自假设、文献、实验设计、代码、数据、分析或 evaluator。目标是把端到端 reward 分解为诊断信号，让 Agent 修改真正故障源。

## OP-05：开放式科研评测如何避免 benchmark gaming？
关注 hidden/dynamic tasks、contamination control、trace-based evaluation、cost-aware evaluation、external verification、longitudinal evaluation。
