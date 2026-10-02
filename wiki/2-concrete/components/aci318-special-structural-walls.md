---
title: ACI 318M-19 special structural walls — reinforcement, design shear, boundary elements, coupling beams, wall piers, precast walls
category: 2-concrete
tags: [aci, earthquake, seismic, special-structural-wall, boundary-elements, coupling-beams]
standards: [ACI 318M-19 Cl 18.10, ACI 318M-19 Cl 18.11]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 special structural walls

> Scope: ACI 318M-19 Cl 18.10 (special structural walls, including ductile
> coupled walls, coupling beams and wall piers) and Cl 18.11 (precast special
> structural walls). SDC routing is on
> [[aci318-earthquake-general-and-ordinary-intermediate-frames]]; ordinary wall
> design is on [[aci318-wall-design]]. This is an **ACI 318M-19 page, kept
> separate from the AS 3600:2018 concept pages** elsewhere in `2-concrete` — see
> [[aci-318m-19-building-code-concrete]] for why. The AS 3600 counterpart is
> [[concrete-earthquake-structural-walls-detailing]] (limited/moderately ductile
> walls) — the ACI "special wall" tier has no direct AS 3600 equivalent.

## Summary

`[code]` Special structural walls (Cl 18.10.1.1) and their components — coupling
beams, wall piers — get ductile detailing driven by three ideas: distributed web
steel and development rules that tolerate yielding (Cl 18.10.2), **capacity-based
design shear** `V_e = Ω_v ω_v V_u ≤ 3V_u` (Cl 18.10.3), and **boundary elements**
confining the compression zone where drift or stress demand is high
(Cl 18.10.6). Precast special walls follow Cl 18.10 plus Cl 18.5.2 yielding rules
(Cl 18.10.1.2, 18.11).

## Detail

### Reinforcement (Cl 18.10.2)

`[code]` Distributed web steel `ρ_ℓ`, `ρ_t ≥ 0.0025`, except `ρ_t` may drop to the
Cl 11.6 values if `V_u ≤ 0.083λ√f'c A_cv`; spacing each way ≤ **450 mm**; shear
steel is continuous and distributed across the shear plane (Cl 18.10.2.1). **At least
two curtains** if `V_u > 0.17λ√f'c A_cv` or `h_w/ℓ_w ≥ 2.0` (Cl 18.10.2.2).
Development/splice for `f_y` per Cl 25.4/25.5 plus (Cl 18.10.2.3): longitudinal bars
extend ≥ **3.6 m** above where no longer needed for flexure (but ≤ `ℓ_d` above the next
floor) except at the wall top; where yielding is likely, development lengths ×
**1.25**; **no lap splices** in boundary regions within `h_sx` (≤ 6 m) above and `ℓ_d`
below critical yielding sections:

![[aci318-fig-r18.10.2.3-wall-boundary-regions-no-lap-splices.png]]
*Fig. R18.10.2.3 — wall boundary regions within the heights where lap splices are
not permitted: (a) elevation showing the critical section, `≥ min(h_sx, 6 m)` above
it and `≥ ℓ_d` below; (b) plan showing boundary regions of length `ℓ_be` and the
wall-intersection boundary regions (ACI 318M-19).*

`[code]` Walls or piers with `h_w/ℓ_w ≥ 2.0` that are continuous base-to-top with a
single critical section (Cl 18.10.2.4) need, at each end of a vertical wall segment:
longitudinal steel ratio ≥ `0.5√f'c/f_y` within `0.15ℓ_w` of the end over the wall
thickness; extending above and below the critical section ≥ the greater of `ℓ_w` and
`M_u/(3V_u)`; with ≤ 50% terminated at any one section:

![[aci318-fig-r18.10.2.4-wall-end-longitudinal-reinforcement.png]]
*Fig. R18.10.2.4 — locations of the Cl 18.10.2.4(a) end longitudinal reinforcement
(within `0.15ℓ_w`) for rectangular, barbell, flanged, T- and L-shaped wall sections
(ACI 318M-19).* Coupling beam reinforcement is developed for `f_y` per Cl 25.4/25.5 with
development lengths × **1.25** when reinforced per Cl 18.6.3.1 (longitudinal bars) or
Cl 18.10.7.4 (diagonal bars) (Cl 18.10.2.5).

### Design forces and shear strength (Cl 18.10.3–18.10.4)

