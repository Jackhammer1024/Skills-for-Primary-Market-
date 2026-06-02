---
name: diligence-evidence-tracker
description: Convert primary-market diligence notes, interview memos, data-room materials, management claims, expert calls, and financial snippets into an evidence tracker that separates facts, claims, risks, contradictions, unresolved questions, required follow-ups, and decision impact. Use during ongoing diligence when the user wants to maintain a living fact base and avoid losing key issues across materials.
---

# Diligence Evidence Tracker

## Objective

Maintain a live diligence evidence base. The goal is not to summarize everything; it is to preserve what matters for the investment decision, expose contradictions, and keep follow-up actions clear.

Use this skill after reading transcripts, meeting notes, BP pages, financials, contracts, technical reports, customer feedback, or prior memos.

## Default Output

Use Markdown tables unless the user asks for Excel.

```text
【项目名称】尽调证据台账

## 1. 投资命题状态

## 2. 关键事实表

| 模块 | 事实/主张 | 证据来源 | 可信度 | 对投资判断的影响 | 待核验动作 |

## 3. 矛盾与异常

| 编号 | 矛盾点 | 涉及来源 | 可能解释 | 需要追问 |

## 4. 风险台账

| 风险 | 触发条件 | 严重程度 | 当前证据 | 缓释/验证方式 |

## 5. 下一步尽调动作

| 优先级 | 动作 | 目标 | 负责人/对象 | 截止时间 |
```

## Evidence Classification

Classify each important item:

- `已证实`: supported by source documents or multiple independent confirmations.
- `较可信`: plausible and supported by one credible source, but still needs confirmation.
- `待核验`: important but currently only from management/BP/verbal claim.
- `矛盾`: inconsistent with another source or with industry logic.
- `高风险`: could materially change the investment conclusion.

## Workflow

1. Extract only decision-relevant information. Ignore greetings, generic industry background, and repeated claims unless repetition changes confidence.
2. Map facts to diligence modules:
   - Product and technology
   - Market and demand
   - Customers and revenue
   - Competition and substitution
   - Team and governance
   - Financials and valuation
   - Legal, IP, compliance, and policy
3. For every strong claim, ask: `What evidence would make this real?`
4. For every contradiction, list the exact sources if available and propose a follow-up question.
5. Keep `待核验动作` concrete: request a file, ask a named question, call a customer, compare a competitor, or check public data.

## Source Notes

When source names are available, cite them in concise form such as `BP p.12`, `管理层访谈 2026-05-18`, `专家A`, `合同扫描件`, or filename. If the source is unknown, write `来源未标明`.

## Style

Write in Chinese. Be skeptical but fair. Do not over-conclude from weak evidence. Make the unresolved questions impossible to miss.
