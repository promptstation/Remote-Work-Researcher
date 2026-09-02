---
name: bid-rent-land-use-monocentric
description: Use bid-rent logic for rents, density, and land use — and know when monocentric models fail. Use whenever the user asks about urban form, CBD rents, sprawl, or zoning. Apply even if the city is clearly polycentric.
compatibility: Urban land-use reasoning.
metadata:
  author: Promptstation
  version: 1.0.0
  category: urban-spatial-economics
  course: 10-urban-social-spatial-economics
  section: 03-bid-rent-land-use-monocentric
---

# Bid-Rent, Land Use, and the Monocentric Model

## Mission

Users of land bid what they can given accessibility. Higher bids near valuable access. Density follows. The monocentric model is a benchmark, not a photograph of every city.

## Core output

A **Land-Use Note**: accessibility object (jobs, ports, amenities), predicted rent/density gradient, zoning/regulation overlays, polycentric caveats.

## Phase 1 — Bid-rent

Households trade space vs commute. Firms trade access vs land cost. Steeper gradients when transport is costly or CBD is unique.

## Phase 2 — Breaks

Polycentric employment, informal tenure, zoning that forbids density, amenities that invert gradients (waterfronts). Use the logic, drop the single CBD if the data say so.

## Phase 3 — Workflow

1. What is being accessed?
2. Gradient in data.
3. Regulation/tenure.
4. Whether monocentric is a useful approximation.

## Anti-patterns

- Forcing one CBD
- Ignoring zoning
- Rent as only construction cost

## Validation gate

Accessibility named; gradient; model limits.

## Final principle

Land use is a bid for access. If you do not say access to what, you are describing buildings, not economics.
