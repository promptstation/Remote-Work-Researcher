---
name: comparing-groups-means
description: Compare group means or paired differences with effect sizes and checked assumptions — t-tests, paired designs, ANOVA, robust alternatives. Use whenever the user compares averages across groups, A vs B means, before-after, or "is the difference real." Apply even if they only paste two column means.
compatibility: t/ANOVA or robust/permutation analogues.
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 07-comparing-groups-means
---

# Comparing Groups and Means

## Mission

A mean comparison is an effect plus uncertainty, not a t-star. Check whether the design is paired, independent, or clustered; whether variance is equal; and whether the mean is even the right location measure.

## Core output

A **Group Comparison**: design, estimand (difference in means), effect size, interval, test, assumption checks, alternative if assumptions fail.

## Phase 1 — Design

- independent samples vs paired/blocked
- randomised vs observational (causal claim needs Course 6)
- unit of analysis = unit of randomisation/sampling (no people-level test on cluster-level treatment without accounting for it)

Paired when the same unit (or matched pair) contributes two measurements. Pairing is not "two columns in Excel."

## Phase 2 — Tests

- one-sample t vs a value
- two-sample t (Welch default unless equal-variance is justified)
- paired t on differences
- ANOVA for >2 groups, with a planned contrast or a multiplicity plan — not a fishing expedition of pairwise tests

Report the difference in original units and a standardised effect if audiences need it (and say which standardisation).

## Phase 3 — Assumptions

t-procedures: iid (or independent groups), finite variance; normality of the sampling distribution of the mean (safer with n large and mild skew; bad with small n and heavy tails or outliers).

If broken: Welch, permutation, bootstrap, or rank methods (nonparametric skill). Do not delete outliers to save a t-test.

Unequal n plus unequal variance: Welch, not pooled.

## Phase 4 — Workflow

1. Design and estimand.
2. Plot distributions (not only means).
3. Choose paired vs independent, Welch vs other.
4. Effect + interval + p.
5. If ANOVA, planned comparisons.

## Anti-patterns

- Multiple t-tests among k groups with no multiplicity plan
- Paired data analysed as independent (or vice versa)
- Mean of Likert-as-interval without comment when the question is about tails
- Causal language on observational group differences
- Pooled t as default

## Validation gate

Design named; Welch/paired choice justified; distributions inspected; effect in original units.

## Final principle

Compare groups as a design plus an estimand. The t-test is optional machinery, not the question.
