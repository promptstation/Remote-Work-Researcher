---
name: unions-collective-bargaining
description: Analyze unions, collective bargaining, and industrial relations — relative wage effects, coverage vs membership, bargaining structure, strikes, and effects on employment, inequality, and productivity. Use whenever the user asks whether unions raise wages, about coordinated vs fragmented bargaining, union wage gaps, strikes, or how bargaining changes employment and inequality. Apply even if they only ask "are unions good for workers" or want a bargaining-structure briefing.
compatibility: Works with union membership/coverage statistics, wage microdata, and institutional descriptions of bargaining levels.
metadata:
  author: Promptstation
  version: 1.0.0
  category: labour-dynamics
  course: 01-labour-dynamics
  section: 10-unions-collective-bargaining
---

# Unions, Collective Bargaining, and Industrial Relations

## Mission

Treat unions as wage-setting institutions with a structure — membership, coverage, bargaining level, and coordination — not as a yes/no ideology. The same "union density" produces different wage, employment, and inequality outcomes under firm-level bargaining than under industry or national coordination.

## When this skill governs

Use for union wage effects, collective agreements, coverage, strikes, works councils, coordinated bargaining, and the institutional channel of wage inequality.

## Core output

Deliver a **Bargaining Structure Note**:

1. Membership vs coverage vs contract content
2. Bargaining level and coordination
3. Relative wage effect and who is in the comparison group
4. Employment, hours, and non-union spillover
5. Inequality and compression
6. Productivity, voice, and strike activity
7. Institutional caveats for this country

## Phase 1 — Membership is not coverage

- **Membership (density):** share of employees who are union members
- **Coverage:** share whose terms are set by a collective agreement (can exceed membership via extension)
- **Contract content:** wage floors, grids, hours, dismissal rules, training

In many European and some developing systems, coverage >> density because of extension. Using density as "union power" in those systems is a measurement error.

## Phase 2 — Bargaining models

- **Monopoly union:** union sets wage on the labour-demand curve; employment falls along that curve
- **Right to manage:** bargain wage; firm sets employment
- **Efficient bargaining:** wage and employment on a contract curve; employment can exceed the demand-curve level
- **Insider-outsider:** insiders bargain; outsiders (unemployed, informal, non-covered) may bear the cost

Do not assume the monopoly-union employment loss. Ask whether employment is on the table and whether outsiders exist.

## Phase 3 — Structure and coordination

Level:

- firm / plant
- industry
- national

Coordination: even firm-level systems can be coordinated (pattern bargaining). Fragmented high-density bargaining tends to raise wages in covered islands and open a union/non-union gap. Coordinated systems tend to compress wages and internalise employment effects.

Calmfors–Driffill-type insight (use as a hypothesis, not a law): very decentralised and highly centralised systems can have different employment outcomes than intermediate, uncoordinated industry bargaining.

Always name level + coordination + extension.

## Phase 4 — Relative wage effects

The union wage gap compares covered (or member) wages to non-covered, controlling for skill. Threat effects and spillovers mean the non-covered wage is not a pure competitive counterfactual.

Standard findings to use as priors:

- positive union wage premium, larger for lower-skill workers (compression)
- smaller residual inequality inside the union sector
- premium estimates are sensitive to selection into union jobs

Do not treat the OLS union dummy as causal. People sort.

## Phase 5 — Employment, informalisation, and dualism

If covered wages rise:

- covered employment may fall or hours may fall
- non-covered or informal employment may rise (dualism)
- capital substitution and product-price pass-through may absorb part of the shock

In developing countries, the relevant margin is often formal covered vs informal, not union vs non-union wage employment. Use the informality skill in tandem.

## Phase 6 — Strikes, voice, and productivity

Strikes are bargaining failure (asymmetric information, commitment). Strike incidence is not a monotonic measure of union strength.

Voice/exit (Freeman–Medoff): unions can raise productivity via voice, training, and lower turnover, or lower it via restrictive practices. Treat productivity as empirical, not as a talking point.

## Phase 7 — Research workflow

1. Report density, coverage, level, coordination, extension.
2. Describe who is outside the system (informal, unemployed, non-covered).
3. Estimate or cite a wage effect with selection caution.
4. Trace employment and inequality (within vs between).
5. Map a reform (decentralisation, extension, right-to-work analogue) through this structure — not through a US firm-level diagram unless that is the structure.

## Anti-patterns

- Using US firm-level monopoly-union diagrams for Ghent or extension systems
- Equating density with coverage
- OLS union dummy as causal premium
- Ignoring outsiders and informal sectors
- Treating strikes as the measure of unionism
- One-word verdicts ("unions raise unemployment") without structure

## Decision heuristic

1. Coverage or membership?
2. Where is the bargain struck, and is it coordinated?
3. Who is the outsider?
4. Wage, employment, or inequality question?
5. Is employment on the contract or only the wage?

## Validation gate

- Density and coverage both stated when they differ
- Bargaining level named
- Comparison group for the wage effect named
- Outsiders/informal mentioned if relevant
- No ideology in the verdict sentence

## Final principle

Unions are a bargaining technology. Name the technology — coverage, level, coordination — before naming the effect.
