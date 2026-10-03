---
title: Structural analysis of concrete structures — basis and definitions
category: 0-standards
tags: [structural-analysis, overview, design-strips]
standards: [AS 3600:2018 Cl 6.1]
status: draft
reviewed: 2026-09-12
---

# Structural analysis of concrete structures — basis and definitions

> Scope: the general basis for structural analysis in AS 3600 (Cl 6.1), the
> menu of permitted analysis methods, and the design-strip terminology used
> throughout Section 6 and beyond.

## Summary

`[code]` Cl 6.1.1: any method of analysis must account for member material
strength/deformation properties, equilibrium, compatibility of deformation,
and support conditions (including foundation/adjacent-structure interaction
where relevant). Cl 6.1.2: whatever simplifications or idealisations the
chosen method makes must be weighed against the structure's real
three-dimensional behaviour when interpreting results — including a note
that software users should confirm the package suits the analysis being
attempted.

## Detail

### Menu of permitted methods (Cl 6.1.3)

`[code]` For strength, serviceability and robustness per Section 2, any of
the following may be used to get action effects and deformations:

- Static analysis of determinate structures.
- Linear elastic analysis (Cl 6.2) — see [[as3600-elastic-analysis-methods]].
- Linear elastic frame analysis with secondary bending moments from lateral
  joint displacement (Cl 6.3) — same page.
- Linear elastic stress analysis (Cl 6.4) — same page.
- Non-linear frame analysis (Cl 6.5) — see [[as3600-nonlinear-analysis-methods]].
- Non-linear stress analysis (Cl 6.6) — same page.
- Plastic methods for slabs and frames (Cl 6.7) — see
  [[as3600-plastic-and-strut-tie-analysis-methods]].
- Strut-and-tie analysis (Cl 6.8) — same page, full model rules in
  [[as3600-strut-and-tie-modelling]].
- Structural model testing, evaluated per mechanics principles.
- Idealized frame method (Cl 6.9) — see [[as3600-idealized-frame-method]].
- Simplified flexural-analysis methods (Cl 6.10) — see
  [[as3600-simplified-flexural-analysis]].

`[code]` Cl 2.2 (see [[as3600-strength-check-procedures]]) explicitly
permits mixing different strength-check procedures and analysis methods
across different members of the same structure.

### Design-strip terminology (Cl 6.1.4)

`[code]` Used throughout the idealized-frame and simplified two-way-slab
methods:

- **Column strip** — the portion of a design strip extending transversely
  from a support centreline, a quarter of the distance to the next parallel
  row of supports (interior) or to the slab edge plus a quarter-distance
  (edge), capped at total width `L/2`.
- **Design strip** — the portion of a two-way slab system supported, in the
  bending direction considered, by a single row of supports, extending
  halfway to the next parallel support row (interior) or to the slab edge
  plus halfway (edge).
- **Middle strip** — the slab portion between two column strips, or between a
  column strip and a parallel supporting wall.
- **Span support length** `asup` — centreline-to-face distance for beams and
  flat slabs without drop panels/capitals; a 45°-line construction to the
  slab-soffit plane where drop panels/capitals are present (circular/
  polygonal columns may be treated as an equal-area square column for this
  purpose).
- **Transverse width** `Lt` — design-strip width measured perpendicular to the
  bending direction considered.

![[as3600-fig-6.1.4a-design-strip-widths.png]]
*Figure 6.1.4(A) — design strip, column strip and middle strip widths for a
two-way slab system (AS 3600:2018).*

![[as3600-fig-6.1.4b-span-support-length.png]]
*Figure 6.1.4(B) — span support length `asup`, including the drop-panel/
capital construction line (AS 3600:2018).*

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-strength-check-procedures]] — the strength checks each analysis
  method feeds.
- All Section 6 concept pages listed above.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clause 6.1 (Figures 6.1.4(A)/(B)
  reproduced as image assets above).
