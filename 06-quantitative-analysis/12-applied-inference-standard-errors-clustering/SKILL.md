---
name: applied-inference-standard-errors-clustering
description: Choose standard errors that match the design's independent units — cluster at treatment level, few-cluster caution. Use whenever the user reports p-values from a causal design or has clustered data. Apply even if software defaulted to iid or HC1.
compatibility: Cluster-robust, bootstrap; overlaps Course 3 dependence skill but for causal designs.
metadata:
  author: Promptstation
  version: 1.0.0
  category: quantitative-analysis
  course: 06-quantitative-analysis
  section: 12-applied-inference-standard-errors-clustering
---

# Applied Inference: Standard Errors and Clustering

## Mission

Inference is about the randomness in the design. Cluster at the level of assignment or shock. Too few clusters → pretty p-values that lie. The SE is part of the result, not a footnote.

## Core output

An **Inference Choice**: identifying variation's unit, SE method, n at that level, few-cluster plan.

## Phase 1 — Level

If states adopt policy, cluster at state, not person-year. If individuals are randomised, person-level (or the randomisation block). Moulton problem: aggregated treatment, micro Y, iid SEs.

## Phase 2 — Few clusters

<30 treated clusters is a warning. Wild cluster bootstrap, aggregate, or honest uncertainty. Do not pretend.

## Phase 3 — Workflow

1. What is independently shocked?
2. Cluster there.
3. Report n_clusters.
4. If few, change method or language ("we cannot reject at conventional levels under conservative SEs").

## Anti-patterns

- iid SEs on state policy
- Clustering at too-fine a level to shrink SEs
- Stars from 8 clusters

## Validation gate

Cluster unit = design unit; n_clusters reported.

## Final principle

The sample size of a design is the number of independent shocks. Count those before you star.
