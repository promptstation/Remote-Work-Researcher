---
name: discrimination-segmentation-unequal-outcomes
description: Measure and interpret group gaps in wages and employment — taste-based and statistical discrimination, Oaxaca-Blinder decompositions, occupational segregation, and labour-market segmentation. Use whenever the user asks about gender, race, caste, migrant, or disability pay gaps, hiring discrimination, glass ceilings, or whether a residual gap is discrimination. Apply even if they only ask "why do women earn less" or want an equal-pay briefing.
compatibility: Works with earnings and employment microdata descriptions, audit-study results, and decomposition outputs.
metadata:
  author: Promptstation
  version: 1.0.0
  category: labour-dynamics
  course: 01-labour-dynamics
  section: 08-discrimination-segmentation-unequal-outcomes
---

# Discrimination, Segmentation, and Unequal Labour-Market Outcomes

## Mission

Measure group gaps carefully, decompose them honestly, and keep "discrimination" as a claim that needs a mechanism — not as the name of every residual. Separate pre-market inequality, hours and occupation sorting, compensating differentials, and unequal treatment in hiring, pay, and promotion.

Do not treat an unadjusted gap as discrimination. Do not treat a zero residual as proof of fairness.

## When this skill governs

Use for gender, race, ethnicity, caste, religion, migrant, disability, or other ascriptive gaps in wages, employment, hours, occupation, and promotion; for audit and correspondence studies; for equal-pay and anti-discrimination policy.

## Core output

Deliver a **Gap Diagnostic Note**:

1. Groups and outcome (hourly wage, annual earnings, employment, occupation)
2. Raw gap
3. Adjusted gap and decomposition
4. Sorting (hours, occupation, firm)
5. Candidate mechanisms
6. Evidence that can distinguish them
7. Policy mapping that matches the mechanism

## Phase 1 — Choose the outcome

Different outcomes answer different questions:

- hourly wage: price of an hour, still mixes occupation and firm
- weekly/annual earnings: mix hours, weeks, and wages — often the policy-relevant household object, but not "unequal pay for equal hours"
- employment / EPR: access to work
- occupation and firm: allocation
- promotion and residual within job: glass ceiling vs pay-within-job

Never answer "the gender pay gap" without saying which of these.

## Phase 2 — Raw then adjusted

Always show the raw gap first. Then adjust.

Oaxaca–Blinder (and Kitagawa) splits the mean gap into:

- **explained:** differences in observables (education, experience, hours, occupation — each of these may themselves be contaminated by discrimination)
- **unexplained:** different prices for the same observables, plus omitted variables

The unexplained part is **not** automatically discrimination. It is a residual. Ability, preferences, unmeasured hours intensity, and discrimination all live there.

If you include occupation and firm, you assign segregation to the "explained" part. That can hide discrimination in assignment. Report decompositions with and without occupation/firm.

## Phase 3 — Mechanisms

**Taste-based discrimination (Becker):** prejudice by employers, employees, or customers. Predicts that discriminating employers sacrifice profit; competition and market expansion can erode it. Customer discrimination can persist.

**Statistical discrimination:** groups differ in average productivity or in the precision of productivity signals; employers use group as a proxy. Can be self-reinforcing if it reduces investment in the discriminated group.

**Human-capital and pre-market:** schooling quality, health, networks — real productivity differences that are not current labour-market discrimination but may be prior injustice.

**Household and hours:** care burdens change hours, experience accumulation, and job choice. This is not "choice" in a vacuum; it is constrained.

**Segmentation:** primary/secondary jobs, formal/informal, internal labour markets that ration access.

Name the mechanism you are using. Do not stack them as if they were one.

## Phase 4 — Evidence that actually identifies unequal treatment

Stronger:

- correspondence/audit studies in hiring (callback gaps)
- tester studies
- within-job pay gaps after precise job controls (still not perfect)
- natural experiments in anonymised hiring or anti-discrimination law
- promotion gaps conditional on performance measures

Weaker:

- residual from a coarse Mincer equation
- "women choose different majors" as a full explanation of lifetime earnings
- international raw-gap league tables with no hours or selection adjustment

Selection into work: if only some women or some minority workers are employed, the observed wage gap is selected. Heckman-style or bounding approaches belong here when employment gaps are large.

## Phase 5 — Segregation and glass ceilings

Occupational and firm segregation can be preferences, networks, hours constraints, or exclusion. Index of dissimilarity and percentile-rank methods describe; they do not explain.

Glass ceiling: gaps that widen at the top of the distribution (quantile decompositions). Sticky floor: gaps at the bottom. These point to different policies.

## Phase 6 — Policy mapping

Match instrument to mechanism:

- unequal pay in the same job → pay transparency, enforcement, comparable-worth (with the usual efficiency caveats)
- hiring callbacks → anonymised screening, targeted outreach, enforcement
- statistical discrimination from noisy signals → better individual assessment, probation, credentials
- hours/care → childcare, leave, tax treatment of second earners
- segmentation → formalisation, mobility, internal-market access
- pre-market → education quality, not only labour-market law

A law that assumes taste-based employer discrimination will disappoint if the gap is hours and occupation.

## Phase 7 — Research workflow

1. Lock groups and outcome.
2. Raw gap, then decomposition with and without occupation/firm.
3. Inspect hours, selection into work, and segregation.
4. Bring the best available causal evidence (audit, law change).
5. Assign a leading mechanism and a runner-up.
6. Recommend policy that hits that mechanism.

## Anti-patterns

- Equating the raw gap with discrimination
- Equating the residual with discrimination
- Controlling for occupation and then declaring no discrimination
- Ignoring selection into employment
- Using annual earnings to talk about equal pay for equal work
- Treating household hours as pure preference
- One-country residual compared naively to another
- Policy slogans unmatched to mechanism

## Decision heuristic

1. Which outcome?
2. Raw or adjusted, and adjusted for what?
3. Is assignment to jobs part of the problem?
4. Taste, statistical, pre-market, hours, or segmentation?
5. What evidence could distinguish those?

## Validation gate

- Outcome named (hourly vs earnings vs employment)
- Raw and adjusted both shown
- Occupation/firm treatment explicit
- Residual not relabelled as proof
- Mechanism named
- Policy matched to mechanism

## Final principle

Unequal outcomes are measured objects. Discrimination is a mechanism. The professional standard is to keep the measurement, the residual, and the mechanism on three different lines.
