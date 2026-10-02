---
title: ACI 318M-19 beam-column and slab-column joints — detailing, joint shear strength, column axial force through floors
category: 2-concrete
tags: [aci, joints, beam-column-joint, slab-column-joint, joint-shear]
standards: [ACI 318M-19 Cl 15.1, ACI 318M-19 Cl 15.2, ACI 318M-19 Cl 15.3, ACI 318M-19 Cl 15.4, ACI 318M-19 Cl 15.5]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 beam-column and slab-column joints

> Scope: ACI 318M-19 Chapter 15 in full — which joints it covers, general
> conditions (strut-and-tie trigger, column/beam extensions, confinement by
> transverse beams), transverse and longitudinal reinforcement detailing, joint
> shear strength `V_n`, and transfer of column axial force through a floor
> system of lower-strength concrete. Special moment frame joints are in
> Cl 18.8 and are not covered here. This is an **ACI 318M-19 page, kept
> separate from the AS 3600:2018 concept pages** elsewhere in `2-concrete` —
> see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Chapter 15 applies to **cast-in-place** beam-column and slab-column
joints (Cl 15.1.1). Beam-column joints satisfy the detailing of Cl 15.3 and the
strength requirements of Cl 15.4 (Cl 15.2.1); all joints satisfy Cl 15.5 for
column axial force transfer through the floor (Cl 15.2.2). Where gravity, wind,
earthquake or other lateral forces transfer moment at a beam-column joint, the
resulting joint shear is designed for (Cl 15.2.3), and at corner joints the
effects of closing and opening moments are considered (Cl 15.2.4). Slab-column
connections transferring moment follow Chapter 8 (see
[[aci318-two-way-slab-design-basis]]), Cl 15.3.2 and Cl 22.6 (see
[[aci318-two-way-shear-strength]]) (Cl 15.2.9).

## Detail

### General conditions (Cl 15.2.5–15.2.8)

`[code]` **Deep beams**: if a beam framing into the joint and generating joint
shear has depth **exceeding twice the column depth**, the joint is analysed and
designed by the strut-and-tie method of Chapter 23 (see
[[aci318-strut-and-tie-method]]), with the Chapter 23 joint shear strength not
exceeding `φV_n` from Cl 15.4.2 and the Cl 15.3 detailing satisfied (Cl 15.2.5).

`[code]` **Extensions providing continuity** through a joint in the direction of
joint shear considered: a *column extension* extends above the joint at least one
column depth `h` (measured in the shear direction) with the lower column's
longitudinal and transverse steel continued through it (Cl 15.2.6); a *beam
extension* extends at least one beam depth `h` beyond the joint face with the
opposite-side beam's longitudinal and transverse steel continued through it
(Cl 15.2.7).

`[code]` **Confinement by transverse beams** (Cl 15.2.8): a beam-column joint is
*confined* in the direction of joint shear considered if **two** transverse beams
are provided, each (a) at least three-quarters the width of the column face it
frames into, (b) extending at least one beam depth `h` beyond the joint faces,
and (c) containing at least two continuous top and bottom bars satisfying
Cl 9.6.1.2 and No. 10 or larger stirrups satisfying Cl 9.6.3.4 and 9.7.6.2.2.

### Detailing of joints (Cl 15.3)

`[code]` **Beam-column joint transverse reinforcement** (Cl 15.3.1): ties,
spirals or hoops per Cl 25.7.2/25.7.3/25.7.4; at least **two layers** of
horizontal transverse reinforcement within the depth of the **shallowest** beam
framing into the joint; spacing `s ≤ 200 mm` within the depth of the **deepest**
beam. This is **not required** if all of: (a) the joint is confined by transverse
beams per Cl 15.2.8 for every shear direction considered, (b) it is not part of a
designated seismic-force-resisting system, and (c) the structure isn't in SDC
D, E or F (Cl 15.3.1.1).

