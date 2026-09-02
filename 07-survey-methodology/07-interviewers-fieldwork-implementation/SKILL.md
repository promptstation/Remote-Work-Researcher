---
name: interviewers-fieldwork-implementation
description: Specify fieldwork controls — interviewer effects, training, paradata, falsification. Use whenever a survey uses interviewers or a field vendor. Apply even if the vendor is "reputable."
compatibility: F2F and CATI operations.
metadata:
  author: Promptstation
  version: 1.0.0
  category: survey-methodology
  course: 07-survey-methodology
  section: 07-interviewers-fieldwork-implementation
---

# Interviewers, Fieldwork, and Implementation

## Mission

Interviewers are part of the instrument. They generate variance and sometimes bias (probing, presence, fabrication). Fieldwork without paradata is a black box.

## Core output

A **Fieldwork Spec**: training, monitoring, back-checks, paradata, interviewer-variance plan.

## Phase 1 — Effects

Interviewer variance on attitudinal items can dwarf sampling variance. Standardise scripts, train, randomise interviewers to areas when possible, include interviewer IDs in analysis.

## Phase 2 — Quality

GPS/time stamps, interview length, audio audits where legal, random back-checks. Fabrication is a real risk under piece-rate pay. Do not pay only on completed interviews without quality.

## Phase 3 — Workflow

1. Protocol.
2. Training + certification.
3. Live monitoring rules.
4. Interviewer ID on file.

## Anti-patterns

- Piece-rate only
- No back-checks
- Ignoring interviewer clustering in SEs
- "The vendor handles quality"

## Validation gate

Monitoring named; interviewer IDs; back-check plan.

## Final principle

A beautiful sample design dies in the field. Paradata is how you see the death.
