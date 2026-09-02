---
name: categorical-data
description: Analyse binary and categorical outcomes — proportions, chi-squared, Fisher's exact, risk difference/ratio/odds ratio, Simpson's paradox. Use whenever the user has counts, 2x2 tables, percentages by group, or risk comparisons. Apply even if they only share a contingency table.
compatibility: Count tables; GLM skill for regression on binaries.
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 08-categorical-data
---

# Categorical Data

## Mission

Counts deserve a risk measure that matches the question. Odds ratios are not risk ratios. Chi-squared is not an effect size. Aggregation can reverse a sign (Simpson).

## Core output

A **Categorical Analysis**: table grain, measure (RD, RR, OR), interval, test, stratification if confounding is in play.

## Phase 1 — Measures

For a binary outcome in two groups:

- **Risk difference:** p1−p0 (absolute, decision-friendly)
- **Risk ratio:** p1/p0
- **Odds ratio:** odds1/odds0 (logistic, case-control; not "times as likely")

Pick RD when the question is "how many extra events." Pick RR for relative risk when baseline is clear. Pick OR when the design or model requires it, and do not translate "OR=2" as "twice as likely."

## Phase 2 — Tests and small counts

- one-sample proportion vs a value (Wilson interval preferred near 0/1)
- two-sample proportions
- chi-squared for independence in larger tables; expected counts too small → exact or Monte Carlo
- Fisher's exact: valid under its sampling model; not magic for tiny observational tables

Chi-squared significance with a tiny RD in a huge n is still a tiny RD.

## Phase 3 — Simpson and stratification

A crude table can reverse the stratified association. If a third variable (age, severity, site) is a confounder, show stratified tables or a regression (GLM skill). Do not average incompatible tables.

## Phase 4 — Workflow

1. Write the 2×2 or r×c with clear row/column meaning.
2. Choose RD/RR/OR.
3. Interval + test.
4. Stratify if a confounder is named.
5. No "likelihood" language for ORs.

## Anti-patterns

- OR as RR
- Percentages without bases
- Chi-squared as a measure of strength
- Ignoring expected-count warnings
- Causal verbs on a table

## Validation gate

Measure named correctly; bases shown; small-count method if needed; Simpson considered if a third variable exists.

## Final principle

A table is a comparison of risks. Name the risk measure, or you have only a star from a chi-squared test.
