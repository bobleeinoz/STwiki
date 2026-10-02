---
title: Limited and moderately ductile structural wall earthquake detailing
category: 2-concrete
tags: [earthquake, seismic, structural-walls, boundary-elements, ductile-detailing]
standards: [AS 3600:2018 Cl 14.6, AS 3600:2018 Cl 14.7]
status: draft
reviewed: 2026-09-16
---

# Structural wall earthquake detailing

> Scope: AS 3600 Cl 14.6 (limited ductile structural walls, `μ = 2`) and
> Cl 14.7 (moderately ductile structural walls, `μ = 3`, which apply Cl 14.6
> with two modifications).

## Summary

`[code]` Both wall classes require vertical and horizontal reinforcement on
both wall faces, divided equally between the faces (Cl 14.6.1). Moderately
ductile walls (Cl 14.7.1) follow all of Cl 14.6 **except** the effective
height/thickness limit (Cl 14.6.5, replaced by Cl 14.7.2) and the boundary-
element restraint trigger (Cl 14.6.2, always restrained per Cl 14.5.4
regardless of calculated stress).

## Detail

### Boundary elements (Cl 14.6.2)

`[code]` Boundary elements are required at discontinuous wall edges and
around openings in any storey where (a) the storey-height vertical
reinforcement isn't laterally restrained per Cl 10.7.4, and (b) the
extreme-fibre compressive stress (from ULS design actions, linear-elastic
model, gross section) exceeds `0.15 f'c`. Not required around openings in
the middle third of a wall that are <25% of the wall's effective height and
<25% of its overall length.

`[code]` **≤4 storeys** (Cl 14.6.2.2): an integrally cast column, or two N16
bars tied with an N12 U-bar, or four N12 bars in R10 closed stirrups (ties at
the lesser of `tw` and 200 mm), satisfies the requirement.

![[as3600-fig-14.6.2.2-boundary-element-4-storeys.png]]
*Figure 14.6.2.2 — reinforcement of boundary elements for buildings of ≤4
storeys: 4N12 bars over `1.5tw`, R10 ties at the lesser of 200 mm centres and
`tw` (AS 3600:2018).*

`[code]` **>4 storeys** (Cl 14.6.2.3): the wall's horizontal cross-section is
treated as an I-beam (boundary elements = flanges, wall between = web).
Longitudinal reinforcement restraint follows Cl 10.7.4, or Cl 14.5.4 where
the extreme-fibre stress exceeds `0.2 f'c`; restraint is mandatory wherever
the stress exceeds `0.15 f'c`. Boundary elements are restrained by nominally
horizontal closed fitments at ≤ the lesser of `tw` and 200 mm, anchored
around the edge reinforcement.

![[as3600-fig-14.6.2.3-boundary-element-over-4-storeys.png]]
*Figure 14.6.2.3 — reinforcement of boundary elements for buildings >4
storeys: wall horizontal/vertical bars, U-bars lapped with/anchoring the
horizontal reinforcement into the boundary element (AS 3600:2018).*

### Wall core confinement, strength and slenderness (Cl 14.6.3–14.6.6)

`[code]` Where `f'c > 50 MPa`, the wall core is confined throughout by
fitments per Cl 14.5.4 (Cl 14.6.3). Mean tested 28-day cylinder strength
`< 1.4 f'c` (Cl 14.6.4). Effective-height-to-thickness ratio ≤20 for limited
ductile walls (Cl 14.6.5; ≤16 for moderately ductile, Cl 14.7.2). In-plane
shear (Cl 14.6.6) must satisfy `φVu ≥ min[(1.6Mu/M*)V* ; (μ/Sp)V*]`,
capturing flexural over-strength and dynamic amplification.

### Reinforcement ratios and critical tension zones (Cl 14.6.7)

`[code]` Minimum vertical ratio `ρwv ≥ 0.0025`, increased in plastic-hinge
regions to `ρwv ≥ 0.7√f'c/fsy` within a **Critical Tension Reinforcement
Zone** — (i) the outermost `Lw` region at each free wall end (Figure
14.6.7(A)); (ii) an integrated end column of area `≥ Lw × tw` (Figure
14.6.7(B)); or (iii) the full length of a transverse wall at the extreme
tension face of an interconnected group (Figure 14.6.7(C)) — and `ρwv ≥
0.35√f'c/fsy` elsewhere in the section. `Lw = max(0.15Lw, 1.5tw)`.

![[as3600-fig-14.6.7ab-critical-tension-reinforcement-zone.png]]
*Figure 14.6.7(A)/(B) — critical tension reinforcement zone at a free wall
end, and at a wall end integrated with a column: zone width
`max(0.15Lw, 1.5tw)` measured from the free/column end in the direction of
bending (AS 3600:2018). Figure 14.6.7(C), not reproduced, applies the same
zone to the extreme-tension-face wall of an interconnected group.*

`[code]` The increased ratio extends vertically from the wall base over the
greater of `2Lw` or the height of the lower two storeys (using the longest
wall of an interconnected group), reducible by 10%/floor above that height
to a floor of 0.0025. Vertical ratio is capped at `16/fsy`, relaxed to
`21/fsy` where lapped splices in boundary elements are unavoidable. Minimum
horizontal ratio `ρwh ≥ 0.0025`. Horizontal bars lapped within the central
2/3 (web) region need minimum 135° hooks with a full-strength splice.

![[as3600-fig-14.6.7d-horizontal-wall-bar-lap.png]]
*Figure 14.6.7(D) — horizontal wall bar lap detail: 135°-hooked bars lapped
over `Lsy.t.lap` within the wall web (AS 3600:2018).*

`[code]` At wall ends with boundary elements, horizontal bars are hooked/
cogged and fully anchored into the confined core, or lapped with U-bars over
`1.2 Lsy.t.lap`; without a boundary element (or under the Cl 14.6.2.2 U-bar
provision), horizontal bars terminate with full tension laps to U-bars of
the same diameter. Ductility Class L reinforcement is barred as structural
reinforcement. Wall reinforcement terminating into footings, columns, slabs
or beams must be anchored to develop `fsy` at that junction.

### Moderately ductile walls — additional requirements (Cl 14.7)

`[code]` Effective-height-to-thickness ≤16 (Cl 14.7.2). Vertical
reinforcement laps/mechanical splices within the greater of `2Lw` or the
lower-two-storey height (from immediately above the footing) must be evenly
staggered so ≤50% of the vertical steel is spliced at any horizontal
section, per the Figure 13.2.2 staggered arrangement (see
[[concrete-splicing-of-reinforcement]]) — using the longest wall for an
interconnected group.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-earthquake-design-basis]] — Cl 14.1–14.4, the `μ`/`Sp` routing
  (limited ductile `μ = 2`, moderately ductile `μ = 3`) into this page.
- [[concrete-earthquake-imrf-detailing]] — Cl 14.5, referenced restraint/
  fitment rules (Cl 14.5.4) reused here for boundary elements/wall cores.
- [[concrete-splicing-of-reinforcement]] — Cl 13.2.2/Figure 13.2.2, the
  staggered lap detail Cl 14.7.3 invokes.
- [[concrete-wall-reinforcement-requirements]], [[concrete-wall-design-basis-and-classification]]
  — Section 11 baseline wall reinforcement/classification this section
  overlays for earthquake design.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clauses 14.6–14.7
  (Figures 14.6.2.2, 14.6.2.3, 14.6.7(A)/(B), 14.6.7(D) reproduced in
  `wiki/2-concrete/assets/`; Figure 14.6.7(C) described in words).
