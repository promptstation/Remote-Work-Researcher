---
name: difference-in-differences
description: Implement or critique difference-in-differences with an explicit parallel-trends defence — including staggered-adoption pitfalls. Use whenever the user has a policy change in some places/times and wants DiD. Apply even if they already ran two-way FE.
compatibility: Panel or repeated cross-section policy evaluation.
metadata:
  author: Promptstation
  version: 1.0.0
  category: quantitative-analysis
  course: 06-quantitative-analysis
  section: 06-difference-in-differences
---

# Difference-in-Differences

## Mission

DiD identifies an ATT under parallel trends: without treatment, treated and control would have moved the same. That is not "we have a control group." Staggered adoption with two-way FE can mix signs and weight badly — do not treat TWFE as automatic DiD.

## Core output

A **DiD Note**: treated, control, timing, parallel-trends defence, estimator (canonical 2×2 vs stacked/Sun-Abraham/Callaway-Sant'Anna etc.), event study, estimate.

## Phase 1 — Parallel trends

Defend with: pre-period event study, similar composition, no simultaneous shocks. Insignificant pre-trends are not proof; they are a minimum. Composition change in who is treated is a threat.

## Phase 2 — Staggered timing

If units adopt at different times, TWFE can be a mess. Use an estimator designed for staggered ATT or a clean 2×2. Report event studies.

## Phase 3 — Workflow

1. Who treated when.
2. Control.
3. Event study.
4. Estimator that matches timing.
5. Cluster at the unit of treatment.
6. Other shocks at the same time?

## Anti-patterns

- TWFE on staggered adoption without comment
- Parallel trends as a vibe
- Controls as a substitute for trends
- Post-only with a dummy called DiD

## Validation gate

Parallel-trends sentence; event study; estimator named; cluster unit = treatment unit.

## Final principle

DiD is a trends assumption. If you cannot look at the pre-period, you do not have DiD. You have a hope.
