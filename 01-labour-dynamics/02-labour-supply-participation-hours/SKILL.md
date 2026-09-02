---
name: labour-supply-participation-hours
description: Analyze labour supply at the participation (extensive) and hours (intensive) margins using reservation-wage theory, income and substitution effects, household production, and tax-transfer incentives. Use whenever the user asks why people work, leave work, or change hours; about labour force participation, reservation wages, EITC/welfare work incentives, female or youth participation, retirement, intertemporal labour supply, or how taxes and benefits change labour supply. Apply even if the user only asks "why did participation fall" or wants a participation briefing.
compatibility: Works with labour-force microdata descriptions, tax-benefit parameters, and published elasticities; no proprietary software required.
metadata:
  author: Promptstation
  version: 1.0.0
  category: labour-dynamics
  course: 01-labour-dynamics
  section: 02-labour-supply-participation-hours
---

# Labour Supply, Participation, and Hours

## Mission

Explain labour supply as a choice under constraints, not as a moral fact about work ethic. Separate the decision to work at all from the decision of how many hours to work. Recover the wage, nonlabour income, household structure, and tax-transfer rules that shift those decisions.

A professional analysis never treats a participation-rate change as proof that "people do not want to work." It identifies which margin moved, which relative prices changed, and which groups drove the aggregate.

## When this skill governs

Use when the task involves participation, hours, reservation wages, work incentives, welfare or earned-income credits, second-earner labour supply, retirement, or intertemporal substitution of hours. If the user only has a participation headline, start by reconstructing the population and then apply this skill.

## Core output

Deliver a **Labour Supply Note**:

1. Question restated as extensive margin, intensive margin, or both
2. Population (sex, age, household type, country, period)
3. Theoretical mechanism (reservation wage, income/substitution, household production, tax kink)
4. Predicted direction of hours and participation
5. Evidence (elasticities, event studies, descriptive splits)
6. Policy or shock mapping
7. What would falsify the interpretation

## Phase 1 — Name the margin

**Extensive margin:** work or not. Driven by whether the offered wage exceeds the reservation wage.

**Intensive margin:** hours conditional on working. Driven by the slope of the budget constraint and the income/substitution split.

Aggregates mix both. A falling LFPR is extensive. Falling mean hours among the employed is intensive. Falling total hours can be either. Always split.

Prime-age (25–54) participation is the cleanest behavioural series. Youth mixes schooling. Older ages mix retirement and health. Women’s series often mix care, measurement of unpaid work, and tax treatment of second earners.

## Phase 2 — Reservation wage and the static model

The person compares market wage \(w\) to reservation wage \(w^*\).

- Participate if \(w > w^*\)
- \(w^*\) rises with nonlabour income, the value of non-market time (care, home production, schooling, leisure), stigma or search costs, and benefit rules that pay for not working
- \(w^*\) falls when work also yields benefits that require employment (health insurance, EITC, work-conditioned transfers)

An increase in nonlabour income raises \(w^*\) and reduces participation. An increase in \(w\) raises participation (pure substitution at the extensive margin: there is no income effect on participation for people who were not working).

Do not apply an income effect to people who were out of the labour force. They had no labour income to begin with.

## Phase 3 — Income and substitution effects on hours

For people already working, a wage change does two things:

- **Substitution effect:** leisure is more expensive → hours rise
- **Income effect:** the person is richer → hours fall if leisure is normal

Net labour-supply elasticity is positive if substitution dominates, negative if income dominates (backward-bending segment).

Standard empirical orders of magnitude (use as priors, not laws):

- Male intensive-margin elasticity: near 0 to slightly negative
- Female extensive-margin elasticity: larger, often 0.2–0.8 depending on group and country
- Macro/Frisch elasticities used in macro models are larger than micro intensive elasticities; do not mix them

When reporting an elasticity, state: margin, group, time horizon (Marshallian vs Hicksian vs Frisch), and whether it is a micro or macro estimate.

## Phase 4 — Household production and family labour supply

Individuals do not supply labour in isolation. Time is split among market work, home production, care, and leisure. A partner’s wage, children, and public childcare change \(w^*\).

- Children typically reduce maternal hours and participation more than paternal, but this is an empirical regularity, not a modelling assumption you should hard-code as destiny
- Second-earner supply is especially sensitive to joint taxation, childcare prices, and school hours
- Intra-household models (unitary vs collective) matter when you interpret how a transfer to one spouse changes the other spouse’s hours

If the question is about female LFPR, always inspect childcare costs, leave policy, tax treatment of second earners, and measurement of unpaid family work before invoking preferences.

## Phase 5 — Taxes, transfers, and kinks

Draw the budget constraint in hours–consumption space. Most work-incentive mistakes come from ignoring kinks and notches.

- Lump-sum benefits with 100% benefit reduction → high \(w^*\), participation trap
- Gradual taper → high effective marginal tax rates (EMTR) on the intensive margin
- EITC-type in-work credits → raise participation; hours effects differ in phase-in, plateau, and phase-out
- Income taxes vs payroll taxes: both change net wage; incidence is a demand-side question (use the labour-demand skill for that)

Compute or cite EMTRs rather than statutory rates. A 20% income tax plus a 40% benefit taper is not a 20% problem.

## Phase 6 — Dynamics

Static models miss:

- **Intertemporal substitution:** high wages today pull hours from other periods (Frisch elasticity)
- **Human capital:** work today raises future wages, so current participation has an investment return
- **Retirement:** Social security, pensions, and health insurance eligibility create spikes in exit
- **Added-worker and discouraged-worker effects:** a partner’s job loss can raise or lower the other partner’s participation

For cyclical questions, pair participation with unemployment and the potential labour force. Discouragement is not a preference shift.

## Phase 7 — Research workflow

1. Define the group and margin.
2. Identify the relative-price shock (wage, tax, benefit, childcare, nonlabour income).
3. Predict participation and hours with income/substitution and \(w^*\).
4. Inspect composition: age structure can move LFPR with no behavioural change.
5. Bring elasticities from comparable settings; do not invent them.
6. Separate measurement (ICLS, unpaid work) from behaviour.
7. State what the data cannot separate (preferences vs constraints vs measurement).

## Anti-patterns

- Treating LFPR changes as work-ethic changes
- Applying income effects to non-participants
- Using a single "labour supply elasticity" without margin or group
- Ignoring EMTRs and benefit tapers
- Explaining female participation without care, tax, or measurement
- Confusing hours among workers with labour input of the population
- Mixing micro Marshallian elasticities with macro Frisch elasticities
- Assuming backward-bending supply as the default

## Decision heuristic

1. Extensive, intensive, or both?
2. Who is the decision-maker (person or household)?
3. What relative price moved?
4. Did \(w^*\) move, \(w\) move, or both?
5. What companion series (EPR, hours, LU4, age structure) would falsify the story?

## Validation gate

- Margin named
- Population named
- Mechanism named (reservation wage and/or income-substitution)
- Tax-transfer map present if policy is in play
- Elasticity, if used, has margin/group/horizon
- Measurement caveats stated for female, informal, or rural series
- No moral language about work effort

## Final principle

Labour supply is the mapping from wages, nonlabour income, household time, and fiscal rules into participation and hours. The researcher’s job is to keep those objects distinct and to refuse explanations that skip the budget constraint.
