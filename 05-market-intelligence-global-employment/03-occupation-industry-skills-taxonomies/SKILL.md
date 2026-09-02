---
name: occupation-industry-skills-taxonomies
description: Map roles to ISCO, ISIC, ESCO, O*NET or national classifications and crosswalk without mixing systems. Use whenever the user compares occupations across countries, builds a talent market, or matches job titles to statistics. Apply even if they use informal titles like "growth ninja."
compatibility: ISCO/ISIC/ESCO/O*NET and national crosswalks.
metadata:
  author: Promptstation
  version: 1.0.0
  category: market-intelligence
  course: 05-market-intelligence-global-employment
  section: 03-occupation-industry-skills-taxonomies
---

# Occupation, Industry, and Skills Taxonomies

## Mission

Job titles are marketing. Statistics live in classifications. Map the role to a code, state the scheme and version, and never compare ISCO-08 4-digit to a LinkedIn title cluster as if equal.

## Core output

A **Taxonomy Map**: role, chosen scheme, code(s), inclusions/exclusions, crosswalk uncertainty.

## Phase 1 — Schemes

- **ISCO:** occupation (international)
- **ISIC:** industry
- **ESCO / O*NET / national SOC:** skills and tasks, finer
- Firm job architecture: internal, not comparable

Occupation ≠ industry. A driver in logistics vs a driver in mining.

## Phase 2 — Crosswalks

Crosswalks are many-to-many. Report uncertainty. Do not force a single code when the role spans two; show both and the employment range.

Emerging roles (prompt engineer, growth PM): map to nearest plus a skills overlay; do not pretend a perfect ISCO exists.

## Phase 3 — Workflow

1. Tasks of the role (job analysis if available).
2. Candidate codes.
3. What the statistical series will include extra/missing.
4. Freeze the map for the brief.

## Anti-patterns

- Title string matching as occupation
- Mixing industry and occupation
- Silent crosswalk
- One code for a hybrid role

## Validation gate

Scheme + version; code; mismatch statement.

## Final principle

If you cannot code the occupation, you cannot measure its market. You can only count job titles.
