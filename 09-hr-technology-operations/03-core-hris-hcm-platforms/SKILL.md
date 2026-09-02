---
name: core-hris-hcm-platforms
description: Decide what belongs in the HR system of record versus satellite tools — configuration vs customisation. Use whenever the user is choosing, configuring, or fighting an HRIS/HCM. Apply even if they want a custom feature first.
compatibility: Major HCM platforms conceptually; vendor-agnostic.
metadata:
  author: Promptstation
  version: 1.0.0
  category: hr-technology
  course: 09-hr-technology-operations
  section: 03-core-hris-hcm-platforms
---

# Core HRIS / HCM Platforms

## Mission

The HRIS is the system of record for people, jobs, and events. Satellites (ATS, payroll engines, LMS) should subscribe, not fork the truth. Configure before customising; custom is a forever tax.

## Core output

A **SoR Decision**: objects in core, objects in satellites, integration, config vs custom, workflow owners.

## Phase 1 — What core owns

Org, jobs, person, events (hire, transfer, terminate), workflow approvals, foundational eligibility. If two systems own "manager," access and pay will diverge.

## Phase 2 — Config vs custom

Use delivered events and fields when they fit. Custom fields and code for every exception will block upgrades. Exceptions belong in a documented process, not always in code.

## Phase 3 — Workflow

1. Object ownership table.
2. Event list.
3. Config first.
4. Custom only with an owner and a test.

## Anti-patterns

- Dual SoR
- Customising instead of changing policy
- Shadow Excel as the real HRIS
- Every country a unique fork without a global design

## Validation gate

SoR named per object; custom justified; events listed.

## Final principle

One system of record per fact. Everything else is a copy that will drift.
