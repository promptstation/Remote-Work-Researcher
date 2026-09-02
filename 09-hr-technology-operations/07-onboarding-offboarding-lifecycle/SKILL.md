---
name: onboarding-offboarding-lifecycle
description: Design joiner-mover-leaver events so access, pay, and records change together. Use whenever onboarding is chaotic, leavers keep access, or movers vanish between systems. Apply even if they have a welcome email.
compatibility: IAM + HRIS + IT + facilities handoffs.
metadata:
  author: Promptstation
  version: 1.0.0
  category: hr-technology
  course: 09-hr-technology-operations
  section: 07-onboarding-offboarding-lifecycle
---

# Onboarding, Offboarding, and Employee Lifecycle Events

## Mission

A lifecycle event is a coordinated change: record, pay, access, assets, compliance. If HRIS says terminated and AD says active, that is an incident. Movers (transfer, location, manager) fail more often than joiners.

## Core output

An **Event Playbook**: trigger, systems touched, RACI, timing vs start/end date, evidence of completion.

## Phase 1 — Joiners

Offer accept → hire event → ID → access day-0 → payroll → equipment. Start date vs event date. Contractors on a different path, still with an end date.

## Phase 2 — Leavers

Terminate event → access kill (same day) → pay final → asset return → retention of records. Revoke first for risky leavers.

## Phase 3 — Movers

Org, location, pay group, access profile. Partial movers (manager only) still need a workflow.

## Phase 4 — Workflow

1. Event types.
2. System list.
3. Same-day access rule.
4. Audit: HRIS vs IAM vs payroll weekly.

## Anti-patterns

- Access by email request only
- No contractor end dates
- Welcome culture, goodbye chaos
- Transfers as "just update the spreadsheet"

## Validation gate

RACI; access tied to HRIS event; leaver same-day; mover path.

## Final principle

Identity follows the HR event. If it does not, you do not have a lifecycle. You have a collection of tickets.
