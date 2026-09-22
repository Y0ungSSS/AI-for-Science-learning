# Scientific Coding

## 1. 为什么 scientific coding 是 AI4S 的重要切入口

许多科学研究最终必须落到可执行软件：数据预处理、模型、模拟、统计分析和可视化。代码因此成为“研究想法”和“可测量证据”之间的桥。

它还有一个优势：相较真实湿实验，计算实验更容易自动执行、重复和评价，非常适合研究 AI Scientist。

## 2. ERA：从 code generation 到 empirical research search

普通 code generation 的问题通常是“根据 specification 写出正确代码”。ERA 更接近科研：

```text
Research ideas
      ↓
LLM proposes program
      ↓
Execute in sandbox
      ↓
Objective score
      ↓
Tree search / mutation
      ↓
better empirical method
```

系统不仅生成代码，还围绕可量化 scientific objective 搜索更好的方法，并可从论文、教材等外部来源吸收研究思想。

## 3. 为什么 tree search 有意义

如果只保留当前最好程序并不断修改，搜索容易局限在一个局部路线。保留候选树允许系统回到较早节点并探索其他分支。

但它也留下一个更深的问题：

> “换一个候选分支”是否等于“理解当前研究策略为什么失败”？

答案并不必然成立。这正是 ERA 与 Strategy Switching / Failure Attribution 主线的连接点。

## 4. Scientific coding 的评测优势

计算环境允许：
- 自动执行；
- objective metric；
- 重复实验；
- 保存完整代码；
- 控制随机种子；
- 比较 baseline；
- 做 ablation；
- 记录轨迹。

因此它是研究 evaluation protocol、research state 和 autonomous experimentation 的理想沙盒。

## 5. 潜在研究路线

与其只研究“代码写得更好”，更值得关注：

**idea → code → experiment → diagnosis → revised idea**

也就是代码如何成为科学推理闭环的一部分。
