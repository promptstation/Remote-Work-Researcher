---
name: generalised-linear-models
description: Choose and interpret GLMs that match the outcome — logistic, Poisson/negative binomial, link functions, predicted probabilities and counts. Use whenever the user has a binary, count, or bounded outcome and wants regression. Apply even if they run OLS on a 0/1 anyway.
compatibility: GLM routines in R/Python/Stata.
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 10-generalised-linear-models
---

# Generalised Linear Models

## Mission

Match the model to the type of Y. Binary outcomes need a probability model; counts need a count model. Report effects on the response scale (probabilities, expected counts), not only on the logit or log.

## Core output

A **GLM Report**: family + link, coefficients, response-scale effects (AME or predictions at stated X), overdispersion check, diagnostics.

## Phase 1 — Family

| Y | Default |
| --- | --- |
| Binary | Logistic (or Bernoulli with logit/probit) |
| Count | Poisson; negative binomial if overdispersed |
| Positive continuous, skewed | Gamma / log-linear; or OLS on log with smearing caution |
| 0/1 with linear probability | LPM only as a descriptive approximation with robust SEs; watch fitted values outside [0,1] |

Link connects mean to linear predictor. Logit for odds; log for counts. Do not interpret a logit coefficient as a percentage point effect.

## Phase 2 — Interpretation

- odds ratios from logistic: still not risk ratios
- average marginal effects or predicted P at realistic X for probability points
- for Poisson, exp(β) is a multiplicative factor on expected counts, under the model

Interactions on nonlinear models are not the coefficient on the product term alone. Use predicted differences.

## Phase 3 — Trouble

- complete separation in logistic: inflate SEs; penalise or simplify
- overdispersion in Poisson: SEs too small → NB or robust/quasi-Poisson
- excess zeros: zero-inflated or hurdle, if the science has two processes
- clustered data: clustered SEs or mixed GLM (dependence skill)

## Phase 4 — Workflow

1. Type of Y.
2. Family + link.
3. Fit; check overdispersion/separation.
4. Response-scale table.
5. No causal verbs unless designed.

## Anti-patterns

- OLS on binary as the only model without comment
- Logit coefficients as percentage points
- Ignoring overdispersion
- Product-term interaction as the whole story in logistic

## Validation gate

Family matches Y; response-scale effect present; overdispersion/separation checked.

## Final principle

A GLM is a mean model for a type of data. If the reader cannot see an effect in probabilities or counts, you have not finished interpreting.
