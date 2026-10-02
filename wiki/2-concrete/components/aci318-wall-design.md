---
title: ACI 318M-19 wall design — thickness, axial/flexure, in-plane shear, reinforcement and slender wall method
category: 2-concrete
tags: [aci, walls, shear-walls, slender-walls, reinforcement-detailing]
standards: [ACI 318M-19 Cl 11.1, ACI 318M-19 Cl 11.2, ACI 318M-19 Cl 11.3, ACI 318M-19 Cl 11.4, ACI 318M-19 Cl 11.5, ACI 318M-19 Cl 11.6, ACI 318M-19 Cl 11.7, ACI 318M-19 Cl 11.8]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 wall design

> Scope: ACI 318M-19 Chapter 11 in full — scope and routing to other chapters,
> load distribution and intersecting elements, minimum thickness, required and
> design strength (the simplified out-of-plane axial method, in-plane and
> out-of-plane shear), reinforcement limits and detailing, and the alternative
> out-of-plane slender-wall analysis method. This is an **ACI 318M-19 page,
> kept separate from the AS 3600:2018 concept pages** elsewhere in
> `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Chapter 11 covers nonprestressed and prestressed walls — cast-in-place,
precast in-plant, and precast on-site including tilt-up (Cl 11.1.1). It
**excludes** special structural walls (Chapter 18, Cl 11.1.2), plain concrete
walls (Chapter 14, Cl 11.1.3), cantilever retaining walls (Chapter 13,
Cl 11.1.4) and walls acting as grade beams (Cl 13.3.5, Cl 11.1.5). Cast-in-place
walls with insulating forms are permitted for one- or two-storey buildings
(Cl 11.1.6; guidance in ACI 506R/PCA 100 per Cl R11.1.6). `[derived]` The Code
treats "structural wall" as synonymous with "shear wall"; ordinary (non-seismic)
in-plane shear provisions live here, while seismic walls move to Chapter 18
(Cl R11.1.2).

## Detail

### General (Cl 11.2)

`[code]` Concrete per Chapter 19, reinforcement per Chapter 20, embedments per
Cl 20.6; precast wall connections per Cl 16.2, wall-to-foundation connections per
Cl 16.3 (Cl 11.2.1–11.2.2). **Load distribution**: unless shown otherwise by
analysis, the horizontal length of wall effective for each concentrated load is
the lesser of the centre-to-centre load spacing and the bearing width plus
**four wall thicknesses**, and does not extend past vertical wall joints unless
force transfer across the joint is provided (Cl 11.2.3.1). Walls must be
anchored to intersecting floors/roofs, columns, pilasters, buttresses or
intersecting walls, and to footings (Cl 11.2.4.1). For cast-in-place walls with
`P_u > 0.2 f'c A_g`, the wall portion within the floor-system thickness needs
specified strength at least `0.8 f'c` of the wall (Cl 11.2.4.2) —
`[derived]` reflecting less confinement at floor–wall joints than at
floor–column joints under gravity load (Cl R11.2.4.2).

### Minimum thickness (Cl 11.3)

![[aci318-table-11.3.1.1-min-wall-thickness.png]]
*Table 11.3.1.1 — minimum wall thickness `h`: bearing walls the greater of
100 mm and 1/25 the lesser of unsupported length and height; nonbearing walls
the greater of 100 mm and 1/30 of the same; exterior basement and foundation
walls 190 mm; the bearing and basement/foundation rows apply only to walls
designed by the simplified method of Cl 11.5.3 (ACI 318M-19).* Thinner walls are
permitted if strength and stability are shown by structural analysis
(Cl 11.3.1.1); the minimum doesn't apply to bearing and basement/foundation
walls designed by Cl 11.5.2 or analysed by Cl 11.8 (Cl R11.3.1.1).

### Required strength (Cl 11.4)

`[code]` Loads per Chapters 5–6 (Cl 11.4.1.1–11.4.1.2); slenderness per
Cl 6.6.4, 6.7 or 6.8, or alternatively the Cl 11.8 out-of-plane method for walls
that qualify (Cl 11.4.1.3 — see
[[aci318-column-slenderness-and-moment-magnification]] and
[[aci318-second-order-and-advanced-analysis]]). Walls are designed for eccentric
axial loads and all lateral loads (Cl 11.4.1.4), for the maximum `M_u` that can
accompany `P_u` in each combination, with `P_u ≤ φP_n,max` (`P_n,max` per
Cl 22.4.2.1 and `φ` the **compression-controlled** value of Cl 21.2.2), and with
`M_u` magnified for slenderness (Cl 11.4.2.1). Both in-plane and out-of-plane
`V_u` are designed for (Cl 11.4.3.1):

