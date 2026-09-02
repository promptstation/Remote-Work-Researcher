---
name: missingness-features-leakage
description: Prepare features without leaking the label or the future; handle missingness (MCAR/MAR/MNAR), encoding, scaling, and valid train/test cuts. Use whenever the user is building a model matrix, imputing, encoding categoricals, creating lags, or splitting data. Apply even if they only ask "how should we impute" or "why is my AUC 0.99."
compatibility: Tabular modelling pipelines in Python/R or equivalent.
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 05-missingness-features-leakage
---

# Missingness, Features, and Leakage-Aware Preparation

## Mission

The model matrix is where honest projects die. Leakage produces celebrity AUC. Imputation without a missingness model produces fiction. Prepare features as if a hostile auditor will ask what was known at decision time.

## When this skill governs

Use when creating features, imputing, encoding, scaling, splitting, or when a model's performance looks too good.

## Core output

Deliver a **Preparation Spec**:

1. Decision time and label horizon
2. Split rule (time, group, random — and why)
3. Missingness diagnosis per key field
4. Imputation/indicator policy fit only on training data
5. Encoding and scaling fit only on training data
6. Leakage audit (fields that must not enter)
7. Feature list with provenance

## Phase 1 — Decision time

Write: "At time t we may use information dated ≤ t to predict outcome in (t, t+h]."

Anything computed with future values, post-outcome updates, or the label itself is leakage. Common killers:

- customer "lifetime value to date" that includes the outcome period
- status fields updated after the event
- target encoding fit on the whole file
- IDs, row numbers, dump timestamps
- aggregates that include the current row's label

If performance is unbelievable, assume leakage until the audit fails to find it.

## Phase 2 — Splits

- **Random split:** only if units are i.i.d. and time does not matter
- **Time split:** default for anything with a clock
- **Group split:** people, firms, households must not appear in both sides
- **Nested CV:** if you will tune

Never fit imputers, encoders, scalers, or PCA on the test fold. Never explore the test fold in EDA if it is the confirmatory set.

## Phase 3 — Missingness

- **MCAR:** missingness independent of data — rare
- **MAR:** missingness depends on observed fields — imputation can help if the model is right
- **MNAR:** missingness depends on the missing value itself — indicators and sensitivity, not a pretty mean fill

Default: add a missing indicator for fields where missingness is informative (refusals, skipped questions, unlogged events). Mean-fill without an indicator is usually wrong.

Do not drop rows with missing target and then claim the same population (that is a selected sample).

## Phase 4 — Encoding and scaling

- unordered categoricals: one-hot or embeddings; watch cardinality
- ordered categoricals: preserve order or use a monotone encoding
- target encoding: only inside CV, never global
- trees do not need scaling; penalised linear models do
- log1p and winsorising are analysis choices; document them

## Phase 5 — Research workflow

1. Write decision time and horizon.
2. List every field; mark known-at-t vs forbidden.
3. Split first.
4. Diagnose missingness on train.
5. Fit preparation on train; transform val/test.
6. Leakage audit: ablate suspicious fields; performance should not collapse from a dump timestamp.
7. Freeze the matrix and the spec.

## Anti-patterns

- Impute-then-split
- Global target encoding
- Random splits on time series
- Filling MNAR with means
- Using the label to build features
- Scaling the whole dataset
- "0.99 AUC" celebrated without a leakage hunt

## Decision heuristic

1. Was this knowable at decision time?
2. Does the split respect time and groups?
3. Is missingness a signal?
4. Was this transformer fit on train only?
5. If I shuffle the label, do features still "work"? (they should not)

## Validation gate

- Decision time written
- Split rule written
- Transformers fit on train only
- Leakage audit done if metrics are strong
- Missingness class considered
- No silent row drops on the target without a population note

## Final principle

If it was not known at decision time, it is not a feature. It is a spoiler.
