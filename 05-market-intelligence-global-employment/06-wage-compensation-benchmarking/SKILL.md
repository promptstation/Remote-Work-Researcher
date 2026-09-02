---
name: wage-compensation-benchmarking
description: Produce compensation benchmarks with a defined market, percentile, and total-rewards caveat — survey vs advertised vs administrative pay, PPP/FX. Use whenever the user needs salary bands, pay intelligence, or "what should we pay in country X." Apply even if they paste a job-ad salary.
compatibility: Wage surveys, LFS earnings, job-ad pay, total rewards.
metadata:
  author: Promptstation
  version: 1.0.0
  category: market-intelligence
  course: 05-market-intelligence-global-employment
  section: 06-wage-compensation-benchmarking
---

# Wage, Compensation, and Benchmarking Intelligence

## Mission

A pay number without a market, percentile, and what is included (base, bonus, benefits, hours) is not a benchmark. Posted salaries are offers, not accepted pay. Convert currency with a named FX or PPP rule.

## Core output

A **Pay Benchmark**: market definition, source, base vs total cash vs total rewards, percentile, n and date, caveats.

## Phase 1 — Market and object

Same taxonomy and geography as the intelligence requirement. Percentile: P50 is not a band. Hours: monthly vs hourly. Benefits (health, pension, 13th month, leave) can dominate cross-country cash gaps.

## Phase 2 — Sources

Employer surveys (best when sample is named), LFS earnings, admin tax, job-ad scraped pay (selection to firms that post). Do not average them. Prefer one primary, one check.

PPP for living-standard comparisons; spot FX for employer budget in home currency. Say which.

## Phase 3 — Workflow

1. Object (base / TTC / TR).
2. Market.
3. Primary source.
4. Percentiles + date.
5. What would move the number (seniority mix, FX).

## Anti-patterns

- One Glassdoor screenshot
- Mixing base and CTC
- PPP vs FX confusion
- National mean for a city role
- Ignoring hours

## Validation gate

Object named; market named; source+date; percentile; benefits caveat if cross-country.

## Final principle

Compensation intelligence is a defined price in a defined market. Everything else is gossip about pay.
