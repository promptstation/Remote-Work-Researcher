---
name: global-employment-data-sources
description: Pick employment data sources that match the concept — ILOSTAT, OECD, NSOs, LFS, vacancies, admin, platforms — and document vintage and comparability. Use whenever the user needs cross-country jobs data or to reconcile conflicting employment numbers. Apply even if they paste a headline statistic.
compatibility: Public statistical systems and documented private data; never invent series.
metadata:
  author: Promptstation
  version: 1.0.0
  category: market-intelligence
  course: 05-market-intelligence-global-employment
  section: 02-global-employment-data-sources
---

# Global Employment Data Sources and Provenance

## Mission

Every employment number has a factory. Official LFS, establishment surveys, ILO modelled estimates, vacancy platforms, and payroll APIs do not measure the same object. Provenance is the first sentence of intelligence.

## Core output

A **Source Card**: concept, source, series name, vintage, adjustment (SA/NSA), modelled vs reported, comparability notes.

## Phase 1 — Match concept to factory

- stocks of people: LFS / ILOSTAT / CPS-like
- jobs in firms: establishment / payroll
- unemployment: LFS, not claimant counts unless labelled
- vacancies: JOLTS-like or job-ad indexes (ads ≠ vacancies ≠ hires)
- wages: LFS, establishment earnings, tax, job-ad posted pay
- cross-country panels: ILO modelled — label as such

Use the labour-measurement skill for definitions. Here, choose the factory.

## Phase 2 — Provenance rules

Cite agency, table, download date, and whether 13th vs 19th ICLS. Do not mix modelled and official in a rank table without flags. Do not splice job-ad indexes to LFS employment.

Private platform data: coverage is the platform's users. State that.

## Phase 3 — Workflow

1. Concept.
2. Best official source.
3. One complementary source if needed (e.g. ads for demand now).
4. Source card in the brief.
5. Reconcile conflicts as object differences, not as "data quality" alone.

## Anti-patterns

- Unlabelled ILO modelled ranks
- Job ads as employment
- Mixing SA monthly with annual official
- Undated screenshots

## Validation gate

Series named; vintage named; modelled vs official labelled; concept match.

## Final principle

An un-sourced employment number is a rumour. Intelligence cites the factory.
