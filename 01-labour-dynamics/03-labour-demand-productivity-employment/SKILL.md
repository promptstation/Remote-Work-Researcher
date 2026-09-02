---
name: labour-demand-productivity-employment
description: Analyze firms' demand for labour — short-run and long-run hiring, own-wage and cross-wage elasticities, scale and substitution effects, payroll-tax incidence, monopsony, and capital-labour substitution. Use whenever the user asks why firms hire or fire, about labour demand, productivity and employment, minimum wages from the employer side, automation replacing workers, payroll taxes, labour hoarding, or how product-demand shocks pass into jobs. Apply even if they only ask "will this tax kill jobs" or "is AI reducing labour demand."
compatibility: Works with firm, industry, and aggregate employment/wage/productivity data and published demand elasticities.
metadata:
  author: Promptstation
  version: 1.0.0
  category: labour-dynamics
  course: 01-labour-dynamics
  section: 03-labour-demand-productivity-employment
---

# Labour Demand, Productivity, and the Firm's Employment Decision

## Mission

Treat labour demand as a derived demand. Firms do not hire people because wages are low in the abstract; they hire until the extra worker’s contribution to revenue no longer covers the extra cost. Every employment forecast from the firm side must pass through product demand, productivity, factor prices, and market structure.

Do not jump from "wages rose" to "employment must fall" without stating the elasticity, the time horizon, and whether scale or substitution dominates.

## When this skill governs

Use for hiring, layoffs, labour-demand elasticities, payroll taxes and subsidies, minimum wages as a cost shock, automation and capital-labour substitution, monopsony, labour hoarding, and industry employment responses to product-demand shocks.

## Core output

Deliver a **Labour Demand Note**:

1. Shock named (wage, payroll tax, product demand, technology, input prices)
2. Horizon (short run: capital fixed; long run: all factors adjustable)
3. Market structure (competitive labour market vs monopsony)
4. Predicted path of employment, hours, and skill mix
5. Elasticity used and why it fits
6. Incidence (who pays)
7. What would reverse the prediction

## Phase 1 — The hiring rule

In a competitive labour market, a profit-maximizing firm hires until

\[
MRP_L = MC_L
\]

where \(MRP_L\) is the marginal revenue product of labour and \(MC_L\) is the marginal cost of an extra hour or worker (wage plus mandated costs).

- Short run: capital fixed; diminishing returns drive a downward-sloping labour-demand curve
- Long run: firm can substitute capital and other inputs and can change scale

Separate **hours** from **bodies**. Overtime, labour hoarding, and part-time adjustment mean headcount can lag output.

## Phase 2 — Scale and substitution

A wage increase has two long-run channels:

- **Substitution effect:** labour is more expensive relative to capital and other inputs → employment falls for a given output
- **Scale effect:** costs rise, output falls, so all inputs including labour fall

Hicks–Marshall laws: labour demand is more elastic when

- the price elasticity of product demand is high
- labour’s share is high (for scale) or low (for substitution — state which version you are using)
- other factors substitute easily for labour
- the supply of cooperating factors is elastic

Do not quote a generic "labour-demand elasticity of −0.3" without industry, skill, and horizon. Unskilled labour and long-run industry demand are typically more elastic than short-run skilled labour in a specialized firm.

## Phase 3 — Own-wage and cross-wage elasticities

- Own-wage elasticity: % change in labour of type \(i\) for a 1% change in its wage
- Cross-wage elasticity: complements vs substitutes among skill groups

A rise in the wage of type A can raise or cut demand for type B. Automation that substitutes for routine labour can complement non-routine labour. Always specify the labour type.

Conditional (output-constant) vs unconditional (output-adjusting) elasticities are different objects. Policy briefs that ignore this distinction overstate or understate job loss.

## Phase 4 — Payroll taxes, subsidies, and incidence

A payroll tax drives a wedge between what the firm pays and what the worker receives. Incidence depends on elasticities of labour supply and demand, not on who writes the cheque.

- Inelastic supply, elastic demand → workers bear more
- Elastic supply, inelastic demand → firms/consumers bear more
- Sticky wages can put more of a new tax on employment in the short run

Wage subsidies and hiring credits are the mirror image. Deadweight loss and employment effects still run through elasticities, not through statutory language.

## Phase 5 — Product-demand and productivity shocks

Labour is derived:

- Product-demand boom → labour demand shifts out
- Productivity increase: ambiguous. Higher MRP_L raises labour demand at a given wage, but if demand is inelastic or if productivity is labour-saving at the task level, employment can fall while output rises

Never treat labour productivity growth as automatically job-destroying or job-creating. Decompose: output growth vs labour-saving technical change vs hours vs composition.

Labour hoarding: firms keep workers through temporary slumps when hiring/firing and training costs are high. Hours and utilisation move first; headcount later.

## Phase 6 — Market power on the buyer side

Monopsony (or oligopsony) means the firm faces an upward-sloping labour supply curve. Then:

- MRP_L = MC_L > w
- Employment and wages are both below the competitive levels
- A modest wage floor can raise employment (the textbook monopsony result)

Do not assume monopsony just because a minimum wage did not destroy jobs. Concentration, commuting costs, job differentiation, and recruiting frictions are the evidence. Use the equilibrium/market-structure skill when the question is which model to pick; use this skill for the firm’s first-order condition.

## Phase 7 — Technology and task substitution

Capital-labour substitution is not "robots take all jobs." Use a task frame:

- Which tasks in the job are being automated?
- Are remaining tasks complements to the new capital?
- Does product demand expand enough to absorb displaced hours?
- Which skill groups are net substitutes vs complements?

Distinguish labour-saving process innovation from product innovation that creates new tasks.

## Phase 8 — Research workflow

1. Name the firm/industry/skill group and the shock.
2. Fix the horizon (short vs long run).
3. Choose competitive vs monopsony hiring rule.
4. Split scale vs substitution vs product-demand shift.
5. Pick an elasticity with matching horizon and labour type.
6. Translate into employment, hours, and wage-bill implications.
7. State incidence and the main cross-price effects.

## Anti-patterns

- "Higher wages always reduce employment" with no elasticity or horizon
- Treating payroll taxes as paid only by the statutory bearer
- Equating productivity growth with job destruction
- Using a firm-level elasticity for an industry-wide shock (partial vs general equilibrium)
- Ignoring hours and labour hoarding in cyclical analysis
- Declaring monopsony from a single minimum-wage study
- Mixing employees with persons employed (jobs vs people)

## Decision heuristic

1. What cost or revenue object moved?
2. Short run or long run?
3. Scale, substitution, or demand shift?
4. Competitive or monopsonistic buyer?
5. Which labour type?

## Validation gate

- Hiring rule stated
- Horizon stated
- Elasticity, if used, matches type and horizon
- Scale vs substitution separated for long-run wage shocks
- Incidence discussed for taxes/subsidies
- Headcount vs hours distinguished
- No slogan-level automation claims

## Final principle

Firms demand labour as an input into revenue. The professional move is to write down the first-order condition, name the shock that shifted it, and refuse job-count claims that skip productivity, product demand, and the relevant elasticity.
