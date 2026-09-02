---
name: dependence-clustering-hierarchical
description: Recognise dependent data and replace naive iid SEs with clustered or hierarchical uncertainty. Use whenever observations are nested (students in schools, months in people, patients in clinics), repeated measures, or the user treated clustered data as iid. Apply even if software printed tiny p-values.
compatibility: Cluster-robust SEs, mixed models, GEE-style thinking.
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 15-dependence-clustering-hierarchical
---

# Dependence, Clustering, and Hierarchical Models

## Mission

iid standard errors assume independent leftovers. Nested and repeated data violate that. The effective sample size is closer to the number of independent clusters than to the number of rows. Naive p-values will look exciting.

## Core output

A **Dependence Note**: clustering unit, why dependence exists, method (cluster SEs, mixed model, aggregate to cluster), effective n.

## Phase 1 — Find the independent piece

Ask: which units could be reshuffled without breaking the design? Schools, firms, people, villages, time-series blocks.

Rows of a panel are not independent draws of a country's economy.

## Phase 2 — Tools

- **Aggregate** to the cluster when the estimand is cluster-level and n_clusters is small
- **Cluster-robust SEs:** keep rows, correct variance; need enough clusters
- **Hierarchical / random-effects models:** partial pooling, variance components; still need care on the number of groups
- **GEE:** population-average effects with working correlation

Do not add a random intercept and keep talking as if n = N_rows.

Design effect: ICC and cluster size inflate variance of means. Even a description of a school survey needs this (Course 7 will go deeper on survey design effects).

## Phase 3 — Small number of clusters

10 clusters with cluster SEs is a shaky ritual. Use caution, wild cluster bootstrap, or aggregate. Do not pretend.

## Phase 4 — Workflow

1. Name the clustering unit.
2. Report n_clusters, not only n_rows.
3. Choose cluster SE vs mixed model vs aggregate.
4. Recompute inference; expect SEs to rise.
5. If they do not rise, explain why (ICC≈0, or a bug).

## Anti-patterns

- People-level tests of school-level treatments with iid SEs
- Mixed models as a magic independence eraser
- Clustering at the wrong level (too fine)
- Huge n in the abstract of a 20-country panel

## Validation gate

Cluster unit named; n_clusters reported; method named; iid SEs not used when dependence is material.

## Final principle

The sample size that matters is the number of independent pieces. Count those, then infer.
