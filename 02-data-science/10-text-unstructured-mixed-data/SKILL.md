---
name: text-unstructured-mixed-data
description: Turn text and other unstructured sources into defensible features, labels, or retrieval — tokenisation, document-term methods, embeddings, simple NLP classification, and joins to tabular data. Use whenever the user has documents, comments, tickets, PDFs, or mixed text-plus-table problems. Apply even if they want "sentiment" or "ask the documents."
compatibility: Text files, PDFs, tickets, survey open-ends; classical NLP and embedding APIs.
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 10-text-unstructured-mixed-data
---

# Text, Unstructured, and Mixed Data

## Mission

Unstructured data become research only after a grain, a label or retrieval task, and a validation path exist. Do not run a sentiment model on comments and call it public opinion.

## When this skill governs

Use for text classification, retrieval, coding of open-ends, document search, and joining text to tabular units.

## Core output

Deliver a **Text-to-Table Note**:

1. Document grain (tweet, ticket, page, person-all-tickets)
2. Task (classify, retrieve, extract, embed as features)
3. Corpus construction and filters
4. Method (rules, supervised, embeddings)
5. Validation against human labels or retrieval relevance
6. How text joins to the analysis unit
7. Failure modes (irony, language mix, leakage)

## Phase 1 — Grain and corpus

A "document" is not obvious. Tickets have threads; surveys have items; PDFs have pages. State the unit.

Corpus construction is sampling: date, language, channel, spam filters. Report what was excluded.

PII in free text is still PII. Redact before dumping into third-party APIs unless the basis is clear.

## Phase 2 — Method ladder

1. **Rules and dictionaries** — start here for well-defined concepts (IDs, product names, refusals)
2. **Bag-of-words / TF-IDF + linear model** — strong baseline for classification
3. **Embeddings + simple head or retrieval** — semantic search, clustering of comments
4. **Generative models** — extraction or coding with a rubric and a human audit sample, not as unaudited measurement

If rules get you 90% on a clear task, stop.

Sentiment as a default is usually the wrong task. Prefer a label that matches the decision (complaint vs request vs spam; topic; toxicity).

## Phase 3 — Labels and leakage

Human labels need a codebook, double-coding on a subset, and agreement. Model-generated labels are not ground truth.

Leakage: do not use the agent's closing note that contains the resolution to "predict" the resolution. Decision-time rule still applies.

## Phase 4 — Mixed data

Join text features to the tabular unit without exploding grain. Aggregate (counts, flags, embeddings pooled) with an explicit rule.

Do not concatenate all of a customer's messages including post-outcome messages.

## Phase 5 — Research workflow

1. Task and grain.
2. Tiny labelled set; try rules.
3. Baseline TF-IDF model if classification.
4. Embeddings if retrieval or if linear text models fail.
5. Error examples in the report (false extractions).
6. Freeze codebook and model.

## Anti-patterns

- Sentiment on everything
- Unaudited LLM coding as measurement
- No grain
- Training on text that includes the answer
- Word clouds as analysis
- Language-agnostic models on mixed-language corpora without checks
- Shipping PII to an API by default

## Decision heuristic

1. What unit is a document?
2. Classify, retrieve, extract, or feature-ise?
3. Would a rule work?
4. Who labelled, and how well?
5. What is the join key to the rest of the study?

## Validation gate

- Grain named
- Task not defaulted to sentiment without cause
- Human or gold validation present for measurement claims
- Leakage checked
- PII handling stated
- Errors shown as examples

## Final principle

Text is data only after you say what a document is, what a correct output is, and how you know the machine got it right.
