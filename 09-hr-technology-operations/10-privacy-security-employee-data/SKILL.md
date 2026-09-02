---
name: privacy-security-employee-data
description: Set access and retention rules for HR data — RBAC, minimisation, vendor risk. Use whenever employee data are stored, exported, or sent to a vendor. Apply even if someone wants the whole roster in a spreadsheet.
compatibility: Security reviews; not jurisdiction-specific legal advice.
metadata:
  author: Promptstation
  version: 1.0.0
  category: hr-technology
  course: 09-hr-technology-operations
  section: 10-privacy-security-employee-data
---

# Privacy, Security, Access, and Employee Data Protection

## Mission

Employee data are sensitive: IDs, bank, health, performance. Access is role-based and logged. Exports are still copies. Vendors are processors. Minimisation beats a bigger lake.

## Core output

A **Data-Protection Spec**: data classes, roles, retention, vendor clauses, export rules.

## Phase 1 — Class

Public, internal, confidential, special (health, union, ethnicity if collected). Different access.

## Phase 2 — Access

RBAC, need-to-know, break-glass, quarterly access recertification. HRBP sees their pop, not the company. Payroll sees pay, not performance comments.

## Phase 3 — Retention and vendors

Candidate data ≠ employee data. Leaver data kept for legal minimum, not forever. DPA, location of processing, subprocessors.

## Phase 4 — Workflow

1. Classify.
2. RBAC matrix.
3. Retention.
4. Export/download controls.
5. Refuse bulk PII in chat/email.

## Anti-patterns

- Roster in a shared drive
- God-mode accounts
- Infinite ATS retention
- Unvetted "AI HR" vendor getting the dump

## Validation gate

RBAC; retention; vendor; no casual PII dumps.

## Final principle

If a spreadsheet of everyone can leave the building, you do not have HR security. You have a leak waiting for a filename.
