---
name: exploratory-data-analysis-visualization
description: Explore datasets and design charts that carry claims — distributions, relationships, missingness, outliers, and small multiples. Use whenever the user asks for EDA, to "see what's in the data," for plots, dashboards of raw structure, or to check whether a modelling idea is even plausible. Apply even if they only want "a quick look" or a pretty chart.
compatibility: Tabular and low-dimensional structured data; any plotting stack.
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 04-exploratory-data-analysis-visualization
---

# Exploratory Data Analysis and Visualization

## Mission

Look at the data until you can name its structure, its failures, and its surprises. Charts are arguments. If a chart does not change what a serious reader believes about a defined question, it is decoration.

## When this skill governs

Use before modelling, when checking data quality visually, when choosing a chart for a claim, or when a stakeholder wants "insights from the data" without a model.

## Core output

Deliver an **EDA Brief**:

1. Question and grain restated
2. Univariate structure of key fields
3. Missingness and outlier patterns
4. Relationships that matter for the question
5. Segment differences
6. Charts that carry each claim
7. Implications for modelling or reporting (including "stop")

## Phase 1 — Sequence

1. Count rows, units, time span.
2. Univariate: histograms, CDFs, tables of top categories — not only means.
3. Missingness: rates, missing-together, missing-by-segment.
4. Bivariate: the target vs each plausible driver; time vs the target.
5. Small multiples by the segments the decision cares about.
6. Write what would surprise a domain expert.

Means without tails lie. Always show a distribution for the target.

## Phase 2 — Chart choice

| Claim | Chart |
| --- | --- |
| Distribution of a quantity | Histogram, CDF, box/violin with points if n is small |
| Composition | Bars (sorted); pie only for 2–3 parts and even then reluctantly |
| Comparison across groups | Aligned bars or dots; same baseline |
| Change over time | Line; mark breaks and missing periods |
| Relationship of two quantities | Scatter; hex/bin if dense; trend only as a helper |
| Many series | Small multiples, not a rainbow spaghetti unless interaction is the point |

Rules:

- zero baseline for counts and bar magnitudes
- encode the claim in position before colour
- one claim per chart
- annotate the actual number the sentence needs
- dual axes only when the reader cannot be misled (almost never)

## Phase 3 — Skepticism while exploring

EDA is a garden of false paths. Protect the confirmatory metric:

- if you will test a hypothesis, pre-specify it or split exploratory vs confirmatory samples
- do not hunt p-values in EDA
- outliers: show them; decide later with a rule
- log scales: say so, and know when they hide zeros

## Phase 4 — Research workflow

1. Restate the question.
2. Distribution of the target.
3. Data-quality plots (missing, duplicates, impossible values).
4. Planned relationships.
5. Segment slices.
6. Three charts maximum in the stakeholder version; the rest stays in the appendix.
7. Write "what I still do not know."

## Anti-patterns

- Chart junk, 3D, rainbow categorical palettes for ordered data
- Means as the only EDA
- Plotting after the model "to illustrate" a result the plot does not support
- Dual-axis tricks
- Exploring the test set
- 20 undifferentiated dashboards
- Treating a correlation blob as a mechanism

## Decision heuristic

1. What claim is this figure making?
2. Is the distribution visible?
3. Would a table be clearer?
4. Am I exploring or confirming?
5. What would falsify the claim on this same chart?

## Validation gate

- Target distribution shown
- Missingness addressed
- Chart type matches the claim
- Axes honest
- Exploratory vs confirmatory split respected if tests will follow
- No model yet unless the frame said description only

## Final principle

EDA is how you earn the right to model. Visualization is how you let someone else check that you looked.
