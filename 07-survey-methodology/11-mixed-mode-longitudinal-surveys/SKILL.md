---
name: mixed-mode-longitudinal-surveys
description: Design or analyse mixed-mode and panel surveys without ignoring mode effects and attrition. Use whenever the user has waves, panels, or mixed-mode fielding. Apply even if they treat wave 2 as a fresh cross-section.
compatibility: Panels and mixed-mode studies.
metadata:
  author: Promptstation
  version: 1.0.0
  category: survey-methodology
  course: 07-survey-methodology
  section: 11-mixed-mode-longitudinal-surveys
---

# Mixed-Mode and Longitudinal Surveys

## Mission

Repeating a survey adds attrition, conditioning, and mode changes. Change in estimates can be real change, who left, or how you asked. Keep those separate.

## Core output

A **Panel/Mixed-Mode Note**: waves, mode by wave, attrition, conditioning risk, estimand (cross-section vs change).

## Phase 1 — Estimands

Repeated cross-section: each wave represents the population (with its own error).  
Panel change: the same people; attrition bias is first-order.

Do not use a balanced panel as the population without weights for attrition.

## Phase 2 — Problems

- attrition correlated with Y
- panel conditioning (people learn the questionnaire)
- mode switches between waves
- time-in-sample in rotating panels

## Phase 3 — Workflow

1. Estimand.
2. Attrition table vs frame.
3. Mode log.
4. Weights for NR/attrition.
5. Sensitivity of the trend to mode.

## Anti-patterns

- Complete-case panel as population
- Silent mode switch
- Conditioning ignored on knowledge items

## Validation gate

Estimand named; attrition described; mode history named.

## Final principle

A wave is not a photocopy of the last wave. Document what changed in who and how, or do not call it a trend.
