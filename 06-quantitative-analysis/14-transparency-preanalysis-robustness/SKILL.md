---
name: transparency-preanalysis-robustness
description: Present results as a design plus a robustness set — pre-analysis, specification curves, multiple tests. Use whenever the user has a result they want to "stress test" or a paper with one favourite spec. Apply even if they only report the significant table.
compatibility: Pre-analysis plans, specification curves, disclosure.
metadata:
  author: Promptstation
  version: 1.0.0
  category: quantitative-analysis
  course: 06-quantitative-analysis
  section: 14-transparency-preanalysis-robustness
---

# Transparency, Pre-analysis, and Robustness

## Mission

A finding is a design plus the set of reasonable analyses that still show it. One specification is a choice. Robustness cannot create identification; it can show you did not luck into a column.

## Core output

A **Transparency Pack**: primary spec (pre-specified if possible), robustness set, what would kill the result, disclosure of unplanned paths.

## Phase 1 — Primary

One primary outcome, sample, and estimator, written before seeing Y if you can. If not, say so.

## Phase 2 — Robustness

Vary: sample, controls (pre-treatment only), SEs, bandwidth, donor pool, functional form. Specification curves beat 2 appendix tables of friends of the result.

If the result lives only in one spec, that is the finding.

## Phase 3 — Workflow

1. Primary.
2. Curve of reasonable specs.
3. Multiple-testing if many outcomes.
4. Disclose dead ends that changed the path.

## Anti-patterns

- 12 specs, 11 hidden
- Robustness as adding 40 controls
- Pre-analysis ignored after a null
- p-hacked then "robust"

## Validation gate

Primary named; robustness set not only friends; unplanned analyses labelled.

## Final principle

Transparency is how identification survives contact with the analyst. Hide the path and the coefficient is a private object.
