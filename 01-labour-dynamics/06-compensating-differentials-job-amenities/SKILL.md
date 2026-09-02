---
name: compensating-differentials-job-amenities
description: Analyze wage differences that compensate for job risk, hours, flexibility, location, and benefits using hedonic wage theory. Use whenever the user asks why similar workers earn different wages, about dangerous jobs, night shifts, remote-work pay, health insurance and fringe benefits, job quality beyond the wage, or equalizing differences. Apply even if they only ask "is this job underpaid" or want to compare compensation packages.
compatibility: Works with wage and benefit data, occupational risk statistics, and job-attribute descriptions.
metadata:
  author: Promptstation
  version: 1.0.0
  category: labour-dynamics
  course: 01-labour-dynamics
  section: 06-compensating-differentials-job-amenities
---

# Compensating Differentials, Job Amenities, and Non-Wage Compensation

## Mission

Wages are not the full price of a job. Hedonic theory says workers sell labour and buy job attributes at the same time. A lower wage can be equilibrium compensation for safety, flexibility, prestige, or benefits — or it can be a true penalty. The skill is to tell those apart.

Do not call a wage gap "unfair" or "efficient" until attributes, selection, and constraints are on the table.

## When this skill governs

Use for occupational wage gaps, risk premia, shift pay, remote-work discounts or premia, commuting, employer-provided insurance, leave, job quality indices, and package comparisons across jobs or countries.

## Core output

Deliver a **Compensation Package Note**:

1. Jobs or groups being compared
2. Wage gap (raw and skill-adjusted)
3. Attribute inventory (risk, hours, flexibility, location, benefits, status)
4. Predicted compensating differential
5. Evidence (revealed premia, stated preference, constrained choice)
6. Verdict: amenity, constraint, or residual penalty
7. Full-compensation comparison if benefits matter

## Phase 1 — Hedonic wage idea

In Rosen's hedonic model, the observed wage-attribute locus is the envelope of firm offer curves and worker indifference curves. The slope is the marginal willingness to pay for (or to bear) the attribute among workers who choose that job.

Implications:

- the market premium for risk is not "the" value of a statistical life for every worker; it is the local slope
- workers with weaker aversion to the bad attribute sort into it
- firms that can cheaply provide the amenity do so and pay less

You cannot read a compensating differential off a raw occupational mean. Control for skill, or you will confuse human capital with amenities.

## Phase 2 — Inventory the attributes

Standard attributes that move wages:

- fatality and injury risk
- unemployment / layoff risk
- hours, nights, weekends, on-call
- physical and psychosocial strain
- autonomy and flexibility, including remote work
- location and commute, including urban costs
- employer-provided health insurance, pensions, leave
- legal formality and contract security
- status, meaning, and career option value

List the attributes that differ in this comparison. If you cannot name them, you are not ready to interpret the wage gap.

## Phase 3 — Full compensation, not the wage

Total compensation ≈ wage + mandated benefits + voluntary fringe + expected amenity value − job disamenities.

When comparing public vs private, formal vs informal, US vs other systems, health insurance and pensions can dominate small wage gaps. Never rank jobs on cash wages alone if benefits or hours differ.

For hours: compare hourly wages, then say whether weekly earnings or utility of hours is the object. A high weekly wage on a 70-hour job is not the same object as a high hourly wage.

## Phase 4 — Identification problems

Compensating differentials are hard to see in OLS because:

- ability bias: safer jobs often hire higher-skill workers
- measurement error in risk and amenities
- sorting: the people in dangerous jobs are not a random draw
- constraints: discrimination, monopsony, and imperfect information prevent equalizing differences from appearing
- bundled attributes: risk comes with other bad or good traits

Better designs: occupation-by-industry risk measures, worker fixed effects around job changes, stated-preference experiments, discrete-choice models of job taking.

If the estimated risk premium is zero or wrong-signed, do not conclude theory failed until you have addressed ability, measurement, and constraints.

## Phase 5 — When the differential is not compensating

A wage gap that remains after attributes and skills may be:

- discrimination (use the discrimination skill)
- rents and bargaining (unions, public-sector premia, firm wage effects)
- information frictions
- mobility costs
- non-competitive wage setting

Compensating-differential language should not launder those.

Remote work: a wage discount can be a compensating differential for flexibility, or a productivity/monitoring effect, or a labour-supply shift. Name which.

## Phase 6 — Policy and valuation

Hedonic slopes are used to value statistical life, injury, and environmental disamenities. Use them only when:

- workers knew the risk
- they could choose
- the slope is estimated at the relevant margin

Mandated amenities (safety rules, paid leave) can raise utility and still cut wages or employment depending on whether workers valued the amenity by more than it costs. That is an incidence question, not a reason to ignore the mandate.

## Phase 7 — Research workflow

1. Name the comparison.
2. Adjust for skill/human capital as far as the data allow.
3. Inventory attributes and benefits.
4. Predict the sign of the compensating differential.
5. Inspect whether choice was free enough for hedonic logic.
6. Report wage, full compensation, and residual.

## Anti-patterns

- Ranking jobs on cash wages alone
- Calling every residual gap a compensating differential
- Using raw occupational means as risk premia
- Ignoring hours when comparing earnings
- Treating a zero estimated premium as proof workers do not value safety
- Using a US health-insurance premium in a country with public health care
- Moralising "dirty jobs" without pricing the disamenity

## Decision heuristic

1. What attributes differ?
2. Could workers choose?
3. Is the gap wage or full compensation?
4. After skills, what residual remains?
5. Amenity, rent, or constraint?

## Validation gate

- Comparison named
- Skill adjustment attempted or impossibility stated
- Attribute list explicit
- Benefits included if they differ
- Hedonic vs constraint vs rent distinguished
- No unlabelled "underpaid"

## Final principle

A job is a bundle. The wage is one price in that bundle. Professional comparison prices the whole bundle or admits that it has not.
