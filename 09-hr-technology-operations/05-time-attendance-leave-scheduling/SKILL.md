---
name: time-attendance-leave-scheduling
description: Specify time, leave, and scheduling rules that a system can execute without becoming a pay error factory. Use whenever the user has timesheets, shifts, overtime, or leave systems. Apply even if they think payroll "just knows."
compatibility: Time/leave/WFM systems.
metadata:
  author: Promptstation
  version: 1.0.0
  category: hr-technology
  course: 09-hr-technology-operations
  section: 05-time-attendance-leave-scheduling
---

# Time, Attendance, Leave, and Scheduling Operations

## Mission

Time is a payroll input and a legal record. Ambiguous overtime, unapproved leave, and shadow rotas will hit pay and compliance. Rules must be executable: who approves, what rounds, what is a day.

## Core output

A **Time-and-Leave Spec**: capture method, rounding, OT rules, leave types, approval, exceptions, feed to payroll.

## Phase 1 — Capture

Clock, badge, app, honour system, manager entry. Each has fraud and error modes. Scheduling must match captured time or you invent OT.

## Phase 2 — Rules

Leave balances effective-dated. Public holidays by location. Overtime by jurisdiction. Rounding disclosed. Retro when rules change.

## Phase 3 — Workflow

1. Write rules in examples (worked 8:07–17:12 Friday...).
2. Configure; test those examples.
3. Lock the payroll feed.
4. Exception queue with SLA.

## Anti-patterns

- Policy PDF not in the system
- Managers editing time after payroll cutoff without retro
- Leave in spreadsheets
- Scheduling in WhatsApp

## Validation gate

Example-tested rules; payroll feed; exception path.

## Final principle

If the rule cannot be shown in a worked example, the system cannot pay it correctly.
