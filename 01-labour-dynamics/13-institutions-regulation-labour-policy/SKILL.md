---
name: institutions-regulation-labour-policy
description: Predict and evaluate labour-market regulations and programmes — minimum wages, employment protection, active labour-market policies, payroll and income taxes, and social security — with explicit identification. Use whenever the user asks what a minimum wage, EPL, training programme, or tax will do to jobs and wages, or wants a policy evaluation design. Apply even if they only ask "should we raise the minimum wage" or "does firing regulation kill jobs."
compatibility: Works with legal/institutional descriptions, evaluation studies, and labour-market aggregates.
metadata:
  author: Promptstation
  version: 1.0.0
  category: labour-dynamics
  course: 01-labour-dynamics
  section: 13-institutions-regulation-labour-policy
---

# Institutions, Regulation, and Labour-Market Policy

## Mission

A labour-market policy is a change in prices, constraints, or information. Translate the law into those objects, pick the market structure, and only then predict employment, wages, and distribution. Evaluate with a design that could have been wrong.

Do not answer institutional questions with slogans. Do not import a US minimum-wage elasticity into a different bite, coverage, and enforcement setting.

## When this skill governs

Use for minimum wages, employment protection legislation (EPL), active and passive labour-market programmes, hiring subsidies, working-time rules, payroll and labour taxes, and social security design as they affect labour markets.

## Core output

Deliver a **Policy Evaluation Note**:

1. Instrument (what actually changed)
2. Bite, coverage, and enforcement
3. Working market structure (competition, monopsony, bargaining, dualism)
4. Predicted winners and losers
5. Identification strategy for the claim
6. Magnitudes from comparable estimates
7. Implementation risks (informality, non-compliance, substitution)

## Phase 1 — Translate the law into an economic object

- Minimum wage → price floor with a bite (Kaitz, share below the new floor) and enforcement
- EPL → firing cost, hiring option value, dual contracts
- ALMP → training, job search assistance, wage subsidy, public jobs — each a different object
- Payroll tax → wedge
- UI → outside option and liquidity (see unemployment skill)
- Working-time law → hours constraint

If you cannot name the object, you cannot predict.

## Phase 2 — Minimum wages

Predictions depend on structure:

- competitive, binding: employment of affected workers down (or hours down); wages up
- monopsony, modest bite: employment can rise
- high informality: formal wage up, formal jobs down or hours down, informal sector absorbs
- non-compliance: the law is not the wage

Always report bite and coverage. A minimum wage that binds 2% of workers is not the same policy as one that binds 40%.

Look at wage histograms around the floor, not only mean employment. Spillovers above the floor are common.

Hours, non-wage benefits, and prices can absorb a shock that employment levels miss.

## Phase 3 — Employment protection

EPL raises the cost of dismissal. In a simple model it reduces both firing and hiring; the unemployment-rate effect is ambiguous; dualism and temporary contracts often rise.

Evaluate EPL on:

- worker flows (not only stocks)
- dualism (permanent vs temporary vs informal)
- productivity via reallocation
- who is protected (insiders)

"EPL causes unemployment" is not a theorem. "EPL reduces job-to-job and job-to-unemployment flows" is closer to the robust prediction.

## Phase 4 — Active labour-market programmes

Split:

- job-search assistance and monitoring: cheap, often positive, lock-in small
- training: lock-in then possible long-run gain; heterogeneous
- private-sector wage subsidies: can work; deadweight and substitution
- public employment: often poor post-programme outcomes

Use meta-evidence (Card–Kluve–Weber type) as a prior, then match programme type, target group, and cycle. ALMPs work better in tighter markets for some treatments and worse for others. Do not average all ALMPs into one verdict.

## Phase 5 — Taxes and social security

Payroll and income taxes change net wages and labour cost. Incidence is an elasticity question (demand skill). Social security contributions that buy valued benefits are not a pure tax.

Pension and retirement rules are labour-supply institutions for older workers (see labour-supply skill). Disability insurance is a participation institution.

## Phase 6 — Identification

Preferred designs:

- difference-in-differences with a credible control (and pre-trends)
- bunching and histogram evidence for minima
- RDD on age or eligibility thresholds
- randomised ALMP trials
- event studies on law changes

Refuse to treat cross-country regressions of unemployment on EPL indices as causal. Institutions cluster, and indices are coarse.

External validity: bite, enforcement, informality, and bargaining structure must match before you transplant an elasticity.

## Phase 7 — Research workflow

1. Name the legal change as a price, constraint, or information object.
2. Measure bite, coverage, enforcement.
3. Choose structure (including informal dualism).
4. Predict stocks and flows.
5. Cite estimates from similar bite and structure, with identification.
6. List substitution margins (hours, prices, informality, non-compliance).

## Anti-patterns

- Slogan verdicts on minimum wages or EPL
- Transplanting elasticities across unlike institutions
- Evaluating EPL on unemployment rates only
- Averaging all ALMPs
- Ignoring enforcement and informality
- Cross-country index regressions as causal
- Confusing statutory tax with incidence

## Decision heuristic

1. What object did the law change?
2. How many people are actually affected?
3. What is the market structure, including informality?
4. Which margin will adjust (jobs, hours, prices, compliance)?
5. What design identified the estimate you are citing?

## Validation gate

- Legal object translated
- Bite/coverage/enforcement addressed
- Structure named
- Identification named for empirical claims
- Substitution margins listed
- No transplanted elasticity without a similarity sentence

## Final principle

Labour policy changes a price or a constraint in a specific structure. Predict in that structure, evaluate with a design, and do not borrow someone else's elasticity without borrowing their institutions.
