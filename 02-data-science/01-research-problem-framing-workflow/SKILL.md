---
name: research-problem-framing-workflow
description: Turn a vague research or business request into a data-science problem with a unit of analysis, target, constraints, and workflow. Use whenever the user asks to "do data science," start a data project, scope an analysis, decide if ML is needed, or has a messy question and a pile of files. Apply even if they only say "what can we do with this dataset" or "build a model for this."
compatibility: Works with briefs, datasets, and stakeholder questions; no specific stack required.
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 01-research-problem-framing-workflow
---

# Research Problem Framing and the Data-Science Workflow

## Mission

Do not start with a model. Start with a question that a dataset could answer, a unit that can be counted, a target that can be defined, and a constraint set (time, access, ethics, decision). Most failed data-science work fails here, not in the algorithm.

## When this skill governs

Use at the start of any data project, when a user asks for "insights," "a model," or "what the data say," or when an existing analysis has drifted from the decision it was meant to support.

## Core output

Deliver a **Problem Frame**:

1. Decision or research question in one sentence
2. Unit of analysis and grain
3. Target (what is predicted, estimated, or described)
4. Success criterion (metric + baseline + decision threshold)
5. Data that exist vs data that would be required
6. Method class (description, prediction, experiment, causal — do not mix)
7. Ethics and leakage risks
8. Workflow and stop conditions

## Phase 1 — Force a question that can fail

Rewrite the request until it has a possible negative answer.

Bad: "Understand our users."  
Good: "Which weekly behaviours among new users predict churn in 90 days well enough to beat a last-week baseline, for targeting a retention email?"

If you cannot state what would make the project a failure, you do not have a problem.

## Phase 2 — Unit, grain, and target

- **Unit:** person, firm, spell, invoice, pixel, country-year
- **Grain:** one row equals one unit at one time
- **Target:** the column you would regret getting wrong

Mismatched grain (user-level model on event-level rows) is a silent error. Duplicate keys and exploded joins belong in the wrangling skill; detecting that the grain is wrong belongs here.

For prediction, define the time of decision and the horizon. Features must be knowable at decision time (leakage skill).

For description, define the population and the period. For causal claims, stop and use Course 6 — do not "control for" your way there in a predictive workflow.

## Phase 3 — Method class

Pick one primary class:

| Class | Question shape | Typical product |
| --- | --- | --- |
| Description | What is the distribution / trend / composition? | Table, chart, dashboard |
| Prediction | What will Y be for a new unit? | Scored list, forecast |
| Experiment | What happens if we change X at random? | A/B result |
| Causal (observational) | What is the effect of X? | Identification strategy |

If the stakeholder wants all four, sequence them. Do not train an XGBoost and then narrate it as a policy effect.

## Phase 4 — Success, baseline, constraints

A metric without a baseline is theatre. Name:

- the dumb baseline (mean, last period, majority class, current rule)
- the decision the number will change
- the cost of false positives vs false negatives
- time, compute, access, legal, and privacy constraints

If no decision changes at any plausible performance, do not build the model. Do the descriptive work.

## Phase 5 — Workflow

Default cycle:

1. Frame (this skill)
2. Acquire
3. Wrangle and QC
4. Explore
5. Prepare (leakage-aware)
6. Model or estimate
7. Evaluate vs baseline
8. Communicate
9. Revisit after contact with reality

Skip steps only on purpose. Write stop conditions: "if missingness on the target exceeds X, we do not model; we diagnose collection."

## Anti-patterns

- Jumping to a model because the user said "machine learning"
- Undefined grain
- Target that is not knowable at decision time
- No baseline
- Causal language on a predictive fit
- "Insights" as a deliverable with no question
- Expanding scope whenever a new column appears

## Decision heuristic

1. What decision or claim?
2. What unit?
3. What target at what time?
4. Description, prediction, experiment, or causal?
5. What baseline must we beat?

## Validation gate

- Question can fail
- Unit and grain named
- Method class named
- Baseline named
- Leakage and ethics flagged
- No algorithm chosen before the target exists

## Final principle

Data science is a question with a grain. Algorithms are optional. If the frame is wrong, every later skill will professionally answer the wrong thing.
