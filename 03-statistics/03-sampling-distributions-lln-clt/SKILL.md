---
name: sampling-distributions-lln-clt
description: Distinguish samples from populations and use sampling distributions, the LLN, and the CLT — including when the CLT is a poor excuse. Use whenever the user talks about "the sample," standard errors, why means look normal, or how large n must be. Apply even if they invoke "n>30" as a spell.
compatibility: Simulation welcome.
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 03-sampling-distributions-lln-clt
---

# Sampling, Sampling Distributions, LLN, and CLT

## Mission

The data are one realisation of a sampling process. Estimators have distributions. The CLT is a theorem with conditions, not a blessing of n=30.

## Core output

A **Sampling Note**: population, sampling process, estimator, sampling distribution (exact or approximate), whether LLN/CLT apply.

## Phase 1 — Population and sampling

- target population vs sampled population vs dataset
- iid is an assumption: no clustering, no time dependence, no without-replacement issue at large fractions
- survey sampling (Course 7) may be design-based; here the default is iid model-based unless told otherwise

## Phase 2 — Sampling distribution

The sampling distribution is the distribution of the estimator across repeated samples, not the distribution of the raw data.

Standard error = SD of that sampling distribution (estimated). It is not the SD of the data.

## Phase 3 — LLN and CLT

LLN: averages settle at expectations when moments exist and dependence is limited.  
CLT: averages become approximately normal. Rate depends on skew and tails.

"n>30" is folklore. For Bernoulli p≈0.01 you need much more; for heavy tails the CLT may be useless at your n. Simulate if unsure.

Means of means can be approximately normal when the data are not. That does not make the data Gaussian for methods that need Gaussian errors.

## Phase 4 — Workflow

1. Name population and sampling.
2. Name estimator.
3. Exact sampling distribution if available (e.g. binomial).
4. Otherwise, justify CLT or bootstrap (later skill).
5. Refuse n>30 as a sufficient condition.

## Anti-patterns

- SE confused with SD
- n>30 mantra
- Treating the histogram of data as the sampling distribution
- iid SEs on clustered samples

## Validation gate

Estimator named; SE vs SD distinct; CLT conditions addressed.

## Final principle

Uncertainty lives in the sampling distribution of the estimator. If you have not named that object, you do not yet have inference.
