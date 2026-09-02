---
name: ethics-privacy-fairness-documentation
description: Spot privacy and fairness failures in data pipelines and document datasets and models so others can audit them. Use whenever the user handles personal data, builds scoring models that affect people, needs a model card or datasheet, or asks about bias. Apply even if they only want to "ship the model" or dump PII into a notebook.
compatibility: Research and product data work; legal advice is not provided — flag when counsel is required.
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 14-ethics-privacy-fairness-documentation
---

# Ethics, Privacy, Fairness, and Documentation

## Mission

Data science that affects people needs a legitimate purpose, minimised data, documented limits, and a fairness check that is more than a slogan. Documentation is part of the work product, not an appendix if time remains.

This skill does not replace legal counsel. It prevents casual harm and forces the questions counsel will ask.

## When this skill governs

Use when personal data, scoring, targeting, monitoring, or public communication of models is in play.

## Core output

Deliver an **Ethics and Documentation Pack**:

1. Purpose and lawful/ethical basis (as stated by the user / organisation)
2. Data minimisation list (fields kept vs dropped)
3. Privacy risks (re-identification, downstream APIs)
4. Fairness slices and error gaps
5. Dataset documentation (datasheet-style)
6. Model card (intended use, out-of-scope, metrics by group)
7. Red lines (what this model must not be used for)

## Phase 1 — Purpose and minimisation

Collect and retain only what the frame needs. "Might be useful" is not a purpose.

Special-category and children's data: stop and require an explicit basis.

Sharing with third-party model APIs is a disclosure. Say so.

## Phase 2 — Privacy

- PII in logs, notebooks, and screenshots is still PII
- aggregations can still re-identify (small cells)
- "anonymous" IDs that join back to people are not anonymous
- suppress or coarsen small cells in published tables

If the user asks to deanonymise, scrape private profiles, or bypass access control, refuse.

## Phase 3 — Fairness

Fairness is not one number.

- define groups only with a legitimate reason to check them
- report outcome rates and error rates (FPR/FNR) by group, not only overall AUC
- equalised odds, calibration by group, and demographic parity answer different moral questions — name which is relevant to this decision
- gaps can come from labels, sampling, or the world; do not "de-bias" by hiding the gap without a decision rule

A fairness fix that destroys the legitimate signal may still be required if the use is high-stakes. That is a governance choice; surface it.

## Phase 4 — Documentation

Datasheet: origin, collection, preprocessing, known gaps, recommended uses.  
Model card: intended use, out-of-scope uses, metrics, slices, caveats, maintenance owner.

If it is not written, the next person will misuse it.

## Phase 5 — Research workflow

1. Purpose and data list.
2. Privacy screen (cells, APIs, logs).
3. Slice performance for affected groups.
4. Write datasheet + model card.
5. State red lines in the decision product.

## Anti-patterns

- Shipping without group error tables on a people-scoring model
- Calling a dataset anonymous because names were removed
- Fairness as a marketing paragraph
- Dumping PII into prompts or tickets
- Dual-use silence (a model that can be used to exclude)
- Documenting only after an incident

## Decision heuristic

1. Who can be harmed if we are wrong?
2. Do we need this field?
3. Which fairness criterion matches this decision?
4. What is out of scope?
5. Would we publish the datasheet?

## Validation gate

- Purpose stated
- Minimisation done
- Small-cell / PII handling stated
- Slice metrics if people are scored
- Model card / datasheet produced for anything that will be reused
- Red lines explicit

## Final principle

If a person can be hurt by a wrong score or a leak, privacy, fairness, and documentation are not extras. They are the work.
