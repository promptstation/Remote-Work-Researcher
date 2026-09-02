---
name: sample-size-precision-allocation
description: Size samples for stated precision under the actual design — margins of error, design effects, stratum allocation. Use whenever the user asks how many interviews. Apply even if they use an online n=400 calculator.
compatibility: Design-effect adjusted n.
metadata:
  author: Promptstation
  version: 1.0.0
  category: survey-methodology
  course: 07-survey-methodology
  section: 04-sample-size-precision-allocation
---

# Sample Size, Precision, and Allocation

## Mission

n is for a variance under a design. Clustered designs need n_eff = n / deff. Subgroup estimates need n in the subgroup. A national ±3pp does not give you a district estimate.

## Core output

An **n Plan**: estimand, precision or MDE, deff, n and n per stratum/cluster, cost.

## Phase 1 — Target precision

MOE for a proportion at p=0.5 is conservative. For rare traits, p(1-p) is smaller but n_positive is the constraint. For experiments, use power (Course 3/6).

## Phase 2 — Design effect

ICC × cluster size drives deff. If unknown, use a conservative deff from similar surveys — do not use SRS n.

## Phase 3 — Allocation

Neyman if variances differ; proportional if not; oversample small domains you must report.

## Phase 4 — Workflow

1. Which estimate must be precise?
2. deff.
3. n.
4. Domain n.
5. Cost vs drop a domain.

## Anti-patterns

- SRS calculator on a cluster sample
- National n for local claims
- Ignoring item nonresponse on the key variable

## Validation gate

Estimand; deff; domain n if subgroups matter.

## Final principle

Sample size without a design effect and a domain is a shopping number.
