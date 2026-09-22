# Critic：从“说这个想法不好”到可执行验证

## 1. Critic 的两种含义

### Language Critic
阅读 idea / plan 后给出自然语言批评。

### Evidence-grounded Critic
把怀疑转成可以执行、可以证伪的检查。

后者更接近科研。

## 2. 一个更可靠的 Critic loop

```text
Claim / Hypothesis
      ↓
Collect evidence
      ↓
Find falsifiable assumption
      ↓
Design minimal intervention
      ↓
Controlled experiment
      ↓
Objective metric
      ↓
Validate
      ↓
Keep / Modify / Reject
```

这里的“minimal”很重要：一次修改太多东西，就无法知道为什么结果变化。

## 3. 为什么纯 verbal self-critique 不够

LLM 可以生成听起来合理的 critique，但 critique 本身仍是模型输出，没有增加外部证据。

真正可靠的 critic 应尽可能调用：
- code execution；
- unit / property tests；
- data checks；
- simulation；
- literature evidence；
- independent evaluator；
- repeated experiments。

## 4. Optimistic critic

SoundnessBench 显示模型在 proposal-stage judgment 中容易过度乐观。简单增加“be strict”提示主要改变决策阈值，而没有获得新的验证能力。

因此更值得研究的方向是：

**让 critic 获得新的 evidence，而不是只要求它“想得更认真”。**

## 5. 与 Failure Attribution 的关系

Critic 判断“哪里可能有问题”；Failure Attribution 判断“已经观察到的失败由什么导致”。

二者结合后才形成：

```text
predict failure → test → observe failure → locate cause → revise
```
