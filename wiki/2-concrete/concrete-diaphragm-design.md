---
title: Diaphragm design — actions, toppings and reinforcement
category: 2-concrete
tags: [diaphragms, collectors, cast-in-place-toppings, seismic]
standards: [AS 3600:2018 Cl 15.1, AS 3600:2018 Cl 15.2, AS 3600:2018 Cl 15.3, AS 3600:2018 Cl 15.4]
status: draft
reviewed: 2026-09-16
---

# Diaphragm design

> Scope: AS 3600 Section 15 in full — general scope (Cl 15.1), design
> actions and analysis (Cl 15.2), cast-in-place toppings on prefabricated
> floors (Cl 15.3), and diaphragm reinforcement including collectors (Cl
> 15.4). No figures or tables in this section.

## Summary

`[code]` Section 15 applies to conventionally reinforced and prestressed
diaphragms — cast-in-situ slabs (with or without beams) and cast-in-situ
topping slabs on prefabricated concrete (Cl 15.1). Diaphragms are part of
the primary structure, with identifiable internal load paths transferring
actions between the diaphragm and the elements of the lateral-force-
resisting system; both diaphragm elements and their connections must
accommodate the imposed displacement **and** force demands.

## Detail

### Design actions and analysis (Cl 15.2)

`[code]` Design actions (Cl 15.2.1) include: permanent/imposed floor or roof
actions; diaphragm in-plane forces from lateral loads (including floor
design accelerations/inertia loads under seismic actions per Cl 14.4.5 — see
[[concrete-earthquake-design-basis]]); force transfer between lateral-
force-resisting elements interconnected by the diaphragm; and interaction
with elements supporting the diaphragm vertically or near-vertically. Load
combinations follow AS 1170.0, with in-plane and out-of-plane loading
assumed concurrent where relevant; forces at vertical-stiffness
discontinuities or plan irregularities between storeys must be considered.

`[code]` Analysis (Cl 15.2.2.1): rational analysis establishes adequate ULS
in-plane flexural and shear strength, optionally via a Section 7
strut-and-tie model (see [[concrete-strut-and-tie-modelling]]); opening/
penetration effects must be considered. Cracking/joint-opening effects from
distributed in-plane-tension reinforcement may be ignored if that
reinforcement is distributed within 1/4 of the diaphragm width from the
tension edge. Stiffness (Cl 15.2.2.2): where the diaphragm's calculated
maximum lateral deformation exceeds half the average inter-storey deflection
of the associated vertical lateral-force-resisting elements, the diaphragm
is **flexible** and its displacement must be included in the structural
analysis.

### Cast-in-place toppings (Cl 15.3)

`[code]` A topping cast on a prefabricated floor/roof may act as a structural
diaphragm if either: (a) the topping alone is proportioned/detailed to
resist the diaphragm forces, with minimum 75 mm thickness; or (b) sufficient
Cl 8.4 composite reinforcement is provided so topping and precast elements
act compositely, the substrate surface is clean/laitance-free/intentionally
roughened, and the topping is ≥65 mm thick (excluding the precast element)
everywhere within the diaphragm.

### Diaphragm reinforcement (Cl 15.4)

`[code]` Where concentrated actions develop (collector elements, diaphragm
perimeter under in-plane bending), only Ductility Class N reinforcement or
bonded post-tensioning may resist diaphragm forces (Cl 15.4.1). Diaphragm
reinforcement is additional to reinforcement for other load effects, except
shrinkage/temperature steel may double up. Minimum reinforcement follows Cl
9.5.3 in both orthogonal directions, spacing capped per Cl 9.5.1 (Cl 15.4.2).
Development/lap effects, and stresses induced by vertical actions, are
included per Section 13 (Cl 15.4.3 — see
[[concrete-development-length-of-reinforcement]] and
[[concrete-development-of-tendons-and-coupling]]).

`[code]` **Collectors** (Cl 15.4.4) transfer concentrated diaphragm forces to
the lateral-system vertical elements, extending beyond the point where
analysis shows the collector is no longer in tension by at least one
development length, and along the vertical element for the greater of: (a)
the Section 13 tension development length at the wall face; (b) the Cl 8.4
longitudinal-shear transfer length; or (c) a mechanical/tension lap per
Section 13. Splices in collector elements are permitted only where the
splice length develops the full yield strength (Section 13).

`[code]` **Construction joints** (Cl 15.4.5): diaphragm-force transfer across
a construction joint may only be assumed where sufficient fully-developed
reinforcement crosses the joint; mechanical connectors may substitute,
designed for the required tension under anticipated joint opening.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-earthquake-design-basis]] — Cl 14.4.5, seismic diaphragm
  inertia-force calculation feeding this section's design actions.
- [[concrete-strut-and-tie-modelling]] — Section 7, the optional analysis
  route for diaphragm in-plane strength.
- [[concrete-development-length-of-reinforcement]],
  [[concrete-development-of-tendons-and-coupling]],
  [[concrete-splicing-of-reinforcement]] — Section 13 development/splice
  rules this section applies to collectors and diaphragm reinforcement.
- [[concrete-beam-longitudinal-shear-composite]] — Cl 8.4, composite-action
  reinforcement referenced for cast-in-place toppings and collector
  transfer.
- [[concrete-slab-crack-control]] — Cl 9.5, minimum-reinforcement/spacing
  rules Cl 15.4.2 points to.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clauses 15.1–15.4 (no
  figures or tables in this section).
