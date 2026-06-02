---
name: ic-memo-synthesizer
description: Synthesize primary-market diligence findings into an investment committee memo or decision note for Chinese technology investments, combining thesis, evidence, commercial validation, technical defensibility, risks, valuation, deal terms, open questions, and a clear recommendation. Use after diligence materials, interview minutes, evidence trackers, financials, or project-judgment notes are available and the user needs IC-ready output.
---

# IC Memo Synthesizer

## Objective

Turn diligence evidence into a decision-quality investment memo. The memo should make the investment case testable, show the evidence behind each claim, and state the recommendation clearly.

This skill complements `primary-market-project-judgment`: use that skill for analytical judgment; use this one to assemble an IC-facing memo from multiple diligence inputs.

## Default Output

Use this structure unless the user provides a firm template:

```text
【项目名称】投决备忘录

## 1. 投资建议

## 2. 项目概况

## 3. 投资亮点

## 4. 核心证据

## 5. 关键风险与反方观点

## 6. 估值、融资方案与回报测算

## 7. 尽调完成度与待决事项

## 8. 投后跟踪指标

## 9. 投委会需决策事项
```

## Recommendation Standard

The recommendation must be one of:

- `建议推进`
- `有条件推进`
- `暂缓`
- `建议放弃`

Name the condition if the answer is `有条件推进` or `暂缓`. Example: `有条件推进，前提是两家核心客户验证采购预算和技术替代成本成立`.

## Workflow

1. Inventory the available materials and identify source quality.
2. Extract the investment thesis in one paragraph.
3. Tie each investment highlight to evidence. Do not list highlights that only come from BP slogans.
4. Build the risk section from the strongest opposing case, not from generic risk language.
5. Separate:
   - What has been verified
   - What is plausible but unverified
   - What would kill or materially reprice the deal
6. For valuation and return, state assumptions clearly. If numbers are missing, write the needed inputs rather than inventing a model.
7. End with specific decisions required from IC: proceed, authorize further diligence, approve term sheet, reject, or revisit after milestones.

## Evidence Discipline

Every important claim should carry one of these tags:

- `证据充分`
- `证据一般`
- `待核验`
- `存在矛盾`

Use tags sparingly but visibly on decisive claims.

## Style

Write in Chinese. Use professional investment memo language, but keep the conclusion sharp. Avoid decorative phrasing and avoid hiding uncertainty.
