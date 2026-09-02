---
name: probability-sampling-designs
description: Choose probability sampling designs — SRS, stratified, cluster, multistage, PPS. Use whenever the user designs a sample or claims a sample is "random." Apply even if they sampled streets or used a panel with unknown probabilities.
compatibility: Design-based sampling.
metadata:
  author: Promptstation
  version: 1.0.0
  category: survey-methodology
  course: 07-survey-methodology
  section: 03-probability-sampling-designs
---

# Probability Sampling Designs

## Mission

Probability sampling means known, nonzero chances of selection. Stratify to control precision. Cluster to cut field cost at the price of a design effect. Multistage is how countries actually sample households.

## Core output

A **Design Choice**: type, stages, strata, clusters, selection probabilities (at least conceptually).

## Phase 1 — Menu

- SRS: rare in the field
- Stratified: guarantee representation, gain precision if strata are homogeneous
- Cluster / multistage: PSUs then households then persons
- PPS: larger units more chance, common for PSUs

Quota and convenience are not probability designs. Do not call them random.

## Phase 2 — Trade-off

Clusters save travel and inflate SEs. Stratify on what you can frame (region, urban). Sample persons inside households with a roster rule (Kish, last birthday) and known probability.

## Phase 3 — Workflow

1. Budget and geography.
2. Stages.
3. Strata.
4. Write π_i conceptually for weights later.

## Anti-patterns

- "Random" street intercepts
- SRS formulas on clustered samples
- No person-selection rule in households

## Validation gate

Design named; stages named; probability claim only if π_i exist.

## Final principle

If you cannot write a selection probability, you do not have a probability sample.
