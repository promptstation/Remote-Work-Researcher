---
name: selection-confounding-naive-comparisons
description: Diagnose why treated-vs-untreated gaps are not effects — selection, omitted variables, simultaneity, measurement error. Use whenever the user compares participants to non-participants or shows a before-after as impact. Apply even if they "controlled for demographics."
compatibility: Applied research critique.
metadata:
  author: Promptstation
  version: 1.0.0
  category: quantitative-analysis
  course: 06-quantitative-analysis
  section: 03-selection-confounding-naive-comparisons
---

# Selection, Confounding, and Naive Comparisons

## Mission

People who take D differ in Y(0). That difference is selection. Until a design kills it, the gap is a mix of effect and selection. "Controls" only help if they capture the selection process.

## Core output

A **Selection Critique**: naive contrast, likely Y(0) differences, what controls cannot do, what design would.

## Phase 1 — Stories

- who chooses treatment (motivation, need, access)
- reverse causality (Y causes D)
- simultaneity
- measurement of D and Y (attenuation, differential error)

## Phase 2 — Controls

Conditioning on post-treatment variables (colliders, mediators) can create bias. Conditioning on pre-treatment can help under CIA. A long list of covariates is not a design.

## Phase 3 — Workflow

1. Write the naive gap.
2. Who is missing from treated, and how is their Y(0) different?
3. Kill causal language or propose a design.

## Anti-patterns

- Kitchen sink as solution
- Matching on post-treatment
- Before-after as DiD without a control group

## Validation gate

Selection story named; controls not treated as magic.

## Final principle

The untreated are not a clone army. If you have not said why their Y(0) matches, you have described, not identified.
