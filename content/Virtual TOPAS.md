---
title: Virtual TOPAS
publish: true
updated: 2026-10-22
tags:
  - topas
---

# Virtual TOPAS

[[index|Research progress]]

**Goal:** Develop a reliable virtual neutron instrument workflow connecting McStas simulations, NICOS control, NeXus data output, and Scipp reduction.

## Research question

Can the existing workflow produce reproducible, internally consistent simulated data that can be reduced and checked against a known reference?

## Approach

Establish a small elastic reference case before adding realistic sample environments or polarization analysis. Use that case to check the complete path from simulation settings to the reduced result.

## Current position

The project review dated 9 October 2026 describes an existing proof of concept covering the instrument, control layer, detector events, data writer, and reduction notebook. It identifies issues involving event weights, metadata, geometry, file structure, and compatibility that need to be resolved for a trustworthy baseline.

That review includes focused code checks and synthetic tests. It does not establish successful operation of the complete workflow: a live NICOS run and McStas compilation were not performed in that review, and production data were not supplied for validation.

## Next proposed milestones

| Milestone | Expected output |
| --- | --- |
| Recover a reproducible setup | Documented source versions, dependencies, and run instructions. |
| Resolve baseline blockers | Consistent detector weights, timing, geometry, metadata, and file finalization. |
| Run a small elastic reference | Saved event data and histogram with the actual simulation history count recorded. |
| Reduce and validate the reference | Agreement between event data and histogram, with an elastic peak near zero energy transfer. |

Sample environments and polarization are subsequent extensions once this baseline is established.

## Decisions needed

- Which source versions and environment should define the reference setup?
- What support is needed to restore the workflow and resolve compatibility issues?
- How much time should this baseline receive alongside HoB₄?

## Progress record

- [[Updates/2026-10-22|22 October 2026 — Starting overview]]
