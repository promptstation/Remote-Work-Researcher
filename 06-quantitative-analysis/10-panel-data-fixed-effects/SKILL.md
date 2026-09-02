---
name: panel-data-fixed-effects
description: Know what variation identifies a fixed-effects coefficient — within variation, two-way FE, time-varying confounding FE cannot kill. Use whenever the user has panel data, "we included FE," or difference-out time-invariant confounders. Apply even if they think FE identify everything.
compatibility: Entity and two-way FE.
metadata:
  author: Promptstation
  version: 1.0.0
  category: quantitative-analysis
  course: 06-quantitative-analysis
  section: 10-panel-data-fixed-effects
---

# Panel Data and Fixed Effects

## Mission

Entity FE use only within-entity changes. Time-invariant confounding is gone. Time-varying confounding is not. If D does not change within entity, FE cannot identify it. Two-way FE also absorb common shocks.

## Core output

An **FE Note**: entity, time, what variation is left, threats that remain, estimate.

## Phase 1 — What is differenced out

Anything fixed for the entity (geography, sex, "culture" as fixed). Anything that changes can still bias. Measurement error in D is often worse in within models.

## Phase 2 — Two-way FE

TWFE is not automatically DiD. See DiD skill for staggered treatment. For continuous D, you are using within covariation of D and Y after time shocks.

## Phase 3 — Workflow

1. Does D vary within entity?
2. What time-varying confounder remains?
3. Cluster SEs at entity (or treatment level).
4. Compare to pooled OLS as description, not as rival "truth."

## Anti-patterns

- FE as a causal spell
- No within variation
- Ignoring staggered TWFE issues
- Clustering at the wrong level

## Validation gate

Within variation confirmed; remaining confounders named; cluster named.

## Final principle

Fixed effects buy you the within comparison. They do not buy you a design if the within variation is still confounded.
