# Closed-loop Scientific Discovery

闭环的关键不是模块多，而是后一步产生的证据能够改变前一步的研究决策。

```text
Literature → Hypothesis → Experiment → Observation
→ Analysis → Interpretation → Hypothesis Update ↺
```

如果系统只依次调用检索 Agent、代码 Agent、写作 Agent，但实验结果不会改变假设，它更像 workflow automation，而不是 autonomous discovery。

## Robin

Robin 将文献检索、假设生成、实验设计、真实实验结果分析与后续假设更新连接起来。其关键不只是 multi-agent，而是把**真实实验反馈**放回研究循环。这也说明“autonomous”必须明确：哪些阶段自动化、哪些仍由人类/实验室完成。

## 三类闭环

**Virtual loop**：全部在数据、代码或模拟器中完成，成本低且容易复现。

**Human/lab-in-the-loop**：AI 决定部分步骤，人类执行物理实验并反馈。

**Autonomous lab**：机器人、仪器控制、实验规划和分析高度自动连接。

个人科研起步时，virtual experiment / scientific coding / simulation 更容易形成完整、可重复的闭环。
