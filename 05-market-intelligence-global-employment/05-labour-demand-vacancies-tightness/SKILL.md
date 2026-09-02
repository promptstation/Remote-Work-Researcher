---
name: labour-demand-vacancies-tightness
description: Read labour demand and tightness from employment, vacancies, job ads, and hires without treating ads as a census. Use whenever the user asks if hiring is hot, about shortages, vacancies, or demand for a role. Apply even if they only have a job-board spike.
compatibility: Vacancy surveys, JOLTS-like data, job-ad indexes, LFS employment.
metadata:
  author: Promptstation
  version: 1.0.0
  category: market-intelligence
  course: 05-market-intelligence-global-employment
  section: 05-labour-demand-vacancies-tightness
---

# Labour Demand, Vacancies, and Tightness

## Mission

Demand is firms' desired hires at going terms. Vacancies, ads, employment change, and hires are noisy views of it. Tightness is vacancies relative to available workers. A posting spike can be churn, multi-posting, or genuine demand.

## Core output

A **Demand-and-Tightness Note**: employment trend, vacancy/ad trend, hires/quits if available, tightness, interpretation (growth vs churn vs artefact).

## Phase 1 — Series

- employment by occupation/industry (slow, official)
- vacancy surveys (closer to true vacancies)
- online ads (fast, biased to formal/online)
- hires and quits (churn vs net demand)

Net employment up with high ads: growth. Ads up, employment flat, quits up: churn. Ads up, nothing else: platform artefact.

## Phase 2 — Shortage claims

A shortage needs rising relative wages or unfilled vacancies with search effort — not just employers saying hiring is "hard" at the current wage. Pair this skill with wage intelligence.

## Phase 3 — Workflow

1. Official employment direction.
2. Vacancy or ads with bias note.
3. Tightness vs a base period.
4. Churn vs growth.
5. Confidence.

## Anti-patterns

- Ads as jobs
- Shortage without wages
- Ignoring multi-posting
- National tightness for a local occupation

## Validation gate

More than one demand view; ads bias stated; churn vs growth considered.

## Final principle

Demand is a tightness story, not a job-ad screenshot.
