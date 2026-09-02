---
name: recruiting-operations-ats
description: Design or diagnose ATS-backed recruiting operations — requisition-to-hire, fairness, retention of candidate data. Use whenever the user runs hiring operations or an ATS. Apply even if they treat the ATS as a CV folder.
compatibility: ATS operations; pair with I-O selection skill for validity.
metadata:
  author: Promptstation
  version: 1.0.0
  category: hr-technology
  course: 09-hr-technology-operations
  section: 04-recruiting-operations-ats
---

# Recruiting Operations and ATS

## Mission

An ATS is a workflow: requisition, post, apply, screen, interview, offer, hire event into HRIS. If stages are optional and data are junk, you cannot report time-to-fill or adverse impact. Operations make I-O selection real.

## Core output

A **Recruiting Ops Spec**: stages, required fields, SLAs, integrations to HRIS, data retention, reports.

## Phase 1 — Workflow

Req approval → post → apply → screen (structured) → interview → offer → accept → hire event. Skip-stage culture kills analytics.

## Phase 2 — Data and fairness

Structured reasons for reject. Source tracking. Retention limits for candidate PII. Do not keep CVs forever "just in case." Knockout questions must be job-related (I-O skill).

## Phase 3 — Workflow

1. Stage model.
2. Mandatory data.
3. SLA and owners.
4. Hire event to HRIS (no rekey).
5. Reports: funnel, time, source, adverse impact.

## Anti-patterns

- Email hiring with ATS as archive
- Rekeying hires
- Infinite candidate data
- Unstructured reject reasons

## Validation gate

Stages; HRIS hire event; retention; structured rejects.

## Final principle

If it did not happen in the ATS, it did not happen for operations. Design the path people will actually follow.
