---
name: multiple-testing-integrity
description: Adjust or disclose multiplicity — family-wise error, FDR, p-hacking, optional stopping, pre-registration, exploratory vs confirmatory splits. Use whenever the user ran many tests, peeked, sliced, or asks which findings are "real." Apply even if they only report the significant ones.
compatibility: Bonferroni, Holm, BH/FDR, and honest disclosure.
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 14-multiple-testing-integrity
---

# Multiple Testing, Researcher Degrees of Freedom, and Integrity

## Mission

Every extra look at the data is an extra chance to be wrong in a publishable direction. Control or disclose the family of tests. Silent search is not analysis.

## Core output

An **Integrity Note**: family of tests, primary vs exploratory, adjustment (FWER or FDR), stopping rule, what was unplanned.

## Phase 1 — The family

Count:

- outcomes
- subgroups
- specifications
- looks over time
- transformations

If you would have told a different story had another slice won, that slice was in the family.

## Phase 2 — Adjustments

- **FWER** (Bonferroni, Holm): control P(any false positive). Conservative; good for a small confirmatory family.
- **FDR** (Benjamini–Hochberg): control expected false-discovery proportion. Better for large screens; still not a posterior.

Adjustment does not repair a biased sample or confounding. It only repairs multiplicity.

## Phase 3 — Researcher degrees of freedom

p-hacking, HARKing, optional stopping, outlier rules chosen after seeing p — all inflate Type I error beyond the nominal α.

Repairs:

- pre-specify primary outcome and stopping
- split exploratory / confirmatory samples
- report the full family, not only stars
- sequential designs if peeking is required

## Phase 4 — Workflow

1. List everything that was tested or would have been.
2. Declare primary.
3. Adjust or label exploratory.
4. Show intervals, not only winners.
5. If the user only sent the significant table, ask for the family or treat as exploratory.

## Anti-patterns

- Reporting the winner of 20 tests at α=0.05
- Bonferroni on thousands of tests as the only analysis (just say screen + FDR)
- "We controlled confounders" as a multiplicity fix
- Peeking "just to check"

## Validation gate

Family size stated; primary named; adjustment or exploratory label; unplanned looks disclosed.

## Final principle

A p-value assumes a plan. If the plan was "find something," the p-value is not the one in the textbook.
