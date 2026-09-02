---
name: synthetic-control-comparative-case
description: Build or critique synthetic controls with visible pre-period fit — donor pools, inference limits. Use whenever one (or few) units are treated and a weighted control is proposed. Apply even if they picked one "similar country" by eye.
compatibility: Synthetic control methods; small-N case comparison.
metadata:
  author: Promptstation
  version: 1.0.0
  category: quantitative-analysis
  course: 06-quantitative-analysis
  section: 11-synthetic-control-comparative-case
---

# Synthetic Control and Comparative Case Designs

## Mission

When one place is treated, a synthetic control is a weighted donor pool that matches pre-treatment Y (and covariates). The post gap is the effect if the weights would have continued to match. Pre-fit is the credibility. Placebo-in-space/time is the inference.

## Core output

A **SC Note**: treated unit, donors, weights, pre-fit, post gap, placebo inference, caveats.

## Phase 1 — Donors

Donors that could have been treated similarly, not the whole world. Do not include units that got the same treatment. Interpolating a treated unit as a combination of unlike places with perfect pre-fit can still be interpolation fiction — inspect weights.

## Phase 2 — Inference

With N=1, p-values are placebo ranks, not iid SEs. Do not report a TWFE-style star as if you had 50 treated clusters.

## Phase 3 — Workflow

1. Treated + donor rules.
2. Pre-period fit plot (mandatory).
3. Weights table.
4. Post gap + placebos.
5. Leave-one-donor-out.

## Anti-patterns

- No pre-fit plot
- Donors that are treated
- OLS SEs on a single treated unit
- "Similar country" without weights

## Validation gate

Pre-fit visible; weights shown; inference described as placebo/small-N.

## Final principle

Synthetic control is a weighted narrative of the pre-period. If the pre-period does not match, the post-period is not an effect.
