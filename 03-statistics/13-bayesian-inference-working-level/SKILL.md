---
name: bayesian-inference-working-level
description: Update a stated prior to a posterior and report credible intervals without mixing frequentist language. Use whenever the user wants Bayesian inference, a posterior, a credible interval, or to combine prior knowledge with data. Apply even if they say "Bayesian" but mean "I want P(hypothesis|data)."
compatibility: Conjugate calculations or simple MCMC; state software if used.
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 13-bayesian-inference-working-level
---

# Bayesian Inference at Working Level

## Mission

Bayesian inference is prior × likelihood → posterior. The prior is part of the result. Credible intervals are probability statements about θ given data and prior. Do not call them confidence intervals.

## Core output

A **Posterior Report**: model, prior (and why), likelihood, posterior summary (mean/median, 95% credible interval), sensitivity to prior, predictive check.

## Phase 1 — Ingredients

- prior: uncertainty about θ before these data
- likelihood: model for the data
- posterior: P(θ|data)
- posterior predictive: P(new data|old data)

Flat priors are still priors. They can be improper or surprisingly informative after transformation. Say what you used.

## Phase 2 — Language

Allowed: "Given this prior and model, there is 95% posterior probability that θ lies in (a,b)."

Not allowed: calling that a confidence interval; reporting a p-value as if it were a posterior probability of H0 (it is not, unless you actually computed P(H0|data) with a prior on hypotheses).

Bayes factors are sensitive to priors on nested models. Do not treat them as automatic judges.

## Phase 3 — Computation

Conjugate: write the update in closed form when you can (beta-binomial, normal-normal).  
Otherwise MCMC: diagnostics (R̂, effective sample size, divergences). A pretty density plot is not convergence.

## Phase 4 — Workflow

1. Write the data model.
2. Write the prior in words and math.
3. Compute posterior.
4. Sensitivity: one reasonable alternative prior.
5. Posterior predictive check.
6. Keep frequentist p/CI out of the same sentence.

## Anti-patterns

- Unstated priors
- Mixing CI and credible language
- p-value as P(H0|data)
- MCMC without diagnostics
- "Uninformative prior" as a magic shield

## Validation gate

Prior stated; credible not called confidence; sensitivity mentioned; computation diagnostics if MCMC.

## Final principle

A posterior is a joint of your prior and your data. Hide the prior and you have hidden half the analysis.
