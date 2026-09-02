---
name: supervised-learning-prediction
description: Fit predictive models matched to the target, sample size, and need for transparency — linear and regularised models, trees, ensembles, boosting, and simple neural nets. Use whenever the user wants a predictive model, classifier, ranker, or forecast from labelled data. Apply even if they name a trendy algorithm first.
compatibility: Standard ML stacks; CPU-first unless scale demands otherwise.
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 06-supervised-learning-prediction
---

# Supervised Learning for Prediction

## Mission

Choose the simplest model that beats a serious baseline on a leakage-free split and can be explained to the person who will use it. Algorithm fashion is not a method.

## When this skill governs

Use when predicting a known target from features for new units. Evaluation details live also in the evaluation skill; causal claims are out of scope.

## Core output

Deliver a **Prediction Report**:

1. Target, decision time, baseline
2. Model class and why it fits n, p, and transparency need
3. Training protocol (split, class weight, calibration)
4. Metrics vs baseline, overall and by slice
5. Error analysis
6. How to use scores in the decision
7. What the model must not be used to claim

## Phase 1 — Match model to problem

| Situation | Default |
| --- | --- |
| Small n, need coefficients | Penalised linear / GLM |
| Mixed types, interactions, moderate n | Gradient boosting (e.g. boosted trees) |
| Need a rule people can audit | Shallow tree or sparse linear |
| Text/images as inputs | Representation + simple head (see unstructured skill) |
| Strong linear signal | Linear first; ensembles only if they win |

Start with a linear (or GLM) baseline and a tree/boosting baseline. If they tie, take the simpler.

Deep nets for small tabular problems are usually a delay.

## Phase 2 — Task types

- **Regression:** predict a number; check heteroskedasticity and tails
- **Binary:** predict a probability, not a hard label, until a threshold is chosen from costs
- **Multiclass / ranking:** metric must match the decision (top-k, not only accuracy)

Class imbalance: change the metric and the threshold before you change the architecture. Resampling is optional; calibrated probabilities and cost-sensitive thresholds are not.

## Phase 3 — Training discipline

- leakage-free split (preparation skill)
- tune on validation, once; do not peek at test repeatedly
- regularise when p is large
- calibrate probabilities (Platt/isotonic) if decisions need probabilities
- seeds and library versions recorded

Do not stack seven ensembles because a leaderboard asked. Complexity must pay rent in metric and in operations.

## Phase 4 — Error analysis

A mean metric is not a model review.

- slice by segment (new vs old, high vs low volume)
- inspect false positives/negatives as records
- residual plots for regression
- learning curves if you are deciding whether more data beats more model

If errors cluster in a slice the business cares about, the average AUC is not the product.

## Phase 5 — Research workflow

1. Confirm frame, leakage audit, baseline.
2. Fit simple model; beat baseline or stop.
3. Fit one flexible class; compare.
4. Calibrate; pick threshold from costs.
5. Slice-wise errors.
6. Freeze; document what it is not (not an effect of X on Y).

## Anti-patterns

- XGBoost as the first and only move
- Accuracy on 2% event rates
- Hard labels without a threshold policy
- Causal verbs ("drivers," "impact") from feature importance
- Tuning on the test set
- Ignoring the linear baseline that already won

## Decision heuristic

1. What must we beat?
2. Do we need probabilities or ranks?
3. How much n and p do we have?
4. How transparent must this be?
5. Did the flexible model win on a clean split, by enough?

## Validation gate

- Baseline present
- Split clean
- Metric matches the decision
- Probabilities calibrated if used as probabilities
- No causal language
- Simpler model reported even if not chosen

## Final principle

A supervised model is a function from known-at-t features to a guess. It earns its keep only by beating a baseline a skeptic would have used.
