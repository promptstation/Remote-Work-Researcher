---
name: randomised-experiments-research
description: Design or analyse research RCTs — assignment, ITT vs TOT, compliance, clustered randomisation, ethics. Use whenever the user can randomise or has RCT data. Apply even if they analyse only the treated.
compatibility: Field and lab experiments; product A/B also in Course 2.
metadata:
  author: Promptstation
  version: 1.0.0
  category: quantitative-analysis
  course: 06-quantitative-analysis
  section: 04-randomised-experiments-research
---

# Randomised Experiments in Research

## Mission

Random assignment identifies ITT of assignment. Balance, compliance, spillovers, and clustering still exist. An RCT is not automatically a well-analysed causal study.

## Core output

An **RCT Protocol or Analysis**: unit, assignment, ITT, compliance plan, cluster, power, ethics, result.

## Phase 1 — Assignment

Unit of randomisation = unit of analysis or cluster SEs. Block on strong predictors of Y. Check balance and implementation (SRM analogue).

## Phase 2 — Compliance

ITT always. TOT/LATE via IV if assignment is a valid instrument for take-up (exclusion: assignment affects Y only through D). Do not drop non-compliers.

## Phase 3 — Spillovers and ethics

If treated units affect controls, ITT is not a no-spillover ATE. Randomise at a higher level or measure exposure.

Ethics: consent, equipoise, harm. Do not randomise a known harmful denial without a framework.

## Phase 4 — Workflow

1. Estimand ITT.
2. Power/MDE.
3. Analyse as assigned.
4. Secondary LATE if compliance <1 and exclusion holds.

## Anti-patterns

- Treated-only means
- Ignoring clusters
- Underpowered "null"
- Peeking (see experiments skill in DS)

## Validation gate

Assigned analysis; unit named; ITT primary.

## Final principle

Randomisation identifies the effect of the randomisation. Everything else is extra assumptions.
