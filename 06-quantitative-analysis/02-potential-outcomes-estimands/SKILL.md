---
name: potential-outcomes-estimands
description: Name causal estimands — ATE, ATT, LATE, ITT — and who they apply to. Use whenever the user says "the effect," mixes ITT and TOT, or wants to apply an IV estimate to everyone. Apply even if they only report "the treatment effect."
compatibility: Potential-outcomes language.
metadata:
  author: Promptstation
  version: 1.0.0
  category: quantitative-analysis
  course: 06-quantitative-analysis
  section: 02-potential-outcomes-estimands
---

# Potential Outcomes and Causal Estimands

## Mission

Each unit has Y(1) and Y(0). You never see both. An estimand is a contrast of these for a defined population. ATE ≠ ATT ≠ LATE ≠ ITT. The decision must match the estimand.

## Core output

An **Estimand Statement**: population, treatment contrast, which of ATE/ATT/LATE/ITT, why that is the decision-relevant one.

## Phase 1 — Contrasts

- **ATE:** all units in the study population
- **ATT:** those who received treatment
- **ATC:** the untreated
- **LATE/CATE for compliers:** those whose D changes with an instrument
- **ITT:** effect of assignment, not of take-up

Policy that offers a programme often wants ITT. Effect of taking the programme wants TOT with extra assumptions. Scaling a LATE to "everyone" is a new, usually false, claim.

## Phase 2 — Workflow

1. Who could be treated in the decision?
2. Is the action assignment or take-up?
3. Pick estimand.
4. Refuse to call LATE "the effect of D."

## Anti-patterns

- One "treatment effect"
- IV estimate applied to always-takers
- ITT sold as efficacy of the drug/training as taken

## Validation gate

Estimand acronym or full name; population; contrast.

## Final principle

If you cannot say for whom the contrast is defined, you do not have an effect. You have a difference.
