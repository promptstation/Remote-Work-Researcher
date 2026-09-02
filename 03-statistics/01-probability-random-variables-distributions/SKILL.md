---
name: probability-random-variables-distributions
description: Translate chance processes into random variables and common distributions — probability rules, expectation, variance, Bernoulli/binomial/Poisson/normal/exponential. Use whenever the user needs probability calculations, to pick a distribution, to reason about chance, or to set up a stochastic model. Apply even if they only ask "what's the chance" or "is this normal."
compatibility: Pen-and-paper or simulation in R/Python.
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 01-probability-random-variables-distributions
---

# Probability, Random Variables, and Distributions

## Mission

Name the sample space, the event, and the random variable before computing a number. Probability is not a vibe about whether something "feels likely."

## When this skill governs

Use for chance calculations, distribution choice, expectation/variance, and setting up later inference.

## Core output

A **Probability Spec**: experiment, random variable, distribution (or simulation), computed quantity, assumptions.

## Phase 1 — Objects

- **Sample space** of outcomes
- **Event** as a subset
- **P** as a measure (non-negative, countable additivity, P(Ω)=1)
- Complement, union, intersection; inclusion-exclusion when needed

Conditional probability: \(P(A|B)=P(A\cap B)/P(B)\). Always check P(B)>0.

## Phase 2 — Random variables

A random variable maps outcomes to numbers. Specify discrete vs continuous.

- expectation is a long-run mean, not "the value we expect this time"
- variance is spread, not risk in the decision-theory sense unless you make it so
- linearity of expectation holds without independence; variance of sums needs covariance

## Phase 3 — Common families (pick on story, not habit)

| Story | Family |
| --- | --- |
| Success/failure trial | Bernoulli / binomial |
| Counts of rare events in time/space | Poisson (check overdispersion later) |
| Waiting time, memoryless | Exponential |
| Unknown in an interval, no structure | Uniform (rare in nature) |
| Sums of many small bits | Normal (CLT — next skills) |

Do not assume normality because the variable is continuous.

## Phase 4 — Workflow

1. Write the experiment.
2. Define X.
3. Justify family or simulate.
4. Compute; state assumptions.
5. Sanity-check with simulation if algebra is heavy.

## Anti-patterns

- Probability as "confidence I feel"
- Normal-by-default
- E[X²] vs (E[X])² confusion
- Treating expectation as a typical value in a skewed distribution (use median too)

## Validation gate

Experiment, RV, family, assumption, number — all present.

## Final principle

If you cannot name the random variable, you are not doing probability. You are guessing with a percent sign.
