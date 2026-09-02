---
name: instrumental-variables
description: Argue or reject instruments on exclusion, independence, and monotonicity — LATE, weak instruments, first stage. Use whenever the user proposes an IV, 2SLS, or "we instrumented with." Apply even if first-stage F is large.
compatibility: 2SLS and related.
metadata:
  author: Promptstation
  version: 1.0.0
  category: quantitative-analysis
  course: 06-quantitative-analysis
  section: 08-instrumental-variables
---

# Instrumental Variables

## Mission

An instrument Z shifts D and affects Y only through D (exclusion), is as-if random (independence), and moves D in one direction (monotonicity for LATE). A strong first stage without exclusion is a biased machine with extra confidence.

## Core output

An **IV Brief**: Z, first stage, exclusion argument, independence, LATE population, weak-IV diagnostics, estimate.

## Phase 1 — Conditions

- **Relevance:** Z predicts D (F, not only t)
- **Independence:** Z not tied to Y(0)
- **Exclusion:** no direct Z→Y path
- **Monotonicity:** no defiers, for LATE interpretation

Write the exclusion story in words. If Z is a lagged variable, another policy, or "distance" — list the ways exclusion fails.

## Phase 2 — LATE

IV estimates the effect for compliers. Say who they are. Not ATE.

Weak IV: biased toward OLS; use weak-IV robust inference when in the danger zone.

## Phase 3 — Workflow

1. Exclusion paragraph first.
2. First stage.
3. Reduced form (Z on Y) — if zero, beware.
4. 2SLS + diagnostics.
5. Who are compliers?

## Anti-patterns

- F>10 as a personality certificate
- Exclusion unargued
- Many instruments as a flex (overidentification is a test, not a virtue if they are all invalid)
- LATE as ATE

## Validation gate

Exclusion in words; first stage; LATE population; weak-IV considered.

## Final principle

Instruments are natural experiments. If you cannot tell the experiment, you do not have an IV. You have a second stage.
