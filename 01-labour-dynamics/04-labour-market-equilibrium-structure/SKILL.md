---
name: labour-market-equilibrium-structure
description: Determine how wages and employment are set under competitive equilibrium, cobweb dynamics, monopsony, bargaining, and search frictions. Use whenever the user asks who sets wages, whether a labour market clears, how a tax or migration shock splits between wages and jobs, whether employers have wage-setting power, or which model (competitive, monopsony, union, search) fits a market. Apply even if they only ask "why aren't wages falling" or "who bears this payroll tax."
compatibility: Works with wage-employment data, concentration measures, and institutional descriptions of bargaining and search.
metadata:
  author: Promptstation
  version: 1.0.0
  category: labour-dynamics
  course: 01-labour-dynamics
  section: 04-labour-market-equilibrium-structure
---

# Competitive Equilibrium, Imperfect Competition, and Market Structure

## Mission

Pick the labour-market structure before predicting a wage or employment effect. The same shock — a payroll tax, a migration inflow, a demand boom — produces different incidence under competition, monopsony, bargaining, and search. Structure is not decoration; it is the model.

Do not default to supply-and-demand clearing. Labour markets often have residual unemployment, wage-setting firms, and bargained wages. Default to competition only when the evidence supports it.

## When this skill governs

Use when the question is how wages and employment are jointly determined, who has wage-setting power, how a shock is split between price and quantity, or which textbook diagram is the right one.

## Core output

Deliver a **Market Structure Note**:

1. Market definition (occupation, industry, location, skill)
2. Candidate structures and the evidence for each
3. Chosen working model
4. Shock → wage and employment prediction under that model
5. Incidence
6. What evidence would switch the model

## Phase 1 — Define the market

Wages are set in a market with boundaries:

- occupation / skill
- industry
- geography and commuting
- contract type (formal wage employment vs informal)

A "national labour market" is usually too coarse. A nurse market in one city is not the same object as "Kenya labour." State the market before choosing structure.

## Phase 2 — Competitive benchmark

In a competitive labour market:

- firms take \(w\) as given
- workers take \(w\) as given
- equilibrium equates labour supply and demand
- no involuntary unemployment at the equilibrium wage
- incidence of a payroll tax is independent of statutory assignment and depends on elasticities

Use this as the baseline, then ask what fails.

Failures that reject pure competition as the working model:

- persistent vacancies and unemployment together
- employer concentration with wage markdowns
- bargained or administered wages
- large residuals after controlling for productivity that look like rents

## Phase 3 — Dynamics in the competitive frame

Cobweb and lagged supply (training pipelines) can produce oscillating wages and employment even under competition. Licensing, schooling lags, and construction cycles are classic.

Do not treat every overshoot as monopsony or union power. Check whether supply is slow.

## Phase 4 — Monopsony and oligopsony

Wage-setting employers face upward-sloping labour supply to the firm.

Diagnostics:

- labour-supply elasticity to the firm (not to the market)
- employer concentration (HHI in a local occupation)
- recruiting intensity and wage posting
- job differentiation, moving costs, non-competes

Predictions:

- markdown of wage below MRP
- employment below competitive level
- a binding wage floor can raise both wages and employment over a range
- payroll-tax incidence and pass-through differ from competition

Do not infer monopsony from a zero employment effect of a minimum wage alone. That result is also consistent with low competitive demand elasticity or with measurement problems.

## Phase 5 — Monopoly unions and bargaining

Wages may be bargained:

- monopoly union: union picks wage on the labour-demand curve
- right-to-manage: bargain wage, firm picks employment
- efficient bargaining: wage and employment both bargained (contract curve)

Coverage, coordination (firm, industry, national), and threat points change the outcome. Coordinated bargaining can compress wages without the same employment cost as fragmented high-union-wage islands.

If the market is unionised, competitive diagrams will mis-state incidence.

## Phase 6 — Search and matching as structure

With search frictions, the market does not clear in the classical sense. Vacancies and unemployment coexist. Wages split a match surplus (Nash bargaining or wage posting).

Use this structure when the question involves tightness, duration, job-finding rates, or why wages are rigid. Detailed flow accounting belongs to the unemployment/search skill; here you only decide that search is the right structure.

## Phase 7 — Mapping shocks under each structure

| Shock | Competition | Monopsony | Bargaining | Search |
| --- | --- | --- | --- | --- |
| Labour supply increase | w down, E up | w down (less), E up | depends on contract | tightness down, w down |
| Payroll tax | split by elasticities | more on the side with less power | bargained incidence | surplus shrinks, tightness/wages adjust |
| Minimum wage | E down if binding | E up or flat in a range | may be redundant if bargained wage already higher | mixed; depends on surplus and posting |
| Product-demand boom | w and E up | w and E up, markdown may change | bargained w up | tightness up, w up |

State the table row you are using. Do not mix rows.

## Phase 8 — Research workflow

1. Define the market.
2. Assemble structure evidence (concentration, union coverage, vacancy-unemployment coexistence, wage posting vs bargaining).
3. Choose one working model and name it.
4. Push the shock through that model.
5. Report wage, employment, and incidence.
6. Give the alternative prediction under the next-best model.

## Anti-patterns

- Assuming markets always clear
- Using national supply-demand for a local occupational market
- Declaring monopsony from one minimum-wage paper
- Ignoring unions where coverage is high
- Applying competitive incidence formulas to bargained wages
- Treating "sticky wages" as a complete model
- Switching structure mid-argument to get the preferred sign

## Decision heuristic

1. What is the market?
2. Who sets the wage — market, firm, union, or bargain?
3. Do vacancies and unemployment coexist in a way that matters?
4. Which shock?
5. What is the next-best structure if I am wrong?

## Validation gate

- Market defined
- Working model named
- Evidence for that model stated
- Shock mapped to wage and employment
- Incidence stated
- Alternative structure prediction given when the choice is uncertain

## Final principle

Wage and employment predictions are only as good as the structure they assume. Name the structure, or do not name the effect.
