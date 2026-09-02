---
name: data-acquisition-sql-apis
description: Obtain analysis-ready extracts via SQL, APIs, files, and administrative sources without silent duplication, wrong grain, or unethical collection. Use whenever the user needs data pulled, joined, scraped, requested from an API, exported from a warehouse, or combined from multiple systems. Apply even if they only paste a schema or say "get the data for this."
compatibility: SQL warehouses, REST/GraphQL APIs, CSV/Parquet/JSON, official statistical APIs; respect robots, ToS, and privacy law.
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 02-data-acquisition-sql-apis
---

# Data Acquisition, SQL, APIs, and Ethical Collection

## Mission

Get the right rows at the right grain from the right system, with a documented extract that can be repeated. Collection is part of inference: who is missing from the extract is already a bias.

## When this skill governs

Use when pulling from databases, APIs, files, statistical agencies, or web sources, or when reconciling two systems that disagree.

## Core output

Deliver an **Extract Spec**:

1. Source systems and owners
2. Grain and primary keys
3. Population rule (who is in)
4. Time window and time zone
5. Join plan and expected row-count change
6. Fields, PII flags, and minimisation
7. Legal/ethical basis
8. Repeatable query or request
9. Row-count reconciliation

## Phase 1 — Choose the source on purpose

- **Operational DB:** current state, often overwritten, not historical
- **Warehouse / event log:** historical, modelled grains, delay
- **API:** rate limits, pagination, partial fields
- **Files / dumps:** version, delimiter, encoding
- **Admin registers:** coverage = programme rules
- **Web:** last resort; ToS, robots, personal data, instability

Prefer official APIs and warehouses over scraping. If you scrape, say why nothing else works.

## Phase 2 — SQL that respects grain

Write the grain in a comment before the SELECT.

Rules:

- joins are multiplied unless you know the relationship (1:1, 1:N, N:N)
- aggregate in subqueries before joining 1:N
- filter on the correct date column (created vs effective vs loaded)
- explicit LEFT vs INNER; INNER drops non-matches silently
- COUNT(*), COUNT(pk), COUNT(DISTINCT pk) are different diagnostics
- never SELECT * in a research extract

Reconcile: rows in → rows out at each join. If you cannot explain a row-count jump, you do not have the extract yet.

## Phase 3 — APIs and files

- paginate until empty; do not assume one page
- handle 429s; store ETags / cursors
- freeze a pull timestamp
- parse JSON to tables at a named grain; nested arrays explode
- record encoding, delimiter, and null sentinels for files
- prefer Parquet/CSV with a schema over Excel as a source of truth

## Phase 4 — Ethics and law

Do not collect personal data because it is reachable.

- minimisation: only fields the frame needs
- purpose limitation
- robots.txt and terms; authenticated spaces are not fair game
- special-category data needs an explicit basis
- public web is not "not personal"

If the user asks to scrape personal profiles, emails, or behind-login content in violation of terms, refuse that path and propose a lawful source.

## Phase 5 — Research workflow

1. Restate the analysis grain.
2. Map tables/endpoints to that grain.
3. Draft the join/API plan with expected counts.
4. Pull a small sample; check keys and time.
5. Full pull; freeze; checksum; document.
6. Hand a clean extract log to wrangling.

## Anti-patterns

- SELECT * and hope
- Joining then wondering why the mean doubled
- Scraping when an API or FOIA/official download exists
- Mixing time zones silently
- Storing extra PII "in case"
- One-off GUI clicks with no query to rerun
- Treating the warehouse's "customer" table as people without checking duplicates

## Decision heuristic

1. What grain?
2. Which system is the system of record for that grain?
3. What join will multiply rows?
4. What is the legal basis?
5. Can someone rerun this pull?

## Validation gate

- Grain and keys named
- Join row-counts explained
- Time window and zone named
- PII minimised
- Repeatable query/request stored
- No ToS-violating scrape

## Final principle

Acquisition is sampling. A pretty model on the wrong extract is a wrong answer with extra steps.
