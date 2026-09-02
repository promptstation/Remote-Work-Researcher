---
name: bootstrap-resampling
description: Use bootstrap and permutation resampling for SEs and intervals when formulas are shaky — and know when resampling does not save you. Use whenever the user wants a bootstrap CI, a jackknife, or uncertainty for a messy statistic. Apply even if they bootstrap dependent data as if iid.
compatibility: Simulation; clustered bootstrap when dependence exists.
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 12-bootstrap-resampling
---

# Bootstrap and Resampling

## Mission

Resampling estimates a sampling distribution from the sample you have. It inherits the sample's dependence, bias, and coverage of the population. It is not a license to ignore design.

## Core output

A **Resampling Note**: statistic, resampling scheme (iid, stratified, clustered), interval type, B, failure risks.

## Phase 1 — What is being resampled

Resample the independent pieces: people, not their monthly rows; clusters, not observations inside clusters; time series with blocks, not iid draws.

If you resample the wrong unit, you get a confident wrong SE.

## Phase 2 — Intervals

- percentile
- BCa / studentized when bias and skew matter
- permutation intervals are not bootstrap intervals (different null)

B too small → jittery endpoints. Thousands, not 50, for published intervals.

## Phase 3 — Failures

Bootstrap can fail for:

- extremes (max, VaR at the tail)
- non-smooth statistics
- n tiny
- parameters on the boundary
- dependence ignored
- biased samples (resampling a biased sample replicates the bias)

Do not bootstrap a convenience sample and call it population inference.

## Phase 4 — Workflow

1. Name the statistic and the independent unit.
2. Choose scheme.
3. B large enough.
4. Compare to a formula SE if one exists (sanity).
5. Report method in the interval footnote.

## Anti-patterns

- iid bootstrap on clustered or time data
- B=100 as a ritual
- Bootstrapping after peeking at many statistics without multiplicity
- Using bootstrap to "fix" bias from confounding

## Validation gate

Unit of resampling named; interval type named; B named; dependence addressed.

## Final principle

The bootstrap copies your sampling process only if you copy the right units. Otherwise it is a random number generator with a footnote.
