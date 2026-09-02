---
name: from-estimate-to-decision
description: Translate a causal estimate into a decision with magnitude, cost, scaling, and external-validity caveats. Use whenever the user has an effect and needs to act — scale a programme, set a policy, or kill a project. Apply even if they only quote a percent effect.
compatibility: Policy and business decisions using estimates.
metadata:
  author: Promptstation
  version: 1.0.0
  category: quantitative-analysis
  course: 06-quantitative-analysis
  section: 15-from-estimate-to-decision
---

# From Estimate to Decision

## Mission

Decisions need magnitudes, costs, and a population, not stars. A 0.03σ effect can be huge at scale or trivial. A LATE for compliers may not be the policy's ITT. Do the arithmetic and the transport.

## Core output

A **Decision Translation**: estimand, magnitude in natural units, cost, implied return, who it applies to, what would reverse the decision.

## Phase 1 — Units

Convert SDs and logs to people, dollars, hours, percentage points. Use the control mean. A 10% effect on a tiny base is a tiny effect.

## Phase 2 — Costs and scale

Effect × population × take-up − cost. Equilibrium: wages, prices, and crowding can eat RCTs when scaled (GE). Say if you are still in partial equilibrium.

## Phase 3 — Decision rule

Pre-state what magnitude would justify action. Then compare the interval, not only the point, to that threshold.

## Phase 4 — Workflow

1. Estimand vs decision population.
2. Natural units + interval.
3. Cost.
4. Scale/GE caveat.
5. Go / no-go / more evidence.

## Anti-patterns

- Stars as decisions
- Percent of a percent without a base
- Scaling LATE as ATE
- Ignoring costs
- Precision theatre (8 decimals)

## Validation gate

Natural units; interval vs decision threshold; population match; costs.

## Final principle

The last step of quantitative analysis is a decision under a magnitude, not a p-value with a press release.
