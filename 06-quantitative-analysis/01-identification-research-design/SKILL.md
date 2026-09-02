---
name: identification-research-design
description: State an identification strategy before estimation — causal question, ideal experiment, actual design. Use whenever the user wants to know an effect, run a regression "to find impact," or start an empirical paper. Apply even if they already have a coefficient.
compatibility: Applied econometric research.
metadata:
  author: Promptstation
  version: 1.0.0
  category: quantitative-analysis
  course: 06-quantitative-analysis
  section: 01-identification-research-design
---

# Identification and Research Design

## Mission

Identification is the reason a comparison equals an effect. Estimation is how you compute the comparison. Software does the second. You owe the first in writing. No identification paragraph, no causal verb.

## Core output

A **Design Paragraph**: question, estimand, ideal experiment, actual identifying comparison, threats, what will be estimated instead if identification fails.

## Phase 1 — Question

"Effect of D on Y for whom, relative to what alternative." Not "the relationship between."

## Phase 2 — Ideal experiment

Who would you randomise, at what unit, what would the control get? If you cannot describe it, you do not have a causal question.

## Phase 3 — Actual design

RCT, DiD, IV, RDD, unconfoundedness, FE — pick one primary. Mixed salad designs are how papers hide.

Threats: remaining confounding, selection, spillovers, measurement.

## Phase 4 — Workflow

Write the paragraph. Then pick the matching skill. If none fits, the answer is descriptive (Course 2/3).

## Anti-patterns

- Kitchen-sink regression as design
- "We control for" as identification
- Causal verbs on a correlation table

## Validation gate

Ideal experiment named; actual comparison named; threats named.

## Final principle

A coefficient is not a design. The design is the sentence that would still make sense if the coefficient were missing.
