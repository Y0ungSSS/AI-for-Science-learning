# Verification Gap：会做研究 ≠ 能证明研究做对了

## 1. 问题来源

AI Scientist 的生成能力发展很快：idea、代码、实验、分析、论文都可以自动产生。

但验证这些产物仍然困难。

这形成一个不对称：

```text
Generation capability  ↑↑↑
Verification capability  ↑
```

## 2. 什么叫可验证

一个 reviewer 想检查 Agent 的 claim，至少可能需要：
- code；
- data；
- environment；
- random seeds；
- execution traces；
- experiment selection history；
- failed attempts；
- literature provenance；
- claim ↔ evidence mapping。

只有最终 PDF 并不足够。

## 3. 为什么这对 autonomous research 更严重

人类论文已经存在 reproducibility crisis；Agent 可以更快地产生更多实验和论文，如果 verification 不同步提高，就会放大审核压力。

## 4. Verification 与 Evaluation 的区别

**Evaluation**：这个 Agent/产物表现如何？

**Verification**：这个具体 scientific claim 为什么可以相信？

一个系统 benchmark 分数很高，也可能产生某个无法验证的 claim。

## 5. 研究机会

- execution trace standardization；
- claim-level provenance；
- automated replication；
- artifact completeness checks；
- evidence graphs；
- independent verifier agents；
- verifier-generator separation。

这条线与 Agent observability 有概念交叉，但这里关注的是**科学证据链**而不是系统安全监控。
