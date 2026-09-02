---
name: communication-dashboards-decision-products
description: Turn analysis into decision products — analytical writing, honest charts, uncertainty language, and dashboards that answer recurring questions. Use whenever the user needs a briefing, slide, dashboard, or stakeholder summary of data-science work. Apply even if they ask to "make it pretty" or "just give the takeaways."
compatibility: Documents, slides, and lightweight dashboards; no specific BI tool required.
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 12-communication-dashboards-decision-products
---

# Communication, Dashboards, and Decision Products

## Mission

The product is a decision improved or a claim understood, not a gallery of charts. Lead with the answer, the uncertainty, and the action. Put method where a skeptic can find it.

## When this skill governs

Use when writing up results, building a dashboard, or translating a model/EDA into something a non-specialist will use.

## Core output

Deliver a **Decision Product**:

1. Audience and decision
2. Answer in the first paragraph
3. One primary exhibit
4. Uncertainty and limitations
5. What to do next
6. Appendix method

## Phase 1 — Audience

Executives: decision, magnitude, risk, next action.  
Researchers: claim, design, robustness.  
Operators: who/what/when list they can act on today.

Do not send the same notebook to all three.

## Phase 2 — Writing

- first sentence answers the question
- numbers with denominators, periods, and comparators
- verbs that match claim class (predict / associate / cause)
- no "interesting insights" without a so-what
- limitations as operating instructions, not apologies

Bad: "Churn is driven by complaints."  
Good: "Users with ≥2 tickets in week 1 are 3.1× more likely to churn by day 90 than users with none (holdout, n=…). This ranks targeting; it does not say that cutting tickets would cut churn."

## Phase 3 — Exhibits

One claim per figure. Title as a sentence. Source and vintage in the footer. See EDA skill for chart types.

Dashboards: a dashboard is a recurring question, not a dumping ground.

- each tile answers a named question
- default filters match the decision's population
- comparators (target, last period, baseline)
- freshness timestamp
- do not put every slice on page 1

If a dashboard cannot change an action this week, it is a museum.

## Phase 4 — Research workflow

1. Name the decision and audience.
2. Write the answer without a chart.
3. Add the one exhibit that earns that sentence.
4. Add uncertainty.
5. Appendix the method.
6. Cut.

## Anti-patterns

- Mystery-plot slide decks
- Dual-axis drama
- Dashboards with 40 filters and no default question
- Causal verbs in a prediction brief
- Method dumped in the first slide
- "Data shows" without a number
- Delivering the notebook as the product

## Decision heuristic

1. Who decides what?
2. What must they believe after one minute?
3. Which single exhibit?
4. What must they not over-read?
5. What do they do on Monday?

## Validation gate

- Answer first
- Claim-class verbs
- One primary exhibit
- Vintage/source on figures
- Dashboard tiles mapped to questions
- Limitations operational

## Final principle

Communication is part of the analysis. If the reader cannot use it, the metric never left the disk.
