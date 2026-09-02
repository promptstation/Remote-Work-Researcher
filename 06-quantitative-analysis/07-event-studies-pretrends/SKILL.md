---
name: event-studies-pretrends
description: Design and read event-study plots as credibility checks — leads as placebos, dynamic effects, binning. Use whenever a panel design needs dynamics or pre-trend evidence. Apply even if the user only reports a single post dummy.
compatibility: Event-study regression plots.
metadata:
  author: Promptstation
  version: 1.0.0
  category: quantitative-analysis
  course: 06-quantitative-analysis
  section: 07-event-studies-pretrends
---

# Event Studies and Pre-trends

## Mission

An event study shows how Y moves around treatment time relative to a baseline period. Leads should be near zero if parallel trends hold. Lags tell dynamics. A single post coefficient hides both.

## Core output

An **Event-Study Read**: omitted period, leads/lags, pre-trend judgment, dynamic pattern, robustness to binning.

## Phase 1 — Construction

Omit a clean pre-period. Do not omit the last pre if it is already contaminated. Align calendar time vs event time on purpose. For staggered designs, use estimators that do not contaminate pre-period with already-treated units.

## Phase 2 — Reading

Pre-trends: magnitude matters, not only stars. A noisy pre-period does not bless the design. Post: delayed effects vs immediate vs fade.

## Phase 3 — Workflow

Always pair DiD/FE policy papers with an event-study figure. If you cannot plot it, say why.

## Anti-patterns

- No figure
- Using already-treated as controls in event time
- "Pre-trends pass" because p>0.05 on a noisy lead

## Validation gate

Figure described; omitted period named; pre-period judgment about magnitude.

## Final principle

If the leads are a mess, the lag is not a finding. It is a continuation.
