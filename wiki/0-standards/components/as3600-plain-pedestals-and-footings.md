---
title: Plain concrete pedestals and footings
category: 0-standards
tags: [plain-concrete, pedestals, footings, unreinforced]
standards: [AS 3600:2018 Cl 20.1, AS 3600:2018 Cl 20.2, AS 3600:2018 Cl 20.3, AS 3600:2018 Cl 20.4]
status: draft
reviewed: 2026-09-17
---

# Plain concrete pedestals and footings

> Scope: AS 3600 Section 20 in full — applicability (Cl 20.1), durability
> (Cl 20.2), pedestals (Cl 20.3), footings — dimensions, bending, shear (Cl
> 20.4). No figures of its own in this section; it reuses Figure 9.3(A)/(B)
> from Section 9, reproduced below.

## Summary

`[code]` Section 20 applies to (a) plain concrete pedestals with unsupported
height ≤3× the least lateral dimension, and (b) plain concrete pad footings
supported by the ground (Cl 20.1). The capacity reduction factor `φ`
throughout is read from Table 2.2.2.

## Detail

### Durability (Cl 20.2)

`[code]` Plain concrete members conform with Section 4; cover to any
reinforcement present also follows Section 4 (see
[[as3600-durability-and-cover]]).

### Pedestals (Cl 20.3)

`[code]` Under combined flexure and axial load, the maximum compressive
stress must not exceed `φ·0.4f'c` and the maximum tensile stress must not
exceed `φ·0.45√f'c`. Minimum eccentricity is `0.1a` (`a` = the cross-section
dimension in the direction considered).

### Footings — dimensions and bending (Cl 20.4.1–20.4.2)

`[code]` Minimum nominal footing depth is 200 mm. Strength is calculated
over the entire cross-section, with the effective depth taken as the
**nominal depth minus 50 mm**. Design strength in bending (`Muo`) uses the
characteristic flexural tensile strength `f'ctf`, with a linear stress-
strain relationship assumed in both tension and compression. The critical
bending section is: (a) the face of the column/pedestal/wall for concrete
members; (b) halfway between centre and face for a masonry wall; or (c)
halfway between the column face and base-plate edge for a steel column and
base plate.

### Footings — shear (Cl 20.4.3)

`[code]` **One-way (wide-beam) shear**, where failure spans the rectangular
cross-section width `b`: design strength `φVu` where `Vu = 0.15 b D
(f'c)^(1/3)` (Eq 20.4.3(1)), critical section taken at `0.5D` from the
support face.

`[code]` **Local (punching) shear**, around a support or loaded area: design
strength `φVu / [1 + (u M*)/(8 V* a D)]` (Eq 20.4.3(2)), where `Vu = 0.1 u D
(1 + 2/βh) √f'c ≤ 0.2 u D √f'c`; `u` = effective length of the shear
perimeter (Figure 9.3(A)); `a` = dimension of the critical shear perimeter
parallel to the bending direction considered (Figure 9.3(B)); `βh` = ratio
given in Cl 9.3.1.4 — see [[as3600-slab-punching-shear]] for the Section 9
definitions of `u`, `a` and `βh` this clause reuses.

![[as3600-fig-9.3a-critical-shear-perimeter.png]]
*Figure 9.3(A) — critical shear perimeter, offset `dom/2` from the boundary
of the effective area of support or load (`dom` becomes `D` for the plain
concrete footings/pedestals of this section): (a) without critical
openings; (b) with critical openings within `2.5bo` (AS 3600:2018,
Section 9 figure, reused by Cl 20.4.3).*

![[as3600-fig-9.3b-torsion-strips-and-spandrel-beams.png]]
*Figure 9.3(B) — torsion strips (width `a`) and spandrel beams, offset
`dom/2` from the critical shear perimeter — `a` is the dimension Eq
20.4.3(2) uses for the critical shear perimeter parallel to the bending
direction considered (AS 3600:2018, Section 9 figure, reused by Cl 20.4.3).*

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-slab-on-ground-pavements-and-footings]] — Section 21, plain
  concrete footings there defer to this section (Cl 21.3.2).
- [[as3600-slab-punching-shear]] — Cl 9.3, the reinforced-slab punching-
  shear framework (`u`, `βh`, Figure 9.3) this section's shear clause reuses
  for plain concrete.
- [[as3600-durability-and-cover]] — Section 4, durability/cover basis for
  plain concrete members.
- [[as3600-strength-check-procedures]] — Cl 2.2/Table 2.2.2, the `φ`
  values used throughout this section.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clauses 20.1–20.4 (no
  figures of its own; Figure 9.3(A)/(B), extracted from Section 9, are
  embedded above from `wiki/0-standards/assets/`).