`[code]` **Design shear** `V_e = Ω_v ω_v V_u ≤ 3V_u` (Eq. 18.10.3.1), `V_u` from the code
lateral analysis. `Ω_v`:

![[aci318-table-18.10.3.1.2-overstrength-factor-omega-v.png]]
*Table 18.10.3.1.2 — `Ω_v` at the critical section: for `h_wcs/ℓ_w > 1.5`, the greater
of `M_pr/M_u` and 1.5 (a smaller value permitted by detailed analysis but ≥ 1.0);
for `h_wcs/ℓ_w ≤ 1.5`, 1.0 (ACI 318M-19).* `ω_v = 1.0` for `h_wcs/ℓ_w < 2.0`,
otherwise `0.9 + n_s/10 ≤ 1.3 + n_s/30` (Eq. 18.10.3.1.3 — first form for
`n_s ≤ 6`, second for `n_s > 6`), with `n_s` ≥ `0.00028h_wcs`:

![[aci318-fig-r18.10.3.1-shear-demand-slender-walls.png]]
*Fig. R18.10.3.1 — determination of shear demand for walls with `h_w/ℓ_w ≥ 2.0`
(Moehle et al. 2011): lateral forces, wall elevation, shear `V_u` vs amplified `V_e`,
and moment `M_u` vs `M_pr` giving `Ω_v = M_pr,CS/M_u,CS` (ACI 318M-19).*

`[code]` **Shear strength** `V_n = (α_c λ√f'c + ρ_t f_yt)A_cv` (Eq. 18.10.4.1),
`α_c = 0.25` (`h_w/ℓ_w ≤ 1.5`), `0.17` (`≥ 2.0`), linear between; `h_w/ℓ_w` for a segment
is the greater of the whole-wall and segment ratios (Cl 18.10.4.2); distributed steel
in two orthogonal directions, with `ρ_ℓ ≥ ρ_t` if `h_w/ℓ_w ≤ 2.0` (Cl 18.10.4.3).
For all vertical segments sharing a lateral force `V_n ≤ 0.66√f'c A_cv`; for any one
vertical segment `V_n ≤ 0.83√f'c A_cw`; for horizontal segments and coupling beams
`V_n ≤ 0.83√f'c A_cw` (Cl 18.10.4.4–18.10.4.5). Cl 21.2.4.1 (φ = 0.6 for
shear-controlled members) does not apply to walls designed per Cl 18.10.6.2
(Cl 18.10.4.6; see [[aci318-strength-reduction-factors]]).

### Flexure and axial force (Cl 18.10.5)

`[code]` Designed per Cl 22.4 counting concrete and developed longitudinal steel in
effective flanges, boundary elements and web, and considering openings
(Cl 18.10.5.1). Unless analysed in more detail, effective flange width extends from
the web face the lesser of half the distance to an adjacent web and 25% of the wall
height above the section (Cl 18.10.5.2).

### Boundary elements (Cl 18.10.6)

`[code]` Two alternative triggers (Cl 18.10.6.1):

**(a) Displacement-based** (`h_wcs/ℓ_w ≥ 2.0`, continuous base-to-top, single
critical section) (Cl 18.10.6.2): special boundary elements are required where
**1.5δ_u/h_wcs ≥ ℓ_w/(600c)** (Eq. 18.10.6.2a), `c` the largest neutral axis depth at
factored axial force and nominal moment strength consistent with the design
displacement `δ_u`, and `δ_u/h_wcs` not taken below 0.005. If required, (i)
transverse steel extends above and below the critical section at least the greater
of `ℓ_w` and `M_u/(4V_u)` (except as Cl 18.10.6.4(i) permits), **and** either
(ii) `b ≥ √(0.025cℓ_w)`, or (iii) `δ_c/h_wcs ≥ 1.5δ_u/h_wcs`, where
`δ_c/h_wcs = (1/100)[4 − (1/50)(ℓ_w/b)(c/b) − V_e/(0.66√f'c A_cv)]` (Eq. 18.10.6.2b,
not taken below 0.015).

**(b) Stress-based** (all other walls) (Cl 18.10.6.3): special boundary elements at
edges and around openings where the maximum extreme-fibre compressive stress from
earthquake combinations (linear elastic, gross section) exceeds **0.2f'c**; they may
stop where stress falls below **0.15f'c**.

