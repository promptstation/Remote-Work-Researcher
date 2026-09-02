---
name: variance-estimation-complex-samples
description: Estimate sampling variance under the actual design — strata, clusters, replication. Use whenever survey estimates need SEs or CIs. Apply even if the user used naive software defaults.
compatibility: Survey packages (svy, survey); replication weights.
metadata:
  author: Promptstation
  version: 1.0.0
  category: survey-methodology
  course: 07-survey-methodology
  section: 10-variance-estimation-complex-samples
---

# Variance Estimation for Complex Samples

## Mission

Clustered samples have fewer independent bits than n. Stratification can cut variance. Software that thinks you have n iid rows will overstate precision. Use the design: strata, PSU, weights.

## Core output

A **Variance Spec**: strata, PSU, method (Taylor / BRR / jackknife / bootstrap), deff, CI.

## Phase 1 — Structure

Need: stratum ID, PSU ID, weight. Without PSU, you cannot get design-based SEs. Masked public-use files sometimes provide replicate weights — use those.

## Phase 2 — Methods

Linearisation (Taylor) default for many totals. Replication when the statistic is messy or for disclosure-limited files. Finite population correction only when sampling fractions are large.

## Phase 3 — Workflow

1. Declare design in software.
2. Estimate.
3. Report deff.
4. If deff≈1 on a clustered sample, suspect a declaration error.

## Anti-patterns

- iid SEs
- Clustering at person level
- Ignoring strata
- Tiny SEs on 30 PSUs presented as national precision

## Validation gate

PSU+stratum or replicates; deff; no iid default.

## Final principle

Precision is a design property. If the analysis ignores the design, the CI is about a different survey.
