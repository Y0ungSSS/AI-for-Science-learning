# Reliability & Verification

Scientific Agent 的可靠性至少有两层：

**Execution reliability**：工具是否成功、代码是否跑通、数据是否读错。

**Epistemic reliability**：即使代码跑通，科学结论是否真的被证据支持。

第二层更难，因为系统可能生成一套看似完整、内部一致但无法验证的研究叙事。

## Failure Attribution

```text
Question → Retrieval → Evidence → Hypothesis → Plan
→ Tool / Code → Experiment → Analysis → Interpretation → Evaluation
```

若最终只有一个 reward，系统不知道应该改哪一步。Failure attribution 要定位真正导致失败的环节。

## Verification Gap

可运行代码并不自动提供 novelty verification、完整执行轨迹、数据来源、随机性记录、结果选择过程或对科学 claim 的外部验证。因此 reliability 与 provenance 必须和自动化程度一起评价。

## Provenance

```text
Claim
├─ Result R3
│  ├─ Experiment E2
│  │  ├─ code C7
│  │  ├─ dataset D1
│  │  └─ parameters P2
│  └─ analysis A4
└─ Literature L2/L5
```

目标是能够回答：“这个结论究竟为什么成立？”