![[aci318-fig-r11.4.1.3-forces-acting-on-wall.png]]
*Fig. R11.4.1.3 — forces typically acting on a wall: in-plane shear and
moment, out-of-plane shear and moment, axial force and self-weight
(ACI 318M-19).*

### Design strength (Cl 11.5)

`[code]` `φP_n ≥ P_u`, `φM_n ≥ M_u`, `φV_n ≥ V_u` with axial–moment interaction
considered and φ per Cl 21.2 (Cl 11.5.1). For **bearing walls**, `P_n` and `M_n`
(in- or out-of-plane) come from Cl 22.4 (see
[[aci318-sectional-strength-flexure-and-axial]]); alternatively axial load with
out-of-plane flexure may use the simplified method below (Cl 11.5.2.1).
**Nonbearing walls**: `M_n` per Cl 22.3 (Cl 11.5.2.2).

`[code]` **Simplified out-of-plane method** (Cl 11.5.3): valid only if the
resultant of all factored loads lies within the **middle third** of the
thickness of a solid rectangular wall (Cl 11.5.3.1; Cl R11.5.3.1 — solid
rectangular sections only):

**P_n = 0.55 f'c A_g [1 − (kℓ_c/32h)²]**  (Eq. 11.5.3.1)

with `k` from Table 11.5.3.2 — **0.8** for walls braced top and bottom against
translation and restrained against rotation at one or both ends; **1.0** if
braced against translation but unrestrained against rotation at both ends;
**2.0** if not braced against lateral translation (Cl 11.5.3.2). `P_n` is
reduced by the compression-controlled `φ` (Cl 11.5.3.3) and wall steel must meet
Cl 11.6 (Cl 11.5.3.4).

`[code]` **In-plane shear** (Cl 11.5.4): `V_n` at any horizontal section ≤
`0.66√f'c A_cv` (Cl 11.5.4.2 — reduced from 0.83 in ACI 318M-14 because the
effective shear area is now `hℓ_w` rather than `hd`, Cl R11.5.4.2), and

