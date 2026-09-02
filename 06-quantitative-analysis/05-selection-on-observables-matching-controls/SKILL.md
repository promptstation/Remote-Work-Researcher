---
name: selection-on-observables-matching-controls
description: Use matching, propensity scores, and regression controls only when unconfoundedness is plausible. Use whenever the user wants to "control for," match treated to controls, or IPW. Apply even if they think more covariates automatically identify.
compatibility: Matching/IPW/OLS with pre-treatment covariates.
metadata:
  author: Promptstation
  version: 1.0.0
  category: quantitative-analysis
  course: 06-quantitative-analysis
  section: 05-selection-on-observables-matching-controls
---

# Selection on Observables, Matching, and Regression Controls

## Mission

Unconfoundedness (CIA): Y(0), Y(1) ⊥ D | X. That is a substantive claim about X, not a software option. If people select on unobservables (motivation, forecasted Y), matching will not save you.

## Core output

An **Observables Design**: X list (pre-treatment), why CIA is plausible, overlap, method (match/IPW/regression), estimate, remaining threat.

## Phase 1 — CIA

Write the unobservables you worry about. If X does not capture them, stop. Good CIA settings: assignment that is as-if random given a known rule (eligibility scored on X you have).

## Phase 2 — Overlap

No overlap → no matching; you are extrapolating. Show propensity histograms. Trim with a rule, disclose.

## Phase 3 — Methods

Matching, IPW, OLS are different estimators of similar estimands under CIA. Doubly robust methods still need one of the models plus CIA. Regression with "bad controls" (post-treatment) is not CIA.

## Phase 4 — Workflow

1. Defend CIA in words.
2. Overlap.
3. Estimate; balance table.
4. Sensitivity (how large an unobservable would need to be).

## Anti-patterns

- Matching as design
- Post-treatment X
- No overlap check
- 200 covariates as credibility

## Validation gate

CIA sentence; pre-treatment X; overlap; no causal claim if CIA is a wish.

## Final principle

Conditioning is identification only when the observables are the selection process. Otherwise it is a different descriptive gap.
