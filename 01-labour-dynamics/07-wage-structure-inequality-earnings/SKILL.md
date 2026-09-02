---
name: wage-structure-inequality-earnings
description: Diagnose wage structure and earnings inequality — composition vs price effects, residual inequality, polarization, inter-industry and occupational differentials, and earnings mobility. Use whenever the user asks why inequality rose, who gained in the wage distribution, about the college premium, job polarization, firm wage effects, or whether a median-wage story hides tails. Apply even if they only ask "are wages stagnating" or want a wage-distribution briefing.
compatibility: Works with earnings microdata descriptions, wage percentiles, and decomposition results.
metadata:
  author: Promptstation
  version: 1.0.0
  category: labour-dynamics
  course: 01-labour-dynamics
  section: 07-wage-structure-inequality-earnings
---

# Wage Structure, Inequality, and Earnings Dynamics

## Mission

Describe the wage distribution as a structure, not a single average. Separate what people bring (composition: education, experience, occupation, hours) from what the market pays for those attributes (prices) from residual inequality. Never let a mean or median wage stand in for the distribution.

## When this skill governs

Use for wage inequality, the college or skill premium, polarization, between- vs within-group inequality, industry and occupation differentials, age-earnings profiles, earnings mobility, and claims that "wages" rose or stagnated.

## Core output

Deliver a **Wage Structure Note**:

1. Population, earnings concept (hourly vs weekly vs annual; real vs nominal), and period
2. Distributional facts (percentiles, Gini or variance of logs, top shares)
3. Composition vs price vs residual decomposition
4. Between-group vs within-group
5. Leading mechanism (SBTC, polarization, institutions, rents, composition)
6. Mobility caveat if the object is lifetime inequality
7. What would overturn the mechanism

## Phase 1 — Define the earnings object

Before any chart:

- hourly wage vs weekly vs annual earnings (hours and weeks will move the latter)
- employees only vs all employed (self-employment)
- real terms, CPI vs PCE vs chain wage deflator — name the deflator
- top-coding and whether top shares are usable
- full-time full-year vs all workers

A "stagnant median wage" with rising annual earnings of prime-age full-time workers is a different story from a stagnant median among all adults. Name the object.

## Phase 2 — Facts before mechanisms

Report, as data allow:

- 10/50 and 90/50 or 90/10 ratios
- variance of log wages
- college/high-school (or other skill) wage gap
- residual inequality after education and experience
- occupation and industry premia
- firm or establishment wage effects if available
- male/female and other group gaps (full treatment in the discrimination skill; here they are part of structure)

Do not open with "skill-biased technical change" before these numbers exist.

## Phase 3 — Composition versus prices

A rising average wage can be:

- more educated or older workers (composition)
- higher returns to education or experience (prices)
- shifts in unobserved residual variance

Use a decomposition (Kitagawa–Oaxaca–Blinder for means; DiNardo–Fortin–Lemieux or related for distributions). State whether you reweight to the base year's composition.

Hours composition: more part-time work can pull weekly earnings down with stable hourly wages.

## Phase 4 — Residual inequality and polarization

Residual (within-cell) inequality rose in many countries after the 1980s. That is not explained by "more college graduates" alone.

Polarization: employment and relative wages growing in high- and low-wage occupations, hollowing the middle (routine-task jobs). Distinct from a simple monotone skill premium.

Do not use polarization and SBTC as synonyms. SBTC predicts a rising skill premium. Polarization is a task-based, U-shaped employment shift. They can coexist.

## Phase 5 — Mechanisms (choose with evidence)

Candidate mechanisms:

- skill-biased or routine-biased technical change
- globalization and offshoring of tasks
- falling union coverage and minimum wages (institutions)
- rising firm wage premia and sorting of high-wage workers into high-wage firms
- superstar rents and winner-take-all markets
- composition (immigration, female participation, education expansion)

Match mechanism to which part of the distribution moved. A falling real minimum wage shows up at the lower tail. A rising 90/50 with stable 50/10 is not a minimum-wage story.

## Phase 6 — Differentials that are not inequality of the same type

Inter-industry and occupational wage differentials can be compensating differentials, unobserved skill, or rents. Firm wage effects (AKM) are rents or amenity/productivity mixes — do not dump them into "skill."

Age-earnings profiles: cross-section profiles mix cohort and age. Do not read a steeper cross-section as faster life-cycle growth without cohort caution.

## Phase 7 — Mobility

Cross-section inequality overstates lifetime inequality if people move in the distribution. If the question is fairness or lifetime resources, bring earnings mobility, not just the annual Gini.

Short panels overstate mobility relative to longer horizons. Transitory shocks ≠ permanent class change.

## Phase 8 — Research workflow

1. Lock the earnings concept and sample.
2. Show the distributional facts.
3. Decompose composition vs prices vs residual.
4. Locate the movement (lower tail, upper tail, middle).
5. Assign a mechanism that fits that location.
6. Add mobility if lifetime inequality is the claim.

## Anti-patterns

- Using the mean wage as the distribution
- Mixing hourly and annual earnings
- Calling every rise in the college gap SBTC
- Ignoring institutions at the lower tail
- Treating cross-section age profiles as life-cycle
- Equating inequality with immobility
- Comparing top shares across datasets with different top-coding
- Deflating with an unnamed price index

## Decision heuristic

1. Which earnings object?
2. Which part of the distribution moved?
3. Composition, price, or residual?
4. Which mechanism hits that part?
5. Stock inequality or lifetime inequality?

## Validation gate

- Earnings concept named
- Real vs nominal and deflator named
- More than one distributional statistic
- Composition vs price attempted
- Mechanism matched to the tail that moved
- Mobility mentioned if lifetime claims are made

## Final principle

Wage structure is a distribution with prices and weights. Averages hide the story; mechanisms that do not match the tail that moved are not explanations.
