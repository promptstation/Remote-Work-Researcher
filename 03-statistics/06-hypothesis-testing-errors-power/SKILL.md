---
name: hypothesis-testing-errors-power
description: Design or critique hypothesis tests — p-values, Type I/II errors, power, and significance vs importance. Use whenever the user wants a p-value, a significance test, sample size, or asks "is this significant." Apply even if they treat p<0.05 as a discovery.
compatibility: Standard tests; power formulas or simulation.
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 06-hypothesis-testing-errors-power
---

# Hypothesis Testing, Errors, and Power

## Mission

A test is a rule for seeing whether data are surprising under a stated null. A p-value is a tail probability under that null, not P(H0|data) and not an effect size. Significance is not importance.

## Core output

A **Test Protocol or Readout**: H0, H1, α, test statistic, p, effect size + interval, power/MDE, decision language that does not overclaim.

## Phase 1 — State the null

H0 must be a probability model, not a vibe ("nothing interesting"). One-sided vs two-sided is a pre-choice, not a post-choice after seeing the sign.

α is the Type I error rate of the procedure, not of this particular yes/no.

## Phase 2 — p-values

p = P(statistic as extreme or more | H0 true, model true).

It is not:

- the probability the null is true
- the probability of replicating
- the FDR of a literature

p=0.049 and p=0.051 are the same scientific situation; the cliff is a house rule.

Always pair p with an effect size and an interval. A tiny p on a tiny effect in a huge sample is not a finding worth acting on by itself.

## Phase 3 — Power

Power = P(reject H0 | H1 at a specified effect). Compute MDE for given n, α, variance. Underpowered "non-significance" is not evidence of a near-zero effect — report the interval.

Optional stopping and extra tests belong in the multiplicity skill. They invalidate naive p-values.

## Phase 4 — Language

- "We reject H0 at α=0.05" or "we do not reject H0"
- not "we proved H0" / "there is no effect"
- not "highly significant" as a substitute for magnitude

## Phase 5 — Workflow

1. H0, H1, α, primary outcome (pre-specified if confirmatory).
2. Effect size of interest and power.
3. Test + interval.
4. Decision + limitation.

## Anti-patterns

- p-hacking and HARKing (see multiplicity skill)
- NS = no effect
- p as strength of a theory
- One-sided tests chosen after seeing data
- α=0.05 as a law of nature

## Validation gate

H0 explicit; p not misinterpreted; effect size + interval present; power/MDE addressed when NS is used in an argument.

## Final principle

Tests control error rates of procedures. They do not grade the truth of a story. If you need magnitude, show the interval.
