---
name: model-evaluation-validation-uncertainty
description: Evaluate predictive models against baselines and decision costs — proper scoring, calibration, cross-validation, slice errors, and uncertainty. Use whenever the user reports accuracy/AUC, needs a validation plan, compares models, or asks if a model is "good." Apply even if they only paste a classification report.
compatibility: Standard ML evaluation; no specific library required.
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 08-model-evaluation-validation-uncertainty
---

# Model Evaluation, Validation, and Uncertainty

## Mission

A model is as good as its comparison. Report performance against a baseline, on a split that could have falsified it, with a metric that matches the decision, plus uncertainty and slices. Vanity metrics are not evaluation.

## When this skill governs

Use whenever a predictive model is being judged, compared, tuned, or shipped, or when a user presents a metric as proof.

## Core output

Deliver an **Evaluation Card**:

1. Baseline and metric (with why)
2. Split / CV scheme
3. Headline metric ± uncertainty
4. Calibration (if probabilities)
5. Slice table
6. Confusion or residual picture at the chosen threshold
7. Decision: ship, iterate, or stop

## Phase 1 — Metric matches the decision

- **Probabilities for decisions:** Brier, log loss, calibration plots — then a threshold from costs
- **Ranking / targeting:** AUC, PR-AUC (better when events are rare), lift at k
- **Point forecasts:** RMSE/MAE; MAE if tails should not dominate; pinball for quantiles
- **Hard classification:** do not lead with accuracy on imbalanced data

Accuracy is allowed only when classes are balanced and errors are symmetric. That is rare.

Never optimise a metric you would not sign in a report.

## Phase 2 — Validation that can fail

- hold out a test set once
- time-aware or group-aware splits when required
- nested CV if tuning
- prequential evaluation for streaming

Repeatedly tweaking after looking at test is just training on test. If it happened, say so and get a new holdout.

## Phase 3 — Uncertainty

A point AUC is not a fact.

- bootstrap the test metric, or use CV fold spread
- for small test n, wide intervals — do not rank two models that overlap
- prediction intervals for regression when the user needs a range, not only RMSE

## Phase 4 — Calibration and slices

If you act on predicted probabilities, check calibration by decile. A well-ranked uncalibrated model will mis-price risk.

Slices: at least the segments the decision treats differently (region, new vs returning, score bands). A model that fails the slice you will target is a failed model.

## Phase 5 — Research workflow

1. Lock metric and baseline before looking at challenger results.
2. Evaluate on the proper split.
3. Calibration + slices + errors.
4. Compare intervals, not just point estimates.
5. Recommend ship / iterate / stop.

## Anti-patterns

- Accuracy as the hero metric
- No baseline
- Test-set shopping
- AUC as a business KPI
- Ignoring calibration
- Ranking models inside each other's error bars
- One global number, no slices

## Decision heuristic

1. What decision does this number change?
2. What baseline would a skeptic use?
3. Could this split have falsified the model?
4. Are probabilities calibrated?
5. Where does it fail?

## Validation gate

- Baseline present
- Metric justified
- Split scheme named
- Uncertainty shown
- Slices shown
- Threshold tied to costs if labels are issued

## Final principle

Evaluation is a comparison under a protocol. A number without a baseline, a split, and a slice is a press release.
