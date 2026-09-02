---
name: regression-discontinuity
description: Use RDD only at a real cutoff and report a local effect — sharp/fuzzy, bandwidth, density tests. Use whenever treatment is assigned at a threshold (score, age, border). Apply even if the user wants to generalise the cutoff effect to everyone.
compatibility: Sharp and fuzzy RDD.
metadata:
  author: Promptstation
  version: 1.0.0
  category: quantitative-analysis
  course: 06-quantitative-analysis
  section: 09-regression-discontinuity
---

# Regression Discontinuity

## Mission

If D jumps at a cutoff of a running variable R, and Y would be continuous in R without treatment, the jump in Y at the cutoff is a local causal effect. It is not the effect for people far from the cutoff.

## Core output

An **RDD Note**: running variable, cutoff, sharp vs fuzzy, bandwidth, density/McCrary, covariate jumps, local estimate.

## Phase 1 — Design

A real administrative cutoff, not a median split. Units should not perfectly manipulate R (density test). Covariates should not jump.

Fuzzy: the cutoff is an instrument for D; exclusion is "only through treatment probability."

## Phase 2 — Estimation

Local linear, bandwidth justified (data-driven + sensitivity). Donut if manipulation at the exact point. Plots of Y vs R with the cutoff marked are mandatory.

## Phase 3 — Workflow

1. Is there a cutoff that assigns D?
2. Plots.
3. Density and covariate tests.
4. Local estimate + bandwidth sensitivity.
5. Locality in the interpretation sentence.

## Anti-patterns

- Median splits called RDD
- Global high-order polynomials
- Generalising far from cutoff
- No plot

## Validation gate

Cutoff real; plot; local language; density considered.

## Final principle

RDD is a microscope at a line. If the decision is about people far from the line, you need a different design.
