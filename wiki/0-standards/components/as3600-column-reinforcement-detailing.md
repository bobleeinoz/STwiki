---
title: Column reinforcement requirements (longitudinal limits, confinement, splicing)
category: 0-standards
tags: [columns, detailing, confinement, fitments, splicing]
standards: [AS 3600:2018 Cl 10.7]
status: draft
reviewed: 2026-09-12
---

# Column reinforcement requirements

> Scope: AS 3600 Cl 10.7 — longitudinal steel limits, the three functions of
> fitments (shear/torsion, core confinement, buckling restraint), fitment
> sizing/spacing/detailing, and splicing of longitudinal reinforcement.

## Summary

`[code]` Fitments in a column do three jobs at once (Cl 10.7.2): shear/
torsion reinforcement (Cl 8.2/8.3, see
[[as3600-beam-shear-and-torsion-design]] and [[as3600-beam-detailing]]),
core confinement (Cl 10.7.3), and lateral restraint of longitudinal bars
against buckling (Cl 10.7.4) — plus, for moment-resisting frames under
earthquake actions, confinement per Section 14. One set of fitments must
satisfy whichever of these demands is most onerous at a given location.

## Detail

### Longitudinal steel limits (Cl 10.7.1)

`[code]` Cross-sectional area of longitudinal reinforcement: not less than
1% of gross area `Ag` — reducible where the column is oversized for
strength, provided the reduced steel area still satisfies
`Asc·fsy > 0.15·N*`; not more than 4% of `Ag` unless placement/compaction at
splices and member junctions is demonstrably unaffected. Bundled bars: max 4
per bundle, tied together in contact (same rule as beams — see
[[as3600-beam-detailing]]).

### Core confinement (Cl 10.7.3)

`[code]` For `f'c ≤ 50 MPa`, confinement is deemed adequate wherever the
Cl 10.7.4 buckling-restraint spacing rules are met — no separate
confinement calculation needed. For `f'c > 50 MPa`, confinement must be
explicitly provided: in **special confinement regions** (defined below), to
a minimum effective confining pressure of `0.01·f'c`, by one of three
calculation routes; **outside** those regions, deemed adequate if fitment
spacing doesn't exceed the lesser of `0.8b`/300 mm and the Cl 10.7.4 spacing
limit.

`[code]` **Special confinement regions** trigger where either `N* ≥ 0.75φNuo`
or (`N* ≥ 0.3f'cAg` **and** `M* ≥ 0.6φMu`) — i.e. columns carrying
substantial axial load, with or without significant moment, need confined
zones near their critical sections. Within a confinement region, spacing
tightens further to the lesser of `0.6b`/300 mm. Region extent: measured
each side of the maximum-moment section, bounded by the lesser of 1.2× the
bending-plane cross-section dimension or the distance to the member end
(for double-curvature moment-resisting-frame columns within the trigger
range, the region instead extends from each member end by the larger of a
moment-ratio-based length or 1.2× the larger cross-sectional dimension).

![[as3600-fig-10.7.3.1a-confinement-to-the-core.png]]
*Figure 10.7.3.1(A) — confinement to the core, effective confining pressure
concept (AS 3600:2018).*

![[as3600-fig-10.7.3.1b-special-confinement-regions.png]]
*Figure 10.7.3.1(B) — extent of special confinement regions along a column
(AS 3600:2018).*

`[code]` Confining pressure calculation routes: **rational calculation**
(10.7.3.2, triaxial-stress-based, fitment-effectiveness-based — no
prescribed formula); **simplified calculation** (10.7.3.3), building an
effective confining pressure `fr.eff = ke·fr` from an average confining
pressure `fr` (itself from fitment leg area, yield strength, angle to the
confinement plane, number of legs crossing it, core dimension and fitment
spacing — assessed as the *smaller* of the two principal directions for
non-circular sections) and an effectiveness factor `ke` (a function of
restrained-bar count/spacing and core dimensions for rectangular sections, a
simpler spacing-to-core-diameter form for circular sections) — or,
alternatively, a volumetric-ratio-based shortcut (`fr.eff = 0.5·ke·ρs·fsy.f`,
where `ρs` is the fitment volume fraction of the core). **Deemed-to-conform**
(10.7.3.4): a maximum-spacing formula (different forms for rectangular vs.
circular sections) that guarantees the `0.01·f'c` target without an explicit
pressure calculation.

