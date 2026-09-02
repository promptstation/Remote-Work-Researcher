---
name: data-wrangling-tidy-quality
description: Transform messy extracts into tidy, analysis-ready tables with auditable quality checks. Use whenever the user has messy CSV/Excel/JSON, duplicate keys, mixed types, reshaping needs, or asks to clean data before analysis. Apply even if they say "the numbers look off" or paste a broken table.
compatibility: Tabular data in CSV, Excel, Parquet, SQL extracts; Python/R or equivalent.
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 03-data-wrangling-tidy-quality
---

# Data Wrangling, Tidy Structure, and Quality Control

## Mission

Cleaning is research, not janitorial work. Every recode is a decision that can change the claim. Produce tidy tables, a quality log, and a script — not a mysteriously better spreadsheet.

## When this skill governs

Use when data are messy, wide, duplicated, mistyped, or when QC is needed before EDA or modelling.

## Core output

Deliver **Analysis-Ready Data** plus:

1. Tidy tables at named grains
2. Data dictionary
3. Quality log (row counts, failures, recodes)
4. Reproducible cleaning script
5. Known remaining defects

## Phase 1 — Tidy structure

A table is tidy when:

- each column is a variable
- each row is an observation at the stated grain
- each cell is a value

Reshape long/wide on purpose. Dates are dates, categories are categories, numbers are numbers. Do not leave "n/a", "—", and 0 as a soup of sentinels.

Keys must uniquely identify rows at the grain. If they do not, you are not tidy; you are aggregated or duplicated.

## Phase 2 — Quality checks (run, do not admire)

Minimum battery:

- row count vs extract spec
- uniqueness of keys
- null rates by column
- type and range (ages 0–120, rates 0–100 if percents, no future dates unless expected)
- referential integrity to lookup tables
- duplicate full rows vs duplicate keys with conflicting values
- unit checks (currency, thousands separators, percent-as-1 vs percent-as-100)

Conflicting duplicates are not "take the first row." They are a source defect. Surface them.

## Phase 3 — Recodes that you can defend

- strip/normalise strings; map synonyms with an explicit dictionary
- split overloaded fields (name + id in one cell)
- document every drop rule ("drop if target is null" is a population change)
- do not impute here unless the frame says so; missingness is a fact for EDA
- keep a raw_id to join back

Never drop outliers in cleaning because they look ugly. That is an analysis choice.

## Phase 4 — Research workflow

1. Read the extract spec (grain, keys, population).
2. Profile (counts, types, nulls, key uniqueness).
3. Tidy and type.
4. QC battery; write failures into the log.
5. Recode with a dictionary.
6. Freeze analysis-ready tables and the script.
7. List remaining defects for the next skill.

## Anti-patterns

- Cleaning in an unsaved GUI with no script
- Dropping nulls silently
- Excel serial dates as integers left untreated
- Unique-looking IDs that collide after trim/case
- Imputing in the wrangle step
- "I removed some outliers" with no rule
- One mega-table at mixed grains

## Decision heuristic

1. What is the grain?
2. Do keys uniquely identify it?
3. Is this a type problem, a duplicate problem, or a true missing?
4. Will this recode change the population?
5. Can another person rerun the rule?

## Validation gate

- Keys unique or defect logged
- Types correct
- Row-count trail from extract to analysis-ready
- Drop rules explicit
- Script exists
- Outliers not quietly deleted

## Final principle

Wrangling is where populations are made. If it is not in the quality log, you do not know who you are studying.
