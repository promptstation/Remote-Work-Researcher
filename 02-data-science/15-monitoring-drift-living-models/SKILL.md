---
name: monitoring-drift-living-models
description: Detect when a recurring or deployed model has stopped meaning what it meant at launch — training-serving skew, data and concept drift, retraining policy, and fallback. Use whenever a model is in production, a monthly score is reused, or performance may have silently decayed. Apply even if the user only asks "should we retrain" or "why did scores change."
compatibility: Batch or service deployments; logging of inputs, outputs, and delayed labels.
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 15-monitoring-drift-living-models
---

# Monitoring, Drift, and Living Models

## Mission

Launch performance is a historical fact. Living models need input checks, prediction checks, delayed-label checks, and a written retraining and fallback policy. A silent model is a decision made with last year's world.

## When this skill governs

Use after a model is scheduled, deployed, or reused, or when scores shift and nobody knows why.

## Core output

Deliver a **Monitoring Plan** (or a **Drift Diagnosis**):

1. What "healthy" meant at launch (metrics, input ranges)
2. Logging (features, scores, decisions, labels when they arrive)
3. Drift tests (data vs concept)
4. Alert thresholds
5. Retrain vs rollback vs disable
6. Owner and cadence

## Phase 1 — Two failures

**Training-serving skew:** production features are not the training features (different code, defaults, clocks, filters). This is a bug. Unit-test the feature code shared by train and serve.

**Drift:** the world moved.

- data drift: input distribution changed
- concept drift: P(Y|X) changed
- label delay: you will not know concept drift until labels arrive — plan for that lag

## Phase 2 — What to watch

- volume and null rates of each feature
- range / hash of category sets
- score distribution (mean, share above threshold)
- decision volume (emails sent, claims flagged)
- delayed outcome metric vs launch baseline
- slice metrics for high-stakes groups

Population Stability Index and KS are tools, not religions. A shift that does not change decisions may not be an incident. A tiny shift on the threshold boundary may be.

## Phase 3 — Policy

Write before launch:

- when to retrain (calendar vs trigger)
- how to validate a retrain (same evaluation skill, new holdout)
- when to fall back to the baseline rule
- who can disable the model

Retraining on drifted labels without a target audit can encode a broken process (feedback loops: the model affects who is labelled).

## Phase 4 — Research workflow

1. Confirm train=serve feature code.
2. Compare live input and score distributions to launch snapshots.
3. When labels arrive, recompute the evaluation card.
4. Separate skew (fix code) from drift (retrain or redesign).
5. Record the incident.

## Anti-patterns

- No logging of production features
- Retrain every week with no evaluation
- Ignoring feedback loops
- Alerting on every PSI tick
- No fallback
- Assuming last quarter's AUC still holds

## Decision heuristic

1. Is this skew or drift?
2. Did the decision volume change?
3. Have labels arrived?
4. Retrain, rollback, or redesign?
5. Who owns the disable switch?

## Validation gate

- Launch snapshot exists
- Feature parity checked
- Input, score, and (when possible) label monitors exist
- Retrain/fallback policy written
- Feedback loops considered

## Final principle

A model is a claim about a joint distribution. When that distribution moves, the claim expires. Monitoring is how you notice the expiry date.
