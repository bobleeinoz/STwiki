---
title: ACI 318M-19 plain concrete design — walls, footings, pedestals, joints, strength
category: 0-standards
tags: [aci, plain-concrete, footings, pedestals, walls]
standards: [ACI 318M-19 Cl 14.1, ACI 318M-19 Cl 14.2, ACI 318M-19 Cl 14.3, ACI 318M-19 Cl 14.4, ACI 318M-19 Cl 14.5, ACI 318M-19 Cl 14.6]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 plain concrete design

> Scope: ACI 318M-19 Chapter 14 in full — when structural plain concrete may
> be used (including the restricted SDC D–F cases), minimum thicknesses,
> contraction/isolation joints, required strength, and the plain-concrete
> design strength equations for flexure, axial compression, combined action,
> shear and bearing. This is an **ACI 318M-19 page, kept separate from the AS
> 3600:2018 concept pages** elsewhere in `2-concrete` — see
> [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Chapter 14 covers plain concrete members in buildings and in
non-building structures such as arches, underground utility structures, gravity
walls and shielding walls (Cl 14.1.1). It does **not** govern cast-in-place piles
and piers embedded in ground (Cl 14.1.2 — the general building code does,
Cl R14.1.2). Strength and structural integrity come **solely** from member size,
concrete strength and other concrete properties — no ductility or reserve from
reinforcement — which is why the permitted uses are narrow (Cl R14.1.3).

## Detail

### Where plain concrete is allowed (Cl 14.1.3–14.1.5)

`[code]` Plain concrete is permitted only for: (a) members continuously supported
by soil or other structural members able to give continuous vertical support;
(b) members in which arch action provides compression under all load conditions;
(c) walls; (d) pedestals (Cl 14.1.3). In **SDC D, E or F** it is permitted only
for: (a) footings supporting cast-in-place reinforced concrete or reinforced
masonry walls, if reinforced longitudinally with at least **two continuous bars**
of at least No. 13 and total area ≥ `0.002 ×` the footing gross area, continuous
at corners and intersections; and (b) specified footings and foundation/basement
walls (≥ 190 mm thick, retaining ≤ 1.2 m of unbalanced fill) for detached one-
and two-family dwellings of up to three storeys with stud bearing walls
(Cl 14.1.4). Plain concrete is **not permitted for columns and pile caps**
(Cl 14.1.5) — `[derived]` because it lacks the ductility columns need and a random
crack in an unreinforced column would likely endanger stability (Cl R14.1.5).
Reinforced concrete pedestals fall under [[aci318-column-design]].

### General (Cl 14.2)

`[code]` Materials per Chapters 19–20 and Cl 20.6 (Cl 14.2.1). **Tension may not
be transmitted** through outside edges, construction joints, contraction joints or
isolation joints of an individual plain concrete element (Cl 14.2.2.1). Walls
must be braced against lateral translation (Cl 14.2.2.2) — `[derived]` the
provisions apply only to walls laterally supported to prevent relative
displacement top and bottom (Cl R14.2.2.2). Precast members are designed for all
conditions from fabrication to completion, and connected to a system capable of
resisting lateral forces (Cl 14.2.3).

### Design limits (Cl 14.3)

`[code]` **Bearing walls**: minimum thickness the greater of **140 mm** and 1/24
the lesser of unsupported length and height; exterior basement and foundation
walls **190 mm** (Table 14.3.1.1, Cl 14.3.1.1). **Footings**: thickness ≥ **200 mm**
(Cl 14.3.2.1); base area is set from *unfactored* forces/moments and permissible
soil pressure (Cl 14.3.2.2). **Pedestals**: ratio of unsupported height to average
least lateral dimension ≤ **3** (Cl 14.3.3.1; doesn't apply to portions embedded in
soil providing lateral restraint, Cl R14.3.3.1). **Joints**: contraction or
isolation joints must divide plain concrete members into flexurally discontinuous
elements sized to limit restraint stress from creep, shrinkage and temperature;
their number/location considers climate, materials, mixing/placing/curing,
degree of restraint, load stresses and construction technique
(Cl 14.3.4). `[derived]` In plain concrete, joints are the *only* means of
controlling restraint stress build-up — in reinforced concrete the steel does that
job (Cl R14.3.4.1).

### Required strength (Cl 14.4)

`[code]` Loads per Chapters 5–6 (Cl 14.4.1.1–14.4.1.2); **no flexural continuity
due to tension** is assumed between adjacent plain concrete elements (Cl 14.4.1.3).
Walls are designed for the eccentricity corresponding to the maximum moment that
can accompany the axial load, **but not less than 0.10h** (Cl 14.4.2.1). For
footings: circular/regular-polygon columns may be treated as square of equal area
(Cl 14.4.3.1.1); the `M_u` critical section follows Table 14.4.3.2.1 (same
locations as Table 13.2.7.1 — column/pedestal face, midway to a steel base-plate
edge, concrete wall face, midway centre-to-face of a masonry wall); one-way shear
critical sections lie **`h`** from those locations or from concentrated-load /
reaction-area faces (Cl 14.4.3.3), and two-way shear critical perimeters `b_o` are
minimum but not closer than **`h/2`** to those locations, load faces, or thickness
changes (Cl 14.4.3.4). `[derived]` These mirror the reinforced concrete critical
sections of Cl 22.6.4.1 but use `h` rather than `d`, since there is no steel
(Cl R14.4.3.4.1). See [[aci318-foundation-design]] for the reinforced-footing
equivalents.

### Design strength (Cl 14.5)

`[code]` `φM_n`, `φP_n`, `φV_n` and `φB_n` all `≥` their factored demands with
interaction considered; **a single φ** applies to all plain-concrete strength
conditions (Cl 14.5.1.1–14.5.1.2) — `[derived]` because flexural tension and
shear strength both rest on concrete tensile strength with no ductile reserve,
equal φ for moment and shear is appropriate (Cl R14.5.1.2; see
[[aci318-strength-reduction-factors]] — Table 21.2.1 gives φ = 0.60 for plain
concrete). Concrete tensile strength **may** be considered, provided joints relieve
restraint stress (Cl 14.5.1.3, Cl R14.5.1.3); flexural and axial strength use a
**linear stress–strain** relationship in tension and compression (Cl 14.5.1.4);
**no strength is assigned to reinforcement** (Cl 14.5.1.6); the whole cross-section
is used except for concrete cast against soil, where `h` is taken **50 mm less**
than specified (Cl 14.5.1.7). The effective horizontal wall length per vertical
concentrated load is the lesser of the centre-to-centre spacing and bearing width
plus four times the wall thickness, unless shown otherwise by analysis
(Cl 14.5.1.8).

`[code]` **Flexure** (Cl 14.5.2.1): `M_n` is the **lesser** of
`0.42λ√f'c S_m` (tension face, Eq. 14.5.2.1a) and `0.85f'c S_m` (compression
face, Eq. 14.5.2.1b), `S_m` = the corresponding elastic section modulus.
**Axial compression**: `P_n = 0.60 f'c A_g [1 − (ℓ_c/32h)²]` (Eq. 14.5.3.1)
— `[derived]` no effective-length factor modifies `ℓ_c`, the vertical distance
between supports, because that is conservative for pinned-support walls and
covers the range of braced/restrained end conditions in plain concrete
(Cl R14.5.3.1).

`[code]` **Combined flexure and axial compression** (Cl 14.5.4.1) — dimensions
satisfy both:

![[aci318-table-14.5.4.1-plain-concrete-flexure-axial-interaction.png]]
*Table 14.5.4.1 — tension face: `M_u/S_m − P_u/A_g ≤ 0.42φλ√f'c`; compression
face: `M_u/(φM_n) + P_u/(φP_n) ≤ 1.0` (ACI 318M-19).* For solid rectangular walls
with `M_u ≤ P_u(h/6)` (resultant within the middle third), `M_u` may be ignored
and `P_n = 0.45 f'c A_g [1 − (ℓ_c/32h)²]` (Eq. 14.5.4.2, Cl 14.5.4.2).

`[code]` **Shear** (Cl 14.5.5.1):

![[aci318-table-14.5.5.1-plain-concrete-nominal-shear.png]]
*Table 14.5.5.1 — one-way `V_n = 0.11λ√f'c b_w h`; two-way `V_n` the lesser of
`0.11(1 + 2/β)λ√f'c b_o h` and `0.22λ√f'c b_o h` (β = long/short side ratio of the
concentrated load or reaction area) (ACI 318M-19).* `[derived]` Plain-concrete
proportions are usually governed by tensile (flexural) rather than shear
strength, so shear rarely controls (Cl R14.5.5.1).

`[code]` **Bearing** (Cl 14.5.6.1) — identical to the reinforced-concrete frustum
rule of Cl 22.8.3.2 (see [[aci318-bearing-and-shear-friction]]):

![[aci318-table-14.5.6.1-plain-concrete-nominal-bearing.png]]
*Table 14.5.6.1 — `B_n` the lesser of `√(A₂/A₁)(0.85f'cA₁)` and `2(0.85f'cA₁)` where
the supporting surface is wider on all sides; otherwise `0.85f'cA₁` (ACI 318M-19).*

### Reinforcement detailing (Cl 14.6)

`[code]` At least **two No. 16 bars** around window, door and similarly sized
openings, extending at least **600 mm** beyond the opening corners or anchored to
develop `f_y` in tension at the corners (Cl 14.6.1).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-foundation-design]] — Chapter 13 reinforced footings and pile caps.
- [[aci318-wall-design]], [[aci318-column-design]] — reinforced walls and
  pedestals.
- [[aci318-strength-reduction-factors]] — φ = 0.60 for plain concrete.
- [[as3600-plain-pedestals-and-footings]] — the AS 3600 equivalent, for
  structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 14 Cl 14.1–14.6 (pp. 203–210),
  incl. Tables 14.3.1.1, 14.4.3.2.1, 14.5.4.1, 14.5.5.1, 14.5.6.1.
