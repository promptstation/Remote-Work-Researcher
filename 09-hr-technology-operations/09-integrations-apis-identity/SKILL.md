---
name: integrations-apis-identity
description: Specify HR integrations with an owner, a key, and a recon rule — HR as identity source to IT/finance/benefits. Use whenever systems disagree or a new integration is planned. Apply even if the vendor says "we have an API."
compatibility: HRIS integrations; identity.
metadata:
  author: Promptstation
  version: 1.0.0
  category: hr-technology
  course: 09-hr-technology-operations
  section: 09-integrations-apis-identity
---

# Integrations, APIs, and Identity

## Mission

Every interface needs a source of truth, a join key, a schedule, an error queue, and a recon. "We have an API" is not an integration. HR person ID should seed identity; email is a bad primary key.

## Core output

An **Integration Spec**: producer, consumer, payload, key, cadence, failure, recon.

## Phase 1 — Pattern

HRIS → IAM (joiners/leavers), HRIS → payroll, ATS → HRIS hire, HRIS → benefits, HRIS → finance cost centres. Direction matters. Bidirectional without rules = ping-pong corruption.

## Phase 2 — Operations

Retries, dead letters, alerting, owner. Recon counts daily (hires today in A vs B). Schema versioning.

## Phase 3 — Workflow

1. Object ownership.
2. Key.
3. Cadence vs event-driven.
4. Recon + alert.
5. Do not go live without the recon.

## Anti-patterns

- Email as key
- File drop with no recon
- Both systems editable
- Silent API failures

## Validation gate

Key; owner; recon; direction.

## Final principle

An integration that cannot be reconciled is a future incident on a timer.
