---
name: joint-distributions-dependence-conditioning
description: Handle joint, marginal, and conditional distributions — independence, covariance, correlation, Bayes, and base rates. Use whenever the user has two variables, needs P(A|B), confuses correlation with independence, or ignores base rates. Apply even if they say "these are related" or "given that."
compatibility: Algebra or simulation.
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 02-joint-distributions-dependence-conditioning
---

# Joint Distributions, Dependence, and Conditioning

## Mission

Two quantities have a joint distribution. Marginals do not determine the joint. Independence is a special case, not a courtesy. Conditioning changes the question.

## Core output

A **Joint Spec**: variables, joint or copula/assumption, independence decision, conditional quantity, base rates explicit.

## Phase 1 — Joint, marginal, conditional

From the joint you get marginals by integrating/summing. Conditionals are joints over marginals. You cannot recover the joint from marginals alone without a dependence assumption.

## Phase 2 — Independence vs uncorrelated

Independence: joint factors, all events involving X are independent of those involving Y.  
Uncorrelated: covariance zero. Independence implies uncorrelated (when moments exist); the converse is false.

Correlation is not a complete dependence summary (nonlinear dependence, outliers).

## Phase 3 — Bayes and base rates

\[
P(H|D)=\frac{P(D|H)P(H)}{P(D)}
\]

Always write the base rate P(H). Medical-test and screening fallacies are base-rate fallacies. Sensitivity is not the positive predictive value.

## Phase 4 — Workflow

1. Name both variables.
2. State whether independence is assumed or checked.
3. If conditioning, write Bayes or the conditional definition with the base rate.
4. If using correlation, say it is linear association only.

## Anti-patterns

- P(H|D) ≈ P(D|H)
- Independence by default in a sum of variances
- Correlation as "explained"
- Ignoring Simpson-type aggregation (see also categorical skill)

## Validation gate

Base rates present for Bayes; independence stated; correlation not over-read.

## Final principle

Conditioning is a new experiment. If you skip the base rate, you answered a different question than the one you were asked.
