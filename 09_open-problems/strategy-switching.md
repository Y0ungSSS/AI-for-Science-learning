# OP-01 深入：Strategy Switching / Meta-reasoning

## 1. 从“耐心”问题开始

人做研究时，连续几次改进有限后可能会想：

> 是不是不该继续改 A，而应该试 B 或 C？

这不是简单的“多采样几个答案”，而是对当前搜索过程本身进行判断。

## 2. 五层问题

```text
Outcome monitoring
      ↓
Plateau detection
      ↓
Failure attribution
      ↓
Strategy selection
      ↓
Budget allocation / stopping
```

### Outcome monitoring
记录实验到底发生了什么。

### Plateau detection
判断当前路线的边际收益是否已经很低。

### Failure attribution
判断为什么低：想法错、实现错、数据错、指标错，还是优化不足。

### Strategy selection
决定局部修改、回退、换方法族、补充证据或改变 hypothesis。

### Budget allocation
新路线也有成本，因此还要决定探索多久以及什么时候停止。

## 3. Tree search 与真正 strategy switching 的区别

Tree search 解决“保留多个候选并能回退”。

Strategy switching 更进一步解决：

**为什么离开当前路线，以及应该跳到哪一类路线。**

因此“树更大”不一定代表 meta-reasoning 更强。

## 4. 一个未来可实验化的方向

构造包含多种 failure mode 的 scientific coding benchmark，并记录 Agent 的完整轨迹。评价不只看最终分数，还看：

- 是否正确识别失败类型；
- 是否在合理时间停止无效优化；
- 是否选择合适的新策略；
- 切换带来的收益是否超过额外预算；
- 是否能解释切换依据。

这样“耐心/换思路”就从模糊直觉变成可测量研究问题。
