---
name: nonparametric-rank-methods
description: Test or estimate without a normal sampling model — sign and rank tests, permutation tests, empirical CDFs. Use whenever normality is implausible, n is small and skewed, the user wants Wilcoxon/Mann-Whitney, or asks for a distribution-free test. Apply even if they want to "just use a t-test anyway."
compatibility: Rank and permutation procedures.
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 11-nonparametric-rank-methods
---

# Nonparametric and Rank Methods

## Mission

When the sampling model of the mean is a bad story, change the estimand or the reference distribution. Rank tests answer questions about stochastic dominance or medians (under extra assumptions), not secretly the same question as a t-test.

## Core output

A **Nonparametric Note**: estimand (median, P(X>Y), CDF), method, result, what was not assumed, what is still assumed (iid, etc.).

## Phase 1 — When to leave the t-world

- small n, strong skew, ordinal data, outliers that are real
- interest in medians or whole distributions, not means

Not reasons: "nonparametric is safer so always." Rank tests have assumptions (independence, similar shapes for location interpretations) and different estimands.

## Phase 2 — Tools

- sign test / Wilcoxon signed-rank: paired
- Mann–Whitney / Wilcoxon rank-sum: two samples; estimand is P(X>Y) unless you assume equal shapes then a location shift
- Kruskal–Wallis: k groups
- permutation test: any statistic; independence of assignment/sample
- ECDF / KS: distribution difference, sensitive in ways you should state

Permutation is often the most honest "distribution-free" test of a sharp null of exchangeability.

## Phase 3 — Workflow

1. Name the estimand you actually want.
2. If it is the mean and n is large, t/CLT may still win.
3. If ordinal or skewed small-n, rank or permutation.
4. Report effect on a matching scale (median difference, probability of superiority).
5. Independence still required.

## Anti-patterns

- Wilcoxon as "t-test without assumptions"
- Ignoring ties
- Treating KS p as a full distributional description
- Using ranks then interpreting as means

## Validation gate

Estimand named; method matches; independence stated; effect on a nonparametric scale.

## Final principle

Distribution-free is not assumption-free. It is a different estimand with a different reference distribution. Name both.