**V_n = (α_c λ √f'c + ρ_t f_yt) A_cv**  (Eq. 11.5.4.3)

with `α_c = 0.25` for `h_w/ℓ_w ≤ 1.5`, `0.17` for `h_w/ℓ_w ≥ 2.0`, varying
linearly between. `[derived]` This now has the same form as the seismic wall
shear equation of Cl 18.10.4.1 (Cl R11.5.4.3). For walls with **net axial
tension**: `α_c = 0.17(1 + N_u/(3.45A_g)) ≥ 0` (Eq. 11.5.4.4, `N_u` negative
for tension) — the concrete shear contribution shrinks and may vanish, leaving
the transverse steel to carry most or all the shear (Cl R11.5.4.4). Walls with
`h_w/ℓ_w < 2` may alternatively use the strut-and-tie method of Chapter 23 (see
[[aci318-strut-and-tie-method]]); reinforcement limits of Cl 11.6, 11.7.2 and
11.7.3 apply regardless (Cl 11.5.4.1). **Out-of-plane shear**: Cl 22.5 (Cl
11.5.5.1 — see [[aci318-one-way-shear-strength]]).

### Reinforcement limits (Cl 11.6)

`[code]` If in-plane `V_u ≤ 0.04φα_cλ√f'c A_cv`, minimum `ρ_ℓ` and `ρ_t` follow:

![[aci318-table-11.6.1-min-wall-reinforcement.png]]
*Table 11.6.1 — minimum wall reinforcement ratios (cast-in-place deformed bars
≤ No. 16 with `f_y ≥ 420 MPa`: `ρ_ℓ = 0.0012`, `ρ_t = 0.0020`; lower-grade or
larger bars: 0.0015/0.0025; welded-wire reinforcement ≤ MW200: 0.0012/0.0020;
precast: 0.0010/0.0010) (ACI 318M-19).* Prestressed walls with average effective
compression ≥ 1.6 MPa are exempt from minimum `ρ_ℓ`; one-way precast prestressed
walls ≤ 3.6 m wide not mechanically connected for transverse restraint are exempt
from the minimum in the direction normal to flexural steel. The limits may be
waived if strength and stability are shown by analysis (Cl 11.6.1).

`[code]` If in-plane `V_u > 0.04φα_cλ√f'c A_cv`: `ρ_ℓ ≥ max[0.0025 +
0.5(2.5 − h_w/ℓ_w)(ρ_t − 0.0025), 0.0025]` (Eq. 11.6.2, need not exceed the `ρ_t`
required for strength) and `ρ_t ≥ 0.0025` (Cl 11.6.2). `[derived]` The `ρ_ℓ`
expression recognises that for squat monotonically loaded walls horizontal steel
is less effective for shear than vertical steel (Cl R11.6.2).

### Reinforcement detailing (Cl 11.7)

`[code]` Cover per Cl 20.5.1, development per Cl 25.4, splices per Cl 25.5
(Cl 11.7.1). Maximum **longitudinal** bar spacing in cast-in-place walls: lesser of
`3h` and 450 mm, and `ℓ_w/3` if shear reinforcement is required for in-plane
strength (Cl 11.7.2.1); precast walls: lesser of `5h` and 450 mm (exterior) or
750 mm (interior), and for in-plane shear steel the smallest of `3h`, 450 mm and
`ℓ/3` (Cl 11.7.2.2). **Transverse** spacing: cast-in-place lesser of `3h` and
450 mm, and `ℓ_w/5` if in-plane shear steel is required (Cl 11.7.3.1); precast
as above with `ℓ_w/5` (Cl 11.7.3.2). Walls thicker than 250 mm (except
single-storey basement and cantilever retaining walls) need distributed
reinforcement in at least **two layers**, one near each face (Cl 11.7.2.3);
flexural tension steel is well distributed and close to the tension face
(Cl 11.7.2.4). Longitudinal compression steel with `A_st > 0.01A_g` is
laterally supported by ties (Cl 11.7.4.1). Around window/door-size openings,
add at least two No. 16 bars (two-layer walls) or one No. 16 bar (single-layer
walls), developed for `f_y` at the corners (Cl 11.7.5.1).

### Alternative method for out-of-plane slender wall analysis (Cl 11.8)

`[code]` Permitted for walls with: constant cross-section over the height;
tension-controlled for out-of-plane moment; `φM_n ≥ M_cr` (using `f_r` of
Cl 19.2.3); `P_u` at midheight ≤ `0.06f'c A_g`; and calculated service-load
out-of-plane deflection `Δ_s` (including P-Δ) ≤ `ℓ_c/150` (Cl 11.8.1.1). The
wall is modelled as simply supported, axially loaded, under uniform out-of-plane
load with maximum moment and deflection at midheight (Cl 11.8.2.1); concentrated
gravity loads spread over the bearing width plus a width each side increasing at
2 vertical : 1 horizontal, limited by load spacing and panel edges (Cl 11.8.2.2).

`[code]` Midheight `M_u` includes deflection effects, by iteration
`M_u = M_ua + P_u Δ_u` with
`Δ_u = 5 M_u ℓ_c² / ((0.75) 48 E_c I_cr)` (Eq. 11.8.3.1a/b), where
`I_cr = (E_s/E_c)(A_s + P_u h/(2 f_y d))(d − c)² + ℓ_w c³/3`
(Eq. 11.8.3.1c, `E_s/E_c ≥ 6`), or directly:

**M_u = M_ua / (1 − 5P_uℓ_c²/((0.75)48 E_c I_cr))**  (Eq. 11.8.3.1d)

`[code]` Service-load deflection `Δ_s` follows Table 11.8.4.1, with `M_a`
(including P_sΔ_s effects) found by iteration, `M_a = M_sa + P_sΔ_s`
(Cl 11.8.4.1–11.8.4.2), and `Δ_cr`, `Δ_n` from `5Mℓ_c²/(48E_cI)` using `I_g` and
`I_cr` respectively (Cl 11.8.4.3):

![[aci318-table-11.8.4.1-calculation-of-delta-s.png]]
*Table 11.8.4.1 — `Δ_s = (M_a/M_cr)Δ_cr` for `M_a ≤ (2/3)M_cr`; otherwise
`Δ_s = (2/3)Δ_cr + [(M_a − (2/3)M_cr)/(M_n − (2/3)M_cr)](Δ_n − (2/3)Δ_cr)`
(ACI 318M-19).*

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-sectional-strength-flexure-and-axial]] — Cl 22.4, the general
  axial–flexure basis for bearing walls.
- [[aci318-one-way-shear-strength]] — Cl 22.5 out-of-plane shear.
- [[aci318-strut-and-tie-method]] — the alternative for squat walls.
- [[aci318-column-slenderness-and-moment-magnification]],
  [[aci318-second-order-and-advanced-analysis]] — slenderness effects.
- [[concrete-wall-design-basis-and-classification]],
  [[concrete-wall-simplified-axial-design]], [[concrete-wall-in-plane-shear]],
  [[concrete-wall-reinforcement-requirements]] — the AS 3600 equivalents, for
  structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 11 Cl 11.1–11.8 (pp. 165–174),
  incl. Tables 11.3.1.1, 11.5.3.2, 11.6.1, 11.8.4.1 and Fig. R11.4.1.3.
