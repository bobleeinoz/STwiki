---
title: Plastic and strut-and-tie methods of analysis
category: 0-standards
tags: [structural-analysis, plastic-analysis, yield-line, strut-and-tie]
standards: [AS 3600:2018 Cl 6.7, AS 3600:2018 Cl 6.8]
status: draft
reviewed: 2026-09-12
---

# Plastic and strut-and-tie methods of analysis

> Scope: plastic collapse analysis of frames and slabs (Cl 6.7), and the
> strut-and-tie method of analysis as an analysis-menu item (Cl 6.8) — model
> construction rules themselves live in
> [[as3600-strut-and-tie-modelling]] (Section 7).

## Summary

`[code]` Plastic methods (Cl 6.7.1) apply to frames, one-way/two-way slabs,
and slab-on-ground floors/pavements, provided Ductility Class N reinforcement
is used throughout as flexural reinforcement (steel-fibre slab-on-ground/
pavement is permitted if it meets Cl 16.3.3.8 instead). Reinforcement layout
must still respect serviceability. Strut-and-tie analysis (Cl 6.8.1) is
simply a pointer: when used, the structure/region must satisfy Section 7 in
full — see [[as3600-strut-and-tie-modelling]].

## Detail

### Plastic methods for beams and frames (Cl 6.7.2)

`[code]` Usable for strength design of continuous beams/frames (feeding the
Cl 2.2.2 strength check) provided high-moment regions are shown to have
sufficient moment-rotation capacity to achieve the plastic redistribution
assumed in the analysis — conceptually an extension of the deemed-to-comply
moment redistribution idea in Cl 6.2.7, but without the `ku`-based cap since
full plastic hinging is being assumed.

### Plastic methods for slabs (Cl 6.7.3)

`[code]` Two routes:

- **Lower-bound method** (6.7.3.1): design bending moments derived from any
  moment field satisfying equilibrium and the slab's boundary conditions —
  the classic lower-bound (safe) theorem application.
- **Yield line method** (6.7.3.2): design bending moments derived from the
  mechanism required to form over the whole or part of the slab at collapse;
  where multiple mechanisms are possible, the one giving the most severe
  (highest) design moments governs the design.

### Strut-and-tie method of analysis (Cl 6.8)

`[code]` Cl 6.8.1 is purely a cross-reference to Section 7's requirements.
Cl 6.8.2 requires the same sensitivity check as the other numerical methods
(Cl 6.4.3, 6.5.5, 6.6.5): results must be checked for sensitivity to
variations in geometry and modelling parameters — for a strut-and-tie model
this typically means strut angle, node position and effective-width
assumptions. See [[as3600-strut-and-tie-modelling]] for the actual model
rules (strut types/efficiency, tie anchorage, node classification and
design strengths).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-strut-and-tie-modelling]] — Section 7 detail.
- [[as3600-strength-check-procedures]] — Cl 2.2.2 (plastic methods) and
  Cl 2.2.4 (strut-and-tie) strength checks.
- [[as3600-structural-analysis-overview]] — parent method menu.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clauses 6.7, 6.8.