`[code]` **Slab-column joints** (Cl 15.3.2): column transverse reinforcement is
continued through the joint, including capital, drop panel and shear cap, per
Cl 25.7.2/25.7.3/25.7.4 — except where the joint is laterally supported on four
sides by a slab.

`[code]` **Longitudinal reinforcement** (Cl 15.3.3): bars terminated in the joint
or within a column/beam extension (Cl 15.2.6(a), 15.2.7(a)) are developed per
Cl 25.4, and bars terminated in the joint with a standard hook have the hook
turned **toward mid-depth** of the beam or column.

### Joint shear strength (Cl 15.4)

`[code]` `V_u` is calculated on a plane at **mid-height of the joint**, using
flexural tensile and compressive beam forces together with column shear,
consistent with either (a) the maximum moment transferred between beam and column
from factored-load analysis (for joints with beams continuous in the shear
direction) or (b) beam nominal moment strengths `M_n` (Cl 15.4.1.1). Design
requirement `φV_n ≥ V_u`, φ per Cl 21.2.1 for shear (Cl 15.4.2.1–15.4.2.2; see
[[aci318-strength-reduction-factors]]). `V_n` follows Table 15.4.2.3:

![[aci318-table-15.4.2.3-nominal-joint-shear-strength.png]]
*Table 15.4.2.3 — nominal joint shear strength `V_n` as a multiple of
`λ√f'c A_j` (N): from `2.0` (column continuous or meeting Cl 15.2.6, beam
continuous or meeting Cl 15.2.7, joint confined) down to `1.0` (neither column
nor beam continuous, joint not confined), with intermediate values `1.7`/`1.3`
for mixed cases; `λ = 0.75` for lightweight, `1.0` for normalweight concrete
(ACI 318M-19).* `[derived]` The more continuity (column and beam extensions
through the joint) and the more confinement (transverse beams), the higher the
allowed shear stress; the table encodes the same hierarchy Cl 15.2.6–15.2.8
defines.

`[code]` **Effective joint area** `A_j = (joint depth) × (effective joint
width)`: joint depth is the overall column depth `h` in the direction of joint
shear; effective width is the full column width where the beam is wider than the
column, and where the column is wider than the beam it is at most the lesser of
(a) beam width plus joint depth and (b) twice the perpendicular distance from the
beam axis to the nearest column side face (Cl 15.4.2.4):

![[aci318-fig-r15.4.2-effective-joint-area.png]]
*Fig. R15.4.2 — effective joint area `A_j` in plan: joint depth `h` parallel to
the reinforcement generating shear, effective width the lesser of `(b + h)` and
`(b + 2x)`; the joint area is considered separately for forces in each direction
of framing (ACI 318M-19).*

### Transfer of column axial force through the floor system (Cl 15.5)

`[code]` If the floor system's `f'c` is **less than 0.7 × the column `f'c`**,
axial force transfer through the floor follows one of (Cl 15.5.1): (a) place
column-strength concrete in the floor system at the column location, extending
at least **600 mm** outward from the column face for the full floor depth and
integrated with the floor concrete; (b) calculate the column design strength
through the floor using the **lower** concrete strength, with vertical dowels
and transverse reinforcement as needed; or (c) for joints laterally supported on
four sides by beams of approximately equal depth (satisfying Cl 15.2.7 and
15.2.8(a)) or, for slab-column joints, on four sides by the slab, calculate the
column strength using an assumed joint concrete strength equal to **75% of column
strength plus 35% of floor-system strength**, where the column strength used does
not exceed **2.5 ×** the floor-system strength.

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-beam-design-basis-and-strength]], [[aci318-column-design]],
  [[aci318-two-way-slab-design-basis]] — member chapters that route their
  joints here.
- [[aci318-strut-and-tie-method]] — mandatory for deep-beam joints.
- [[concrete-column-floor-joint-transmission]] — the AS 3600 equivalent for
  axial force transmission through floors, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 15 Cl 15.1–15.5 (pp. 211–215),
  incl. Table 15.4.2.3 and Fig. R15.4.2.
