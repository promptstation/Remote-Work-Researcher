---
name: unemployment-job-search-flows
description: Analyze unemployment as a flow problem — job search, matching, Beveridge curve, job-finding and separation rates, unemployment insurance, and tightness. Use whenever the user asks why unemployment is high, about long-term unemployment, UI effects, vacancies, matching efficiency, or whether joblessness is cyclical or structural. Apply even if they only ask "why can't people find work" or want an unemployment briefing.
compatibility: Works with LFS unemployment series, vacancy data, UI programme rules, and flow statistics.
metadata:
  author: Promptstation
  version: 1.0.0
  category: labour-dynamics
  course: 01-labour-dynamics
  section: 12-unemployment-job-search-flows
---

# Unemployment, Job Search, and Labour-Market Flows

## Mission

Unemployment is a stock produced by flows. Always move from the rate to job-finding, separations, duration, and tightness before naming a cause. A high unemployment rate with high vacancies is not the same object as a high rate with no vacancies.

Do not call unemployment "laziness" or "a lack of jobs" until search, matching, demand, and UI are separated.

## When this skill governs

Use for unemployment rates, duration, long-term unemployment, job search, vacancies, Beveridge curve, matching efficiency, unemployment insurance, and cyclical vs structural joblessness.

## Core output

Deliver an **Unemployment Flow Note**:

1. Stock (LU1 and companions from the measurement skill)
2. Flows (job-finding \(f\), separation \(s\))
3. Duration and long-term share
4. Tightness (\(v/u\)) and Beveridge position
5. Type mix (frictional, cyclical, structural, compositional)
6. UI and search incentives if policy is in play
7. What would move the stock

## Phase 1 — Stocks from flows

In steady state,

\[
u \approx \frac{s}{s+f}
\]

where \(s\) is the separation rate and \(f\) is the job-finding rate (in a simple two-state model).

A rise in \(u\) can be more separations, harder finding, or both. Long-term unemployment is a duration fact, not a different moral category.

Always try to split \(s\) and \(f\). If flow data are missing, duration and the long-term share are the next-best clues.

Three-state models (employment, unemployment, inactivity) matter when participation is moving. Ignore inactivity and you will mis-read \(f\).

## Phase 2 — Types of unemployment (use as labels after flows)

- **Frictional:** search and matching time in a healthy market
- **Cyclical:** deficient aggregate demand; low tightness
- **Structural:** mismatch in skills, location, or industry; Beveridge curve shift
- **Seasonal:** calendar
- **Classical / wage-floor:** wages stuck above clearing (institutions) — a hypothesis, not a default

Do not start with these labels. Start with flows and tightness, then apply a label.

## Phase 3 — Search theory

Workers search until the value of an offer exceeds the value of continued search. Reservation wage rises with UI, nonlabour income, and expected offer quality; it falls with search costs and duration if assets run down.

Implications:

- UI raises reservation wages and can lengthen duration; it also funds better matches and provides insurance
- search intensity responds to tightness and to monitoring
- duration dependence can be true scarring or dynamic selection (the remaining pool is less employable)

Never treat the UI duration effect as the welfare verdict. Insurance value is the point of UI.

## Phase 4 — Matching and the Beveridge curve

Matching function: hires \(h = m(u, v)\). Tightness \(\theta = v/u\).

Job-finding rises with tightness. The Beveridge curve plots \(u\) against \(v\).

- movement along the curve: cyclical tightness
- outward shift: worse matching efficiency (mismatch, composition of \(u\), recruiting intensity)

A simultaneous high \(u\) and high \(v\) is a matching/mismatch problem, not a simple demand shortage. A high \(u\) and low \(v\) is demand (or a wage that will not fall).

Matching efficiency is not "worker quality." It includes recruiting practices, geographic mismatch, and composition of the unemployed.

## Phase 5 — Unemployment insurance design

UI has replacement rate, duration, eligibility, and monitoring.

Trade-off: insurance vs search incentive vs match quality vs automatic stabilisation.

Empirical work often finds positive duration effects; magnitudes vary with tightness (moral hazard is more costly when jobs are plentiful). Do not import a boom-era UI elasticity into a slump.

Liquidity vs moral hazard: some extra duration is people who can afford to search, not people who do not want work.

## Phase 6 — Phillips and wage pressure (limited use)

A tighter labour market (low \(u\), high \(\theta\)) tends to raise wage growth. The Phillips curve is not a substitute for flow analysis. Use it only when the question is inflation or wage pressure, and pair it with tightness, not only LU1.

## Phase 7 — Research workflow

1. Report LU1, EPR, LFPR, duration (measurement skill).
2. Split \(s\) and \(f\) if possible.
3. Place the market on the Beveridge diagram.
4. Label cyclical vs mismatch vs compositional.
5. If UI is the question, map replacement, duration, and tightness.
6. Say what would cut \(u\): higher \(f\), lower \(s\), or both — and how.

## Anti-patterns

- Interpreting LU1 without duration or vacancies
- Calling all unemployment structural
- Calling all unemployment cyclical
- Treating UI as pure moral hazard
- Ignoring inactivity flows
- Equating long-term unemployment with unemployability
- Using a wage-floor story without evidence of a binding floor
- Mixing claimant counts with ILO unemployment

## Decision heuristic

1. Did \(s\) rise or \(f\) fall?
2. Are vacancies high or low?
3. Is the Beveridge curve shifting?
4. Is this insurance, demand, or mismatch?
5. What flow do you want to change?

## Validation gate

- Stock paired with at least one flow or duration fact
- Tightness or vacancies addressed if the data exist
- Type label comes after flows, not before
- UI discussion includes insurance, not only incentives
- Companions (EPR, LFPR) not omitted

## Final principle

Unemployment is produced by separations and job-finding. Name the flow you intend to change, or you have not analysed unemployment.
