---
name: interval-estimation-uncertainty
description: Report confidence intervals with correct coverage interpretation and named standard errors. Use whenever the user needs a CI, margin of error, or to communicate uncertainty around an estimate. Apply even if they want "just the number" or misread a CI as a probability that θ is inside.
compatibility: Formula SEs or bootstrap (see resampling skill).
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 05-interval-estimation-uncertainty
---

# Interval Estimation and Uncertainty Communication

## Mission

A confidence interval is a random interval with a stated long-run coverage of a fixed parameter (frequentist). It is not P(θ ∈ this interval | data) unless you switch to a Bayesian credible interval and say so.

## Core output

An **Interval Report**: estimate, SE, interval, coverage statement, method, assumption.

## Phase 1 — Standard errors

SE is the estimated SD of the sampling distribution. Name the formula (iid, sandwich, clustered, delta method). A wrong SE makes a decorative interval.

Delta method: for g(θ̂), use g'(θ̂)² Var(θ̂). Check that g is not flat or exploding at θ.

## Phase 2 — Wald and better

Wald: θ̂ ± z_{1-α/2} SE. Fine when the sampling distribution is roughly normal.

Poor when:

- p near 0 or 1 for proportions (use Wilson/Jeffreys)
- strong skew, small n
- boundary parameters

Then bootstrap or exact/profile intervals.

## Phase 3 — Language

Allowed: "A 95% confidence interval is (a,b), computed by [method]. In repeated samples this procedure covers the true parameter about 95% of the time."

Not allowed: "There is a 95% chance that θ is between a and b" — unless Bayesian.

Also not allowed: "95% of the data lie in the CI." That is a different interval.

Width is not importance. A tight interval around a tiny effect is precise triviality.

## Phase 4 — Workflow

1. Point estimate and SE method.
2. Check n, skew, boundaries.
3. Choose Wald vs alternative.
4. Report (estimate, SE, interval, n).
5. One correct coverage sentence.

## Anti-patterns

- CI as a probability statement about θ (frequentist)
- SE of the data as SE of the mean (forgot /√n)
- 95% as a personality trait of the study
- Intervals that include impossible values without comment (rates <0)

## Validation gate

SE named; interval method named; interpretation correct; n visible.

## Final principle

Uncertainty is a property of the procedure. Speak that way, or switch explicitly to a posterior.
