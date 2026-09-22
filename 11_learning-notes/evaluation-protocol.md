# 学习笔记：Evaluation Protocol

这是一个需要长期保留并迁移到其他科研项目的方法论。

## 不要只问“指标是什么”

真正公平的实验比较必须同时控制：

- 谁能看到什么数据；
- 是否允许互联网/文献搜索；
- 可以调用哪些 tools；
- 可以改哪些代码/参数；
- token / compute / money / time budget；
- 允许尝试多少次；
- 人类能否介入；
- 最终输出怎样执行；
- 用什么 metric / judge；
- 与哪些 baselines 比；
- 是否重复运行并报告 variance。

## 为什么重要

如果实验协议不同，最终分数差异可能来自额外信息、更多计算资源或更多人工帮助，而不是方法本身。

## 以后读论文固定检查

```text
Claim
 ↓
What is controlled?
 ↓
What is changed?
 ↓
What is measured?
 ↓
What alternatives are ruled out?
 ↓
Does evidence support the claim?
```

这也是理解 benchmark、ablation 和 scientific-agent evaluation 的共同底层逻辑。
