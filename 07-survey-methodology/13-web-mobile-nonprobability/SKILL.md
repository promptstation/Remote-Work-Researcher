---
name: web-mobile-nonprobability
description: Use or refuse nonprobability samples with explicit inference limits — access panels, opt-in, river samples. Use whenever the user has a web panel or convenience sample and wants population numbers. Apply even if the panel is "nationally matched."
compatibility: Opt-in panels; model-based inference with limits.
metadata:
  author: Promptstation
  version: 1.0.0
  category: survey-methodology
  course: 07-survey-methodology
  section: 13-web-mobile-nonprobability
---

# Web, Mobile, and Nonprobability Samples

## Mission

Unknown selection probabilities mean design-based inference does not apply. Matching on age×sex×region is not a probability sample. You may still describe respondents, or use model-based inference with a stated risk. You may not report a ±3pp as if it were an SRS of the country.

## Core output

An **Inference Limit**: how people entered, what matching was done, what you may claim, what you may not.

## Phase 1 — Types

Access panels, river, snowball, customer lists, social ads. Bots and professional respondents on cheap web.

## Phase 2 — What is allowed

- associations inside the sample (still watch selection)
- experiments randomised inside the sample (internal validity ≠ population)
- population totals only with a selection model you are willing to defend (and usually not for high-stakes official stats)

MRP and similar can help and can also hide selection on unobservables.

## Phase 3 — Workflow

1. Entry path.
2. Refuse design-based MOE.
3. If the user needs official-quality prevalence, recommend a probability survey.
4. If they proceed, label "opt-in panel, model-based, not a probability sample."

## Anti-patterns

- Fake MOEs on panels
- "Quota therefore representative"
- Population claims from Twitter/Facebook samples

## Validation gate

Nonprobability labelled; no fake design-based CI; claims bounded.

## Final principle

A matched panel is a modelled convenience sample. Call it that, or do not infer to the nation.
