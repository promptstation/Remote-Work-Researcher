---
name: linear-regression-statistical-model
description: Fit linear regression as a statistical description — assumptions, residuals, collinearity, prediction vs coefficient interpretation without causal overclaim. Use whenever the user wants OLS, multiple regression, R², or to "control for" variables in a statistical sense. Apply even if they want causal controls — then bound the claim or hand off to Course 6.
compatibility: OLS in R/Python/Stata; residual plots required.
metadata:
  author: Promptstation
  version: 1.0.0
  category: statistics
  course: 03-statistics
  section: 09-linear-regression-statistical-model
---

# Linear Regression as a Statistical Model

## Mission

OLS describes how the conditional mean of Y moves with X in a linear approximation. Coefficients are associations holding included variables fixed in the data. They are not effects of intervening on X unless a causal design says so.

## Core output

A **Regression Report**: estimand (conditional mean), specification, coefficients + SEs, residual diagnostics, collinearity, what may be predicted vs what may not be claimed.

## Phase 1 — Model

\[
Y = \beta_0 + \beta_1 X_1 + \cdots + \varepsilon
\]

β1: difference in mean Y associated with a one-unit difference in X1, linearly, among observations with the same other included X.

Assumptions for the usual SEs: linearity of the conditional mean, independence, homoskedasticity, no perfect collinearity; normality of errors for small-sample t (or rely on large-sample).

## Phase 2 — Diagnostics

- residual vs fitted (linearity, hetero)
- QQ or residual histogram (tails)
- leverage / influence (Cook, hat values)
- VIF / condition number (collinearity)

Heteroskedasticity → robust SEs. Dependence → clustered SEs or hierarchical models. Nonlinearity → transform or splines, not a braver p-value.

R² is variance explained in-sample, not model truth, not causality, not out-of-sample performance.

## Phase 3 — Interpretation

- do not call coefficients "impacts" or "drivers"
- do not drop "insignificant" variables as a ritual
- dummy coefficients are mean differences vs the reference level
- interactions mean the association with X depends on Z; report at meaningful Z values

Prediction: OK within support. Extrapolation: say so.

## Phase 4 — Workflow

1. Estimand: description, prediction, or (if causal) stop and design.
2. Specify; fit.
3. Diagnostics; repair SEs or functional form.
4. Report table + residual plot mention.
5. Verb audit.

## Anti-patterns

- Causal verbs
- Stepwise as science
- Ignoring residual plots
- R² as a quality score for causal work
- Perfect multicollinearity patched by silent software drops

## Validation gate

Estimand named; diagnostics mentioned; SEs appropriate; no causal overclaim.

## Final principle

Regression is a conditional-mean machine. Treat it as that, and it is honest. Treat it as a causality machine, and it is a costume.
