---
name: people-analytics-stack-reporting
description: Build HR metric dictionaries and reporting paths that match the data model — headcount/FTE, warehouse vs live HRIS. Use whenever HR numbers disagree or a dashboard is requested. Apply even if they want "just pull headcount."
compatibility: HRIS reports and warehouses; pair with DS communication skill.
metadata:
  author: Promptstation
  version: 1.0.0
  category: hr-technology
  course: 09-hr-technology-operations
  section: 08-people-analytics-stack-reporting
---

# People Analytics Stack and Reporting Operations

## Mission

Headcount is a definition: as-of date, employee vs contractor, FTE vs bodies, paid vs unpaid leave. Without a metric dictionary, every dashboard is a different census. Live HRIS screens are not a warehouse.

## Core output

A **Metric Dictionary + Path**: definitions, as-of rules, source, refresh, access.

## Phase 1 — Definitions

Headcount, FTE, joiners, leavers, regrettable attrition, time-to-fill, offer-accept, absence rate. Each: numerator, denominator, population, date logic.

## Phase 2 — Stack

Operational questions: HRIS. Historical/analytics: warehouse with snapshots. Do not mix a live org tree with last month's pay.

## Phase 3 — Workflow

1. Decision questions.
2. Dictionary.
3. Snapshot cadence.
4. Governed self-service vs certified reports.

## Anti-patterns

- Three headcounts
- No as-of date
- Excel extracts as the warehouse
- Predictive "flight risk" without the DS ethics skill

## Validation gate

Dictionary; as-of; source named; live vs snapshot distinguished.

## Final principle

People analytics is operations plus definitions. If the definition is not written, the number is a rumour with a chart.
