---
title: Idealized frame method of analysis
category: 2-concrete
tags: [structural-analysis, idealized-frame, two-way-slabs]
standards: [AS 3600:2018 Cl 6.9]
status: draft
reviewed: 2026-09-12
---

# Idealized frame method of analysis

> Scope: AS 3600's idealized-frame simplification for multistorey buildings
> with a regular layout (Cl 6.9), including its extension to two-way slab
> systems.

## Summary

`[code]` Applies to reinforced/prestressed multistorey buildings representable
as a regular line-member framework (Cl 6.9.1), and — via Cl 6.9.5 — to framed
structures incorporating two-way slab systems with a regular layout. The
building is analysed either rigorously, or as two series of approximately
parallel 2D idealized frames (one per principal direction), each frame
comprising the footings, a row of vertical members, and the horizontal
members they support at each floor (Cl 6.9.2).

## Detail

### Vertical load analysis (Cl 6.9.3)

`[code]` Load arrangement follows the Cl 2.5.4 pattern-loading rules (see
[[concrete-limit-state-design-basis]]). The frame may be analysed in its
entirety, or one storey at a time: for floor moments/shears, isolate the
floor with columns above/below fixed at their remote ends; for column
forces/moments, isolate each column level with adjoining floors fixed at
adjacent supports and columns fixed against rotation/translation at remote
ends. Axial-deformation-driven length change in beams/slabs and shear
deflection may be neglected; axial shortening of columns must be considered
where it affects floor-system actions. A minimum-shear-force floor is set for
live-load reduction cases (own-words: where the live-load reduction factor
is taken as 1, minimum imposed-action shear anywhere in a member must be at
least a quarter of the maximum imposed-action shear from full uniform
loading; where reduction is used, both max and min must be separately
assessed for partial loading).

### Horizontal load analysis (Cl 6.9.4)

`[code]` In lieu of rigorous analysis, in-situ floor slabs may be assumed to
act as horizontal diaphragms distributing lateral force among frames/walls
(design per Section 15, not yet ingested). The full idealized frame is
considered for horizontal loads unless restrained by bracing/shear walls.

### Extension to two-way slab systems (Cl 6.9.5)

`[code]` Applies where Ductility Class L is not the main flexural
reinforcement, to solid slabs (with/without drop panels), two-way ribbed
(waffle) slabs, slabs with recessed soffits confined within both middle
strips, slabs with openings conforming to Cl 6.9.5.5, and beam-and-slab
systems including thickened slab bands (6.9.5.1). The idealized frame treats
slab floors as wide beams (6.9.5.2); their effective width for vertical-load
stiffness is the full design-strip width `Lt` for flat slabs, or per Cl 8.8.2
for T-/L-beams.

`[code]` **Column strip / middle strip moment distribution** (6.9.5.3): each
design strip splits into column strip + two half-middle-strips. The column
strip takes a proportion of the total negative/positive moment at each
critical section, per Table 6.9.5.3 — own-words: the
column-strip share is highest for negative moment at an interior support and
lowest for positive span moment, with the exact split also depending on
whether an exterior support has a spandrel beam.

![[as3600-table-6.9.5.3-column-strip-moment-distribution.png]]
*Table 6.9.5.3 — distribution of bending moments to the column strip, by
location and limit state (AS 3600:2018).*

Whatever the column strip
doesn't take goes to the adjoining half-middle-strips; a middle strip next to
a wall-supported edge takes double the share of its single adjoining
half-middle-strip.

`[code]` **Torsional moments** (6.9.5.4): moment transferred to a column by
torsion in the slab/spandrel beam is designed per Cl 9.2 (slab) or Cl 8.3
(beam); spandrel beams in beam-and-slab construction need at least the
Cl 8.3.3 minimum torsional reinforcement.

`[code]` **Openings** (6.9.5.5): permitted without further calculation
provided interrupted reinforcement is redistributed to each side of the
opening and the opening's plan size stays within stated fractions of strip
width — a full middle-strip width where it sits entirely within two middle
strips, a quarter of strip width at a middle/column-strip boundary, and an
eighth of column-strip width where it sits within two column strips
(subject to the reduced section still being able to transfer moment/shear to
the support, and to the Cl 9.2 shear requirements).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-structural-analysis-overview]] — parent method menu and
  design-strip/column-strip definitions (Cl 6.1.4).
- [[concrete-limit-state-design-basis]] — Cl 2.5.4 pattern-loading rules
  reused here.
- [[concrete-simplified-flexural-analysis]] — the further-simplified
  coefficient-based alternative to this method.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 6.9 (Table 6.9.5.3
  reproduced).