![[as3600-fig-10.7.3.3-calculation-of-confining-pressures.png]]
*Figure 10.7.3.3 — calculation of confining pressures `fr`/`fr.eff` from
fitment leg area, spacing and core dimensions (AS 3600:2018).*

### Restraint of longitudinal reinforcement (Cl 10.7.4)

`[code]` Bars requiring lateral restraint (10.7.4.1): every corner bar
always; all single bars where spacing >150 mm or `N* > 0.3·Ag·f'c`; at least
every alternate bar where spacing ≤150 mm; every bundle, regardless of
spacing. **Deemed restrained** (10.7.4.2) if held within and in contact with
a fitment bend of ≤135° included angle, between two 135° hooks, inside a
single 135° hook on a fitment roughly perpendicular to the column face, or —
for single-leg internal fitments — a 90° hook meeting a specific bundle of
conditions (opposite end has a 135° hook, alternating end-types on adjacent
fitments in plan and along the bar, `N* ≤ 0.3·Ag·f'c`, `f'c ≤ 65 MPa`); or,
for circular fitments/helices, simply having the bars equally spaced around
the circumference.

![[as3600-fig-10.7.4.2-lateral-restraint-to-longitudinal-bars.png]]
*Figure 10.7.4.2 — deemed-restrained configurations for lateral restraint of
longitudinal bars by fitment bends/hooks (AS 3600:2018).*

`[code]` **Fitment/helix diameter and spacing** (10.7.4.3): minimum bar
diameter from Table 10.7.4.3 — banded by longitudinal bar
diameter, single vs. bundled.

![[as3600-table-10.7.4.3-bar-diameters-fitments-helices-1.png]]
![[as3600-table-10.7.4.3-bar-diameters-fitments-helices-2.png]]
*Table 10.7.4.3 — minimum bar diameters for fitments and helices, by
longitudinal bar diameter and bundling (AS 3600:2018).*

`[code]` This is reducible for higher-strength fitment steel
by a `√(500/fsy.f)`-type factor. Spacing capped at the lesser of `b`/`15dᵦ`
(single bars) or `0.5b`/`7.5dᵦ` (bundled bars) — tightened further under
Section 14 where `Lu ≤ 5D`. First/last fitment (or helix turn) within 50 mm
of a footing top or slab soffit/top, adjusted for column capitals or beams
framing in from all four sides.

`[code]` **Detailing** (10.7.4.4): rectangular fitments spliced by welding or
two 135° hooks at a corner (internal fitments may lap within the core);
circular fitments similarly; helices anchored by 1.5 extra turns at each end,
spliced by welding or mechanical means; bend diameters increased where
hooks/cogs combine with bundled bars.

`[code]` **Column joint reinforcement** (10.7.4.5): where floor-system
bending moments transfer into a column, lateral shear reinforcement
`Asv ≥ 0.35·b·s/fsy.f` is required through the joint — omissible over the
depth of the shallowest slab/beam where a slab or beams exist on all four
sides.

### Splicing (Cl 10.7.5)

`[code]` Every splice face needs a minimum tensile strength `0.25·fsy·As`
regardless of actual design tension (10.7.5.2). Where design tension at a
splice exceeds that minimum, the force must transfer by a welded/mechanical
splice (Cl 13.2.6) or a tension lap splice (Cl 13.2.2/13.2.5) — not by
bearing alone (10.7.5.3). Splices always in compression may instead use
square-cut mating ends in a sleeve, with additional fitments above/below the
sleeve per Cl 10.7.4, bars rotated for maximum contact area, and the
Cl 10.7.5.2 minimum tension strength still satisfied. **Offset bars**
(10.7.5.5): inclined portion slope ≤1:6, parallel bar portions either side
of the offset, lateral support at the offset; where a column face itself
offsets ≥75 mm, bars must not be bent through the offset — use separate
lap-spliced bars adjacent to the offset faces instead.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-beam-shear-and-torsion-design]], [[as3600-beam-detailing]] —
  Section 8 shear/torsion and detailing rules fitments must also satisfy.
- [[as3600-column-strength-interaction]] — spalling/confinement
  interaction referenced from Cl 10.6.
- [[as3600-column-floor-joint-transmission]] — Cl 10.8/10.9, the remaining
  Section 10 clauses.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 10.7 (Figures
  10.7.3.1, 10.7.3.3, 10.7.4.2 and Table 10.7.4.3 reproduced as image assets).
