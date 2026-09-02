---
name: weighting-calibration-imputation
description: Build or critique survey weights — base weights, nonresponse adjustment, calibration, item imputation. Use whenever the user has survey microdata or a vendor weight. Apply even if they analyse unweighted clustered data.
compatibility: Design weights; raking/GREG; imputation.
metadata:
  author: Promptstation
  version: 1.0.0
  category: survey-methodology
  course: 07-survey-methodology
  section: 09-weighting-calibration-imputation
---

# Weighting, Calibration, and Imputation

## Mission

Weights implement the design (1/π_i), then adjust for nonresponse and known population totals. They are a model plus a design. Huge weights and silent trimming are quality issues. Item imputation is a separate model.

## Core output

A **Weighting Spec**: base weight, NR adjustment, calibration totals, trimming, how to use in analysis.

## Phase 1 — Base

w_i = 1/π_i including all stages and within-household selection. If π_i unknown, you do not have design weights (nonprobability skill).

## Phase 2 — Adjustment

NR: cells or propensity. Calibration/raking to age×sex×region (etc.) totals that are trusted. If the totals are wrong, you impose the wrong margin.

Trim extreme weights with a rule; report.

## Phase 3 — Imputation

Item missing: flags + method (hot deck, model). Do not mean-fill income and forget. Multiple imputation if inference needs it.

## Phase 4 — Workflow

1. Reconstruct π_i.
2. NR model.
3. Calibrate.
4. Diagnostics (weight CV, max/min).
5. Analysis with weights + design SEs.

## Anti-patterns

- Unweighted estimates of a stratified sample as "the population"
- Raking to 20 margins on n=400
- Hiding trimmed weights
- Treating weights as making nonprobability equal probability

## Validation gate

Base weight origin; calibration margins named; analysis instruction includes design SEs.

## Final principle

A weight is an argument about who is missing and who the population is. If you cannot state it, do not apply a black-box w.
