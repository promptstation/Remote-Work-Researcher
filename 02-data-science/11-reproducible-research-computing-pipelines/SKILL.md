---
name: reproducible-research-computing-pipelines
description: Produce analyses another researcher can rerun from raw inputs to the reported number — scripts, environments, seeds, data versioning, and workflow order. Use whenever the user needs a reproducible pipeline, to productionise a notebook, to pin dependencies, or when numbers cannot be regenerated. Apply even if they only have a notebook that "worked on my machine."
compatibility: Scripts and notebooks in Python/R; environment files; local or CI runners.
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 11-reproducible-research-computing-pipelines
---

# Reproducible Research Computing and Pipelines

## Mission

A result that cannot be regenerated is not a research result. Package the path from raw extract to reported number so that a stranger with the same inputs gets the same outputs.

## When this skill governs

Use when organising a project, converting notebooks to pipelines, pinning environments, or when two runs disagree.

## Core output

Deliver a **Runnable Project**:

1. Directory layout
2. How to obtain raw data (or a checksummed snapshot)
3. Environment pin
4. Ordered steps (make, targets, snakemake, or a documented script sequence)
5. Seeds
6. One command that rebuilds the reported artefacts
7. What is not deterministic (and why)

## Phase 1 — Layout

```
project/
  data/raw/          # immutable
  data/interim/
  data/processed/
  src/ or R/
  notebooks/         # exploration only
  outputs/           # figures, tables
  environment file
  README with the one command
```

Raw data are never overwritten. Cleaning writes elsewhere.

Notebooks may explore; they must not be the only path to the number in the brief.

## Phase 2 — Environments and seeds

- lock Python/R and package versions
- record OS when binaries matter
- set seeds for sampling, CV, and model inits
- note GPU non-determinism if used

If you cannot pin, say which floating dependency moved a number.

## Phase 3 — Pipelines

Each step: inputs, outputs, and a pure transform. No hidden clicks.

Prefer:

- a Makefile / snakemake / targets pipeline
- or a single `run.sh` that calls numbered scripts in order

Logs: row counts after each step (ties to wrangling quality log).

Config in files, not edited constants buried in cells.

## Phase 4 — Data versioning

- checksum raw files
- if data update, snapshot by date; do not silently replace
- the reported number cites a data vintage

## Phase 5 — Research workflow

1. Separate explore vs confirm.
2. Script the confirm path.
3. Pin env; set seeds.
4. One-command rebuild.
5. Diff outputs against the brief.
6. If numbers move, treat it as a defect.

## Anti-patterns

- Only notebook, no seed, no pin
- Overwriting raw
- Copy-pasted numbers into slides with no artefact
- Hidden manual Excel steps
- Absolute paths to one laptop
- "I'll clean it later" on a result already cited

## Decision heuristic

1. Can a stranger rerun this?
2. Is raw immutable?
3. Is the reported number an output of the pipeline?
4. What vintage of data?
5. What is allowed to be non-deterministic?

## Validation gate

- One command documented
- Raw untouched
- Environment pinned
- Seeds set
- Row-count logs exist
- Brief numbers match pipeline outputs

## Final principle

If you cannot regenerate the number, you do not have the number. You have a memory.
