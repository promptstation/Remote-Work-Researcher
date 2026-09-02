---
name: spatial-data-measurement
description: Choose spatial units that match the economic object and flag MAUP — commuting zones, rasters, mobility data, boundaries. Use whenever the user maps or aggregates spatial data. Apply even if they default to admin districts.
compatibility: GIS and spatial data literacy.
metadata:
  author: Promptstation
  version: 1.0.0
  category: urban-spatial-economics
  course: 10-urban-social-spatial-economics
  section: 11-spatial-data-measurement
---

# Spatial Data and Measurement

## Mission

The unit of analysis on a map is a choice that changes the answer (MAUP). Commuting zones ≠ municipalities ≠ grids. Boundaries split markets. Mobility data are samples with bias. Pick the unit for the object.

## Core output

A **Spatial-Unit Spec**: object (market, neighbourhood, exposure), unit, MAUP risk, data source bias.

## Phase 1 — MAUP

Scale and zoning effects. Report sensitivity across units when the claim is fragile.

## Phase 2 — Sources

Census admin units, commuting-defined markets, satellite/raster, mobile traces (selected users), jobs at workplace vs residence.

## Phase 3 — Workflow

1. Economic object.
2. Unit.
3. Edge effects.
4. Sensitivity.

## Anti-patterns

- District because that is the shapefile
- GPS traces as population
- Workplace jobs mapped as residents

## Validation gate

Object-unit match; MAUP flagged if policy-sensitive.

## Final principle

A map is an aggregation. If the aggregation is wrong, the map is a well-coloured error.
