---
name: target-population-frames-coverage
description: Define target populations and diagnose frame coverage — who is missing. Use whenever the user says "the population," uses a list, or compares a sample to a country. Apply even if they have a "national" online panel.
compatibility: Frames: household, RDD, registers, web, establishments.
metadata:
  author: Promptstation
  version: 1.0.0
  category: survey-methodology
  course: 07-survey-methodology
  section: 02-target-population-frames-coverage
---

# Target Population, Frames, and Coverage

## Mission

Target population is who you want to talk about. Frame is who could be selected. Coverage error is the gap. A mobile-web panel of 18+ urban users is not "adults."

## Core output

A **Coverage Note**: target, frame, ineligibles, undercoverage, multiplicity, implication for estimates.

## Phase 1 — Write the target

Age, geography, civilian, household vs people, establishments vs firms. "Voters" ≠ adults.

## Phase 2 — Frame

Household listings, RDD, population register, customer list, web ads. Dual-frame when one misses a group (landline+mobile historically). Multiplicity: people with two phones.

## Phase 3 — Workflow

1. Target sentence.
2. Frame source.
3. Who is missing (no phone, informal, institutions, no internet).
4. Whether to dual-frame, screen, or narrow the target.

## Anti-patterns

- Panel as population
- Customer list as "market"
- Ignoring institutions (dorms, barracks) when relevant

## Validation gate

Target ≠ frame distinguished; missing groups named.

## Final principle

You can only infer to the population your frame can see, plus a story about the rest. Without the story, shrink the target.
