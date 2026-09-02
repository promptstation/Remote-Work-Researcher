---
name: spatial-econometrics-dependence
description: Treat spatial dependence as a design issue — spillovers, spatial lag/error, why iid fails on maps. Use whenever the user runs regressions on regions or wants a spatial lag model. Apply even if they default to iid SEs on counties.
compatibility: Spatial econometric caution; pair with Course 6 inference.
metadata:
  author: Promptstation
  version: 1.0.0
  category: urban-spatial-economics
  course: 10-urban-social-spatial-economics
  section: 12-spatial-econometrics-dependence
---

# Spatial Econometrics and Dependence

## Mission

Nearby units share shocks and outcomes. iid SEs on polygons are often wrong. Spatial lag models are extra structure, not a default upgrade. Spillovers can be the science or the nuisance.

## Core output

A **Spatial-Dependence Note**: why neighbours correlate, design (cluster, HAC, explicit spillover), whether a spatial model is needed.

## Phase 1 — Nuisance vs substance

Common shocks (region) vs true spillovers (people cross borders). Cluster at a higher geography or use spatial HAC for nuisance. Identify spillovers with a design (who is treated, who is neighbour).

## Phase 2 — Models

Spatial lag/error need a weights matrix that is a theory (who is a neighbour). Do not W-matrix shop for stars.

## Phase 3 — Workflow

1. Why dependence?
2. Nuisance fix vs spillover estimand.
3. Weights as theory if a spatial model.
4. Robustness to W.

## Anti-patterns

- iid county regressions
- Default spatial lag
- W shopping
- Spillovers claimed from residual correlation

## Validation gate

Dependence reason; method; W justified if used.

## Final principle

Maps correlate. That is not an identification strategy. Say whether you are fixing SEs or estimating a spillover.
