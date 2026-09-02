---
name: hr-data-model-master-data
description: Specify employee/job data models with effective dates and unique IDs — person, assignment, org. Use whenever HR data are messy, analytics disagree with payroll, or a system is being implemented. Apply even if they "just need a headcount."
compatibility: HCM data models.
metadata:
  author: Promptstation
  version: 1.0.0
  category: hr-technology
  course: 09-hr-technology-operations
  section: 02-hr-data-model-master-data
---

# HR Data Model, Employee Records, and Master Data

## Mission

Person ≠ assignment ≠ position ≠ org unit. Time-effective records are the truth. Without unique IDs and effective dating, you will double-count humans and mis-pay them.

## Core output

A **Data-Model Spec**: entities, keys, effective dating, mandatory fields, quality rules.

## Phase 1 — Entities

Person (legal identity), employment, assignment/job, position, org, location, pay group. Contractors vs employees. Multiple assignments.

## Phase 2 — Time

Effective start/end, not overwriting history. Headcount on a date is a point-in-time query, not a live table dump.

## Phase 3 — Quality

One person ID. No duplicate emails as keys. Mandatory fields for payroll vs nice-to-have. Supervisory org that matches reality.

## Phase 4 — Workflow

1. Entities and keys.
2. Effective dating.
3. Quality rules and owners.
4. Freeze before analytics or payroll go-live.

## Anti-patterns

- Name as key
- Overwriting history
- Headcount from a spreadsheet export without a date
- Job title free text as the org structure

## Validation gate

Keys; effective dates; person vs assignment distinguished.

## Final principle

HR operations run on master data. If the record is wrong, every downstream system is professionally wrong.