`[code]` **Where a special boundary element is required** (Cl 18.10.6.4): it extends
horizontally from the extreme compression fibre the greater of `c − 0.1ℓ_w` and `c/2`;
flexural compression-zone width `b ≥ h_u/16`, and ≥ **300 mm** for walls with
`c/ℓ_w ≥ 3/8` meeting Cl 18.10.6.4(c); in flanged sections it includes the effective
compression flange and extends ≥ 300 mm into the web. Transverse steel meets
Cl 18.7.5.2(a)–(d) and 18.7.5.3 except the spacing limit (a) becomes **one-third** of
the least boundary-element dimension, with maximum vertical spacing also per Table
18.10.6.5(b); `h_x` ≤ the lesser of 350 mm and two-thirds the boundary-element
thickness, hoop legs ≤ 2× that thickness, adjacent hoops overlapping ≥ the lesser of
150 mm and two-thirds thickness:

![[aci318-table-18.10.6.4g-transverse-reinforcement-special-boundary-elements.png]]
*Table 18.10.6.4(g) — transverse reinforcement for special boundary elements:
`A_sh/sb_c` greater of `0.3(A_g/A_ch − 1)f'c/f_yt` and `0.09f'c/f_yt`; `ρ_s` greater of
`0.45(A_g/A_ch − 1)f'c/f_yt` and `0.12f'c/f_yt` (ACI 318M-19).*

![[aci318-fig-r18.10.6.4a-boundary-transverse-reinforcement-configurations.png]]
*Fig. R18.10.6.4a — boundary transverse reinforcement configurations: (a) perimeter
hoop with supplemental 135° crossties; (b) overlapping hoops with supplemental
crossties, and 135° crossties supporting web longitudinal bars (ACI 318M-19).*

`[code]` Further: floor-system concrete at the boundary element has `f'c ≥ 0.7×` the
wall's (Cl 18.10.6.4(h)); web vertical steel above/below the critical section has
hoop-corner or seismic-hook crosstie support at ≤ 300 mm vertical spacing
(Cl 18.10.6.4(i)); at the wall base, boundary transverse steel extends `ℓ_d` into the
support (≥ 300 mm into a footing/mat/pile cap) (Cl 18.10.6.4(j)); web horizontal steel
reaches within 150 mm of the wall end and anchors for `f_y` in the confined core by
hooks/heads (Cl 18.10.6.4(k)).

![[aci318-fig-r18.10.6.4c-boundary-element-requirements-summary.png]]
*Fig. R18.10.6.4c — summary of boundary element requirements for special walls:
`σ ≥ 0.2f'c` triggers a special boundary element extending until `σ < 0.15f'c`; below
that, ties per Cl 18.10.6.5 if `ρ > 2.8/f_y`, none if `ρ ≤ 2.8/f_y`; around openings,
bars developed for `f_y` past the opening (ACI 318M-19).*

`[code]` **Where not required** (Cl 18.10.6.5): unless `V_u < 0.083λ√f'c A_cv`,
horizontal steel ending at wall edges has a standard hook engaging the edge steel or
the edge steel is enclosed in matching U-stirrups; if boundary longitudinal ratio
exceeds `2.8/f_y`, boundary transverse steel meets Cl 18.7.5.2(a)–(e) over the
Cl 18.10.6.4(a) distance at maximum vertical spacing per:

![[aci318-table-18.10.6.5b-max-vertical-spacing-wall-boundary.png]]
*Table 18.10.6.5(b) — maximum vertical spacing of boundary transverse reinforcement:
within the greater of `ℓ_w` and `M_u/(4V_u)` above/below critical sections the lesser
of `6d_b`/150 mm (G420), `5d_b`/150 mm (G550), `4d_b`/150 mm (G690); elsewhere the
lesser of `8d_b`/200 mm (G420), `6d_b`/150 mm (G550, G690) (ACI 318M-19).*

### Coupling beams (Cl 18.10.7)

