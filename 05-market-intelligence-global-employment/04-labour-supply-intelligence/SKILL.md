---
name: labour-supply-intelligence
description: Build a labour-supply picture for a role and geography — population, participation, pipelines, migration, inactivity. Use whenever the user asks if there are enough people, about talent supply, graduates, or immigration as supply. Apply even if they only look at the unemployment rate.
compatibility: Demographic and LFS sources.
metadata:
  author: Promptstation
  version: 1.0.0
  category: market-intelligence
  course: 05-market-intelligence-global-employment
  section: 04-labour-supply-intelligence
---

# Labour Supply Intelligence

## Mission

Supply is who could do this work, not who is unemployed. Combine working-age population, participation, qualified pipelines, migrants, and hours. A low unemployment rate with a thin pipeline is a supply problem; a high unemployment rate in the wrong occupation is not supply of this role.

## Core output

A **Supply Picture**: qualified stock, flow (graduates, immigrants, reskillers), participation constraints, substitutes, 3–5 year demographic tilt.

## Phase 1 — Stock and flow

Stock: people in the occupation + adjacent occupations + qualified inactives.  
Flow: education completions, visas, internal mobility.

Unemployment in the occupation is a slice, not the supply.

## Phase 2 — Constraints

Licensing, language, location, care burdens, wages below reservation, ageing. Female participation and informal work change "available" in many markets (labour-supply and informality skills).

## Phase 3 — Workflow

1. Define qualified.
2. Stock from LFS/census.
3. Flows from education and migration stats.
4. Constraints.
5. So-what for hiring plan.

## Anti-patterns

- National unemployment as role supply
- Ignoring pipelines
- Counting degrees as skills
- Forgetting hours and participation

## Validation gate

Qualified defined; stock and flow both present; unemployment not used alone.

## Final principle

Supply is a qualified stock plus a pipeline minus constraints. Unemployment is a footnote in that sentence.
