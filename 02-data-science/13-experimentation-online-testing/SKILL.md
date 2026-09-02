---
name: experimentation-online-testing
description: Design and critique A/B tests and digital experiments — randomisation units, interference, peeking, power, and when not to experiment. Use whenever the user wants an A/B test, online experiment, banner test, or to read an experimentation platform result. Apply even if they peeked at p-values mid-test or ask "is this lift real."
compatibility: Experiment platforms and offline randomisation; statistics of experiments overlap Course 3 but this skill is the product/ops protocol.
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 13-experimentation-online-testing
---

# Experimentation and Online Testing

## Mission

An A/B test is a causal design. It earns that status only if randomisation is real, the unit is right, interference is handled, and the stopping rule was written in advance. A dashboard p-value is not an experiment.

## When this skill governs

Use for A/B/n tests, holdouts, geolift-style experiments, and critiques of experiment-platform outputs.

## Core output

Deliver an **Experiment Protocol** (before launch) or **Experiment Readout** (after):

1. Hypothesis and decision
2. Unit of randomisation
3. Outcome and window
4. Power / MDE
5. Interference and spillovers
6. Stopping rule
7. Result with interval, not only p
8. Ship / iterate / kill

## Phase 1 — When not to A/B

Do not randomise if:

- the action is irreversible and harmful at any scale without a smaller proxy
- interference cannot be contained and the estimand is hopeless
- the outcome cannot be measured in a relevant window
- sample is too small for any decision-relevant MDE

Then use another identification strategy or a qualitative stop.

## Phase 2 — Unit and interference

Randomise at the unit where you treat: user, account, session, server, city.

Interference (one user's treatment affects another's outcome) biases naive estimators. Repair with clustering, network experiments, or switchback — or admit the estimand is "direct effect under this exposure."

SRM (sample-ratio mismatch) is a stop-the-line defect, not a footnote.

## Phase 3 — Outcomes, power, peeking

- primary outcome locked
- window locked (no "until it is significant")
- MDE and power computed from baseline variance
- peeking requires sequential designs or alpha spending; otherwise you inflated false positives
- CUPED or pre-period covariates to cut variance — fit with pre-treatment data only

Multiple variants and multiple metrics need a multiplicity plan.

## Phase 4 — Readout

- intent-to-treat as default
- interval on the effect
- slices as exploratory unless pre-registered
- novelty effects: short windows can lie
- long-term holdouts when the metric is lagging (retention, LTV)

A non-significant test is not "no effect"; it is "not larger than we were powered to see," unless you interval that.

## Phase 5 — Research workflow

1. Decision and MDE.
2. Unit, outcome, window, stop rule.
3. Launch checks (SRM, assignment).
4. Analyse at the planned time.
5. Decision; log for meta-analysis later.

## Anti-patterns

- Peeking until p<0.05
- Session-randomising a user-level treatment
- Ignoring SRM
- 20 metrics, one "win"
- Calling NS "no impact"
- Underpowered tests as proof of safety
- Triggering analysis on the treated-only compliers without saying so

## Decision heuristic

1. What decision does this test bind?
2. What is the unit?
3. What MDE is worth detecting?
4. Who interferes with whom?
5. What was the stopping rule before launch?

## Validation gate

- Unit named
- Primary outcome named
- MDE/power addressed
- Stopping rule pre-specified or sequential method named
- SRM checked
- Interval reported

## Final principle

Experimentation is planned comparison under random assignment. Everything that looks like an A/B test but lacks a unit, a window, and a stop rule is just peeking at production.