`[code]` Coupling beams with `ℓ_n/h ≥ 4` satisfy Cl 18.6 (wall boundary treated as a
column), with Cl 18.6.2.1(b)–(c) waivable if lateral stability is shown (Cl 18.10.7.1).
Those with `ℓ_n/h < 2` **and** `V_u ≥ 0.33λ√f'c A_cw` use **two intersecting groups of
diagonal bars** symmetrical about midspan, unless loss of stiffness/strength is shown
not to impair gravity load path, egress or nonstructural integrity (Cl 18.10.7.2);
others may use diagonals or Cl 18.6.3–18.6.5 (Cl 18.10.7.3). For diagonally reinforced
beams (Cl 18.10.7.4): `V_n = 2A_vd f_y sin α ≤ 0.83√f'c A_cw` (Eq. 18.10.7.4); each
group ≥ **four bars** in two or more layers; and confinement by either (c) hoops
around each diagonal group (out-to-out ≥ `b_w/2` parallel to `b_w`, `b_w/5` on the
other sides; spacing along the diagonals ≤ the lesser of `s_o` per Eq. 18.7.5.3(d) and
`6d_b`, ≤ 350 mm perpendicular, plus extra perimeter steel ≥ `0.002b_w s` at ≤ 300 mm)
or (d) hoops/crossties for the **whole beam section** (spacing ≤ the lesser of 150 mm
and `6d_b`, legs/crossties ≤ 200 mm each way):

![[aci318-fig-r18.10.7a-coupling-beam-diagonal-confinement.png]]
*Fig. R18.10.7a — confinement of individual diagonals in a coupling beam with
diagonal reinforcement: elevation, Section A-A hoops around each diagonal group,
`≥ b_w/2` (ACI 318M-19).*

![[aci318-fig-r18.10.7b-coupling-beam-full-section-confinement.png]]
*Fig. R18.10.7b — full confinement of the diagonally reinforced beam section:
elevation, Section B-B with hoops/crossties over the whole section at ≤ 200 mm
(ACI 318M-19).*

### Wall piers, ductile coupled walls, joints, discontinuous walls (Cl 18.10.8–18.10.11)

`[code]` **Wall piers** satisfy the special-moment-frame column provisions of
Cl 18.7.4–18.7.6 (joint faces at the top/bottom of the clear height), or if
`ℓ_w/b_w > 2.5`: design shear per Cl 18.7.6.1 (not exceeding `Ω_o ×` analysed
earthquake shear where the general code provides overstrength); `V_n` and distributed
steel per Cl 18.10.4; hoops (single-leg horizontal steel with 180° bends allowed with
one curtain); vertical spacing ≤ 150 mm; extending ≥ 300 mm above and below the
clear height; special boundary elements if required by Cl 18.10.6.3 (Cl 18.10.8.1).
Edge piers need adjacent-segment horizontal steel to transfer the design shear
(Cl 18.10.8.2). **Ductile coupled walls** (Cl 18.10.9): each wall `h_wcs/ℓ_w ≥ 2` and
a special wall; coupling beams `ℓ_n/h ≥ 2` everywhere, `≤ 5` at every floor in ≥ 90%
of levels, with Cl 18.10.2.5 development at both ends. **Construction joints** per
Cl 26.5.6 with roughened surface (condition (b) of Table 22.9.4.2) (Cl 18.10.10);
columns under **discontinuous walls** per Cl 18.7.5.6 (Cl 18.10.11).

### Precast special structural walls (Cl 18.11)

`[code]` Satisfy Cl 18.10 and 18.5.2 (yielding restricted to steel elements,
non-yielding connection parts for 1.5S_y), except Cl 18.10.2.4 doesn't apply where
deformation demand is concentrated at panel joints (Cl 18.11.2.1); unbonded
post-tensioned precast walls not meeting that may be used if they meet ACI ITG-5.1M
(Cl 18.11.2.2).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-wall-design]] — Chapter 11 ordinary walls; Cl 11.5.4 shear equation
  matches Eq. 18.10.4.1's form.
- [[aci318-earthquake-general-and-ordinary-intermediate-frames]],
  [[aci318-special-moment-frames]] — column/beam provisions reused for wall piers
  and coupling beams.
- [[aci318-strength-reduction-factors]] — Cl 21.2.4 seismic shear φ.
- [[concrete-earthquake-structural-walls-detailing]] — the AS 3600 equivalent, for
  structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 18 Cl 18.10–18.11 (pp. 317–336),
  incl. Tables 18.10.3.1.2, 18.10.6.4(g), 18.10.6.5(b) and Figs. R18.10.2.3,
  R18.10.2.4, R18.10.3.1, R18.10.6.4a, R18.10.6.4c, R18.10.7a, R18.10.7b.
