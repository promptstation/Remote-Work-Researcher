---
name: prediction-explanation-causal-claims
description: Keep predictive performance, statistical association, and causal claims in separate sentences. Use whenever the user wants "drivers," "what causes churn," feature importance as explanation, or to use a predictive model for policy. Apply even if they ask "why did the model predict this" or "which features matter most."
compatibility: Works alongside supervised models and causal designs (Course 6).
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 09-prediction-explanation-causal-claims
---

# Prediction versus Explanation versus Causal Claims

## Mission

These three sentences are not interchangeable:

1. This model predicts Y well.
2. Y moves with X in these data.
3. If we change X, Y will change.

Most stakeholder harm from data science is (1) or (2) sold as (3). This skill is the refusal protocol.

## When this skill governs

Use when interpreting models, feature importance, SHAP, coefficients, "drivers of," or when a predictive project is asked to recommend an intervention.

## Core output

Deliver a **Claim Sort**:

1. The user's question recoded as prediction, association, or causal
2. What the current artefact can support
3. What it must not say
4. If causal is required: the handoff to an identification strategy (Course 6)
5. If explanation of a prediction is required: local vs global, with limits

## Phase 1 — Sort the question

| User language | Usually they need |
| --- | --- |
| Who should we target? | Prediction |
| What is associated with Y? | Description / association |
| What should we change to move Y? | Causal |
| Why did this person get this score? | Local explanation of a prediction |
| Why is Y happening in the world? | Causal or domain theory |

Ask once: "If we could randomly change X, is that the action you want to take?" If yes, you are in causal land.

## Phase 2 — What importance is

Permutation importance, SHAP, Gini, and standardised coefficients answer: how the model uses features, or how prediction error moves when a feature is broken.

They do not answer: the effect of intervening on that feature.

Correlated features split or steal importance. A leaky feature looks "important." A cause with little residual variation looks unimportant.

You may use SHAP to debug a model or to explain a score to a user under a prediction product. You may not write "SHAP shows that reducing X will cut churn."

## Phase 3 — Coefficients

In a predictive linear model, a coefficient is how the fitted surface changes with X holding other included features fixed in the data — not holding the world fixed.

Do not say "controlling for" as if you had a causal model unless you actually specified one (back-door, instrument, design). That is Course 6.

## Phase 4 — When prediction is enough

Targeting, ranking, forecasting, detection: prediction is the product. Then explanations are optional diagnostics. Keep verbs: predict, rank, flag — not cause, drive, impact.

## Phase 5 — Research workflow

1. Recode the question.
2. If prediction: interpret only as model behaviour.
3. If association: use tables, not SHAP theatre.
4. If causal: stop modelling for importance; write the intervention and the identification problem; switch skills.
5. Edit the stakeholder language before delivery.

## Anti-patterns

- "Top drivers" from a random forest
- Policy recommendations from SHAP
- "X causes Y because it is significant in the predictive model"
- Explaining a leaky feature as a business insight
- Using the same model for targeting and for estimating treatment effects without a design

## Decision heuristic

1. Are we changing X in the world?
2. If no, is this prediction or description?
3. If yes, what is the identification strategy?
4. Does this verb survive that answer?

## Validation gate

- Claim class labelled
- Importance not sold as effects
- Causal requests handed off or designed
- Verbs audited
- Leaky "important" features not narrated as mechanisms

## Final principle

Predictive models answer "what will happen if the world looks like this." Causal claims answer "what will happen if we change it." Importance plots answer neither of those unless you already know which question you are in.
