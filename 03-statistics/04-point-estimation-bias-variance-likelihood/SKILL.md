---
name: point-estimation-bias-variance-likelihood
description: Propose estimators and diagnose bias vs noise — MSE, method of moments, maximum likelihood. Use whenever the user asks how to estimate a parameter, whether an estimator is biased, or what MLE is doing. Apply even if they only want "the best estimate."
compatibility: Algebra, numeric MLE, or simulation.
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 04-point-estimation-bias-variance-likelihood
---

# Point Estimation, Bias, Variance, and Likelihood

## Mission

An estimator is a function of the sample. Name the target parameter, the estimator, and whether error is bias, variance, or a wrong target. "The estimate" without that triple is a number, not estimation.

## Core output

An **Estimation Note**: target θ, estimator θ̂, identifying assumption, bias/variance/MSE, method (MoM, MLE, other).

## Phase 1 — Target vs estimator

θ is a property of the population or process. θ̂ is random. Unbiased means E[θ̂]=θ, not "this sample looks fair." Finite-sample unbiasedness can conflict with lower MSE (e.g. some regularised or ratio estimators).

MSE = bias² + variance. Lower MSE can justify a little bias. Say so.

## Phase 2 — Methods

**Method of moments:** match sample moments to model moments. Simple; can be inefficient or produce invalid values.

**Maximum likelihood:** θ̂ maximises L(θ; data). Under regularity, MLE is consistent, asymptotically normal, efficient. Regularity fails at boundaries, with wrong models, and with dependence ignored.

Likelihood is not a probability of the parameter. It is the probability (density) of the data viewed as a function of θ.

## Phase 3 — Diagnostics

- If θ̂ systematically misses in simulations or by algebra → bias
- If it jumps with small data changes → variance
- If the model is wrong, consistency is about a pseudo-true parameter — say that

Do not "debias" by staring at the number. Debias with algebra, a better design, or a known correction.

## Phase 4 — Workflow

1. Write θ in words.
2. Propose θ̂.
3. Sketch bias and variance or cite a theorem.
4. If MLE, write the likelihood and the support of the data.
5. Report θ̂ with an SE (next skills) — a point without uncertainty is incomplete for research.

## Anti-patterns

- Unbiased as automatically best
- Likelihood as P(θ|data)
- MLE on a model that cannot generate the data (wrong support)
- Reporting 8 decimal places of a noisy θ̂

## Validation gate

Target named; estimator named; bias vs variance addressed; method named.

## Final principle

Estimation is a rule with a target. If you cannot say what would happen to the rule in repeated samples, you have not estimated — you have calculated.
