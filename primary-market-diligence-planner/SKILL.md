---
name: primary-market-diligence-planner
description: Build a focused diligence workplan for Chinese primary-market technology investments, including issue trees, material request lists, management interview agendas, expert-call questions, competitor checks, customer validation plans, and next-step priorities. Use when the user is preparing diligence for a startup, hard-tech company, quantum/AI/semiconductor/new-energy project, or any private-market deal and needs a practical DD plan rather than an investment conclusion.
---

# Primary Market Diligence Planner

## Objective

Turn messy project context into an executable diligence plan. The plan should reveal what must be proven, which evidence can prove it, who to ask, what materials to request, and what would change the investment view.

Do not write a generic due diligence checklist. Tailor the plan to the company, sector, stage, claimed moat, commercialization path, and current information gaps.

## Default Output

Use this structure unless the user gives another format:

```text
【项目名称】尽调计划

## 1. 当前判断与核心假设

## 2. 尽调主线（Issue Tree）

## 3. 资料清单（按优先级）

## 4. 管理层访谈提纲

## 5. 专家/客户/竞品访谈提纲

## 6. 关键验证动作

## 7. 红旗与放弃条件

## 8. 本周行动表
```

## Workflow

1. Identify the project category: product company, platform, component, equipment, service, solution integrator, research commercialization, or cyclical beneficiary.
2. State the current investment hypothesis in 3-5 bullets. Mark each as `待验证`, `已有弱证据`, or `已有强证据`.
3. Build an issue tree around the real uncertainty:
   - Demand authenticity and urgency
   - Technology maturity and defensibility
   - Product-market fit and customer validation
   - Commercialization path and revenue quality
   - Competitive landscape and substitution risk
   - Team capability and resource dependence
   - Financing need, valuation, and exit logic
4. Convert each issue into evidence requirements, source channels, and concrete questions.
5. Prioritize actions by decision impact and time sensitivity. The first week should focus on disproving the thesis, not polishing the story.

## Question Design

Questions should be pointed and answerable. Avoid soft prompts like `介绍一下行业情况`. Prefer:

- `客户为什么现在必须买，而不是观望一年？`
- `现有替代方案的总拥有成本是多少，项目方案降低的是哪一项成本？`
- `如果头部客户不采购，收入还能从哪里来？`
- `哪个指标一旦不成立，会直接推翻投资逻辑？`

## Evidence Standards

Separate facts, claims, and judgments:

- `事实`: contract, invoice, test report, customer email, audited financial data, patent filing, public tender result.
- `公司主张`: management statement, BP claim, unaudited pipeline, verbal customer feedback.
- `投资判断`: derived conclusion that must cite the supporting facts or clearly state the missing proof.

## Style

Write in Chinese. Be crisp, operational, and investor-facing. Every section should help the user decide what to do next this week.
