---
title: ACI 318M-19 earthquake provisions for diaphragms, trusses, foundations and members not in the seismic-force-resisting system
category: 0-standards
tags: [aci, earthquake, seismic, diaphragms, collectors, foundations, piles, non-sfrs]
standards: [ACI 318M-19 Cl 18.12, ACI 318M-19 Cl 18.13, ACI 318M-19 Cl 18.14]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 earthquake provisions — diaphragms, foundations, non-SFRS members

> Scope: ACI 318M-19 Cl 18.12 (diaphragms, collectors and structural trusses),
> 18.13 (foundations — footings, mats, pile caps, grade beams, seismic ties, deep
> foundations) and 18.14 (members not designated as part of the seismic-force-
> resisting system). Ordinary-diaphragm design is on [[aci318-diaphragm-design]];
> ordinary foundations on [[aci318-foundation-design]]. This is an **ACI 318M-19
> page, kept separate from the AS 3600:2018 concept pages** elsewhere in
> `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Cl 18.12 applies to diaphragms and collectors that form part of the
seismic-force-resisting system in **SDC D, E, F** (and SDC C when Cl 18.12.11 applies
to precast diaphragms); Cl 18.12.12 to structural trusses in SDC D–F (Cl 18.12.1).
Cl 18.13 applies to foundations resisting or transferring earthquake forces; Cl 18.14
to members *not* designated as part of the system in SDC D–F, which must survive
the design displacement `δ_u` while carrying gravity load.

## Detail

### Diaphragms and collectors (Cl 18.12)

`[code]` Design forces come from the general building code (Cl 18.12.2.1); all
diaphragms and connections transfer force to collectors and vertical elements, and
axial-force elements used around openings follow the collector rules of Cl 18.12.7.6
and 18.12.7.7 (Cl 18.12.3). A **reinforced** cast-in-place **composite topping** on
precast may act as the diaphragm if the precast surface is clean, free of laitance
and intentionally roughened (Cl 18.12.4); a **noncomposite topping** must, acting
alone, resist the design earthquake forces (Cl 18.12.5). Minimum thickness:
**50 mm** for slabs and composite toppings, **65 mm** for noncomposite toppings on
precast (Cl 18.12.6).

`[code]` **Reinforcement** (Cl 18.12.7): minimum ratio per Cl 24.4; spacing ≤ 450 mm
each way (except post-tensioned slabs); welded wire shear reinforcement in toppings
has wires parallel to precast joints at ≥ 250 mm; shear steel is continuous and
uniformly distributed. Bonded tendons used for collector force, shear or flexural
tension are stressed to ≤ **420 MPa** under design earthquake force; unbonded-tendon
precompression may be used if a seismic load path is provided. All such steel is
developed/spliced for `f_y`; mechanical splices on Grade 420 steel between diaphragm
and vertical elements are **Type 2** (Grade 550/690 may not be mechanically spliced
there); collector steel average tensile stress over (a) the length from the collector
end to where transfer begins or (b) between two vertical elements ≤ `φf_y` with
`f_y ≤ 420 MPa`.

`[code]` **Collector confinement** (Cl 18.12.7.6): collector elements with
compressive stress above `0.2f'c` at any section get Cl 18.7.5.2(a)–(e)/18.7.5.3
transverse steel, with the Cl 18.7.5.3(a) limit set to **one-third** of the least
collector dimension; this may stop where stress falls below `0.15f'c` (limits
`0.5f'c` and `0.4f'c` instead if forces were amplified for overstrength):

![[aci318-table-18.12.7.6-transverse-reinforcement-collectors.png]]
*Table 18.12.7.6 — transverse reinforcement for collector elements: rectilinear
`A_sh/sb_c = 0.09f'c/f_yt`; spiral/circular `ρ_s` the greater of
`0.45(A_g/A_ch − 1)f'c/f_yt` and `0.12f'c/f_yt` (ACI 318M-19).* Splice and anchorage
zones of collector bars satisfy either (a) centre-to-centre spacing ≥ `3d_b` (not
under 40 mm) with clear cover ≥ `2.5d_b` (not under 50 mm), or (b) `A_v` ≥ the greater
of `0.062√f'c b_w s/f_yt` and `0.35b_w s/f_yt` (Cl 18.12.7.7).

`[code]` **Flexure** per Chapter 12 including openings (Cl 18.12.8.1 — see
[[aci318-diaphragm-design]]). **Shear** `V_n = A_cv(0.17λ√f'c + ρ_t f_y)` (Eq. 18.12.9.1,
same form as Cl 12.5.3.3) and `V_n ≤ 0.66√f'c A_cv`; for topping slabs `A_cv` uses the
topping thickness (noncomposite) or combined thickness (composite, `f'c` the lesser of
precast and topping). Above precast joints in topped diaphragms `V_n ≤ A_vf f_y μ`
(Eq. 18.12.9.3) with `μ = 1.0λ`, `A_vf` the shear-friction steel perpendicular to the
joints (≥ half uniformly distributed along the shear plane, distributed steel meeting
Cl 24.4.3.2 each direction), and `V_n` within the Cl 22.9.4.4 limits using only
topping thickness (Cl 18.12.9). Construction joints per Cl 26.5.6, roughened (Cl
18.12.10).

`[code]` **Precast diaphragms** not satisfying Cl 18.12.4 (including untopped) are
permitted only per ACI 550.5M, with connections and joint reinforcement tested per
ACI 550.4M and no extrapolation to larger construction tolerances than tested
(Cl 18.12.11). **Structural trusses** with compression above `0.2f'c` get transverse
steel per Cl 18.7.5.2/18.7.5.3/18.7.5.7 and Table 18.12.12.1 (the same four
expressions as Table 18.12.7.6, plus the rectilinear `0.3(A_g/A_ch − 1)f'c/f_yt`
branch); all continuous truss steel is developed/spliced for `f_y` (Cl 18.12.12).

### Foundations (Cl 18.13)

`[code]` Applies to foundations resisting earthquake forces or transferring them
between structure and ground; its pile, pier, caisson and slab-on-ground provisions
supplement the general criteria (Cl 18.13.1). **Footings, mats, pile caps** (SDC D–F,
Cl 18.13.2): column and wall longitudinal steel extends into the foundation and is
**fully developed in tension at the interface**; fixed-base columns have 90° hooks
near the bottom of the foundation turned toward the column centre; columns or wall
boundary elements with an edge within **half the footing depth** of a footing edge
have Cl 18.7.5.2–18.7.5.4 transverse steel below the footing top, extending an
`ℓ_d` (for `f_y`) of the longitudinal steel; where earthquake uplift acts, top flexural
steel (≥ Cl 7.6.1/9.6.1 minimum) resists it; plain concrete per Cl 14.1.4; pile caps
with **batter piles** resist the piles' full short-column compressive strength with
slenderness considered for unsupported portions.

`[code]` **Grade beams and slabs-on-ground** (Cl 18.13.3): in SDC D–F, grade beams and
mat beams taking flexure from SFRS columns follow Cl 18.6; in SDC C–F, a
slab-on-ground resisting in-plane earthquake forces from SFRS walls/columns is a
Cl 18.12 diaphragm and must be shown as such in the construction documents.
**Foundation seismic ties** (Cl 18.13.4): in SDC C–F, individual pile caps, piers or
caissons are interconnected orthogonally unless equivalent restraint is shown; in
SDC D–F, spread footings on Site Class E or F soil are tied. Tie design strength in
tension and compression ≥ `0.1S_DS ×` the greater factored dead + live load of the
pile cap/column, unless restraint comes from reinforced beams or slabs-on-ground, competent rock/hard soil/dense
granular confinement, or other approved means; grade-beam ties have continuous
developed longitudinal steel, smallest dimension ≥ clear column spacing/20 (not above
450 mm) and closed ties at ≤ the lesser of half the smallest cross-section dimension
and 300 mm.

`[code]` **Deep foundations** (Cl 18.13.5): piles/piers/caissons resisting tension
have continuous longitudinal steel over their length; minimum steel and transverse
confinement extend over the whole unsupported length in air, water or soil too weak
to restrain buckling; hoops, spirals and ties end in seismic hooks; in SDC D–F or Site
Class E/F, transverse steel per Cl 18.7.5.2/18.7.5.3 and Table 18.7.5.4 item (e) lies
within **seven member diameters** above and below interfaces between hard/stiff and
liquefiable/soft strata (exempting piles and foundation ties for one- and two-storey
stud bearing wall construction).

![[aci318-table-18.13.5.7.1-min-reinforcement-uncased-piles.png]]
*Table 18.13.5.7.1 — minimum reinforcement for uncased cast-in-place or augered piles
and piers by SDC/site class: longitudinal ratio 0.0025 (SDC C) or 0.005 (SDC D–F),
reinforced length the longest of a pile-length fraction, 3 m, 3 pile diameters and the
flexural length (`0.4M_cr > M_u`), a confinement zone at the cap (3 diameters, or 7
diameters for Site Class E/F) with closed ties/spirals ≥ 10 mm, and a remainder zone
at ≤ 16 longitudinal bar diameters (ACI 318M-19).*

`[code]` Metal-cased piles follow the uncased longitudinal/minimum-length rules with a
spiral-welded casing ≥ 2 mm and protected against soil/water effects (Cl 18.13.5.8);
concrete-filled pipe piles need top longitudinal steel ≥ `0.01A_g` extending at least
twice the cap embedment and not less than `ℓ_d` (Cl 18.13.5.9). **Precast piles**
(Cl 18.13.5.10): transverse length covers variation in tip elevation; SDC C
nonprestressed — longitudinal ratio 0.01, No. 10 closed ties (≤ 500 mm diameter) or
No. 13 (larger), spacing ≤ the lesser of `8d_b` and 150 mm within 3× least dimension
of the cap, ≤ 150 mm throughout; SDC D–F nonprestressed add the Table 18.13.5.7.1
rules; prestressed piles use spiral volumetric ratios `ρ_s ≥ 0.15f'c/f_yt` (SDC C,
upper 6 m) or `0.2f'c/f_yt` (SDC D–F ductile region of ≥ 10.5 m or to zero
curvature + 3 × least dimension), or the more detailed `P_u`-dependent forms
(`f_yt ≤ 690 MPa`), spacing ≤ the least of `0.2×` least dimension, `6×` strand
diameter and 150 mm; for SDC C–F the maximum factored axial load is `0.2f'cA_g`
(square) or `0.4f'cA_g` (circular/octagonal). **Pile anchorage** (Cl 18.13.6): tension
steel is detailed to transfer force into the cap; piles embed reinforcement an `ℓ_d`
(compression `ℓ_d` if in compression; uplift tension `ℓ_d` with no reduction for excess
steel) or use field-placed dowels; grouted/post-installed bars connecting precast
piles to caps in SDC D–F are shown by test to develop ≥ **1.25f_y**.

### Members not designated as part of the SFRS (Cl 18.14)

`[code]` Applies in SDC D–F. These members are checked for gravity load combinations
of Cl 5.3 including vertical ground motion acting with the design displacement
`δ_u` (Cl 18.14.2.1). **Cast-in-place beams, columns and joints**: if induced
moments/shears at `δ_u` don't exceed member strength, Cl 18.14.3.2 applies — beams
Cl 18.6.3.1 steel with transverse steel at ≤ `d/2` (hoops per Cl 18.7.5.2 at ≤ the
lesser of `6d_b` and 150 mm where axial force exceeds `A_g f'c/10`); columns Cl 18.7.4.1
and 18.7.6 with spiral/hoop steel full-length at ≤ the lesser of `6d_b` and 150 mm and
Cl 18.7.5.2(a)–(e) steel over `ℓ_o` from each joint (with half the Table 18.7.5.4
amount when gravity axial force exceeds `0.35P_o`); joints per Chapter 15. If the
induced actions exceed `φM_n`/`φV_n`, or aren't calculated, Cl 18.14.3.3 applies:
special moment frame materials/splices (Cl 18.2.5–18.2.8), beams per Cl 18.14.3.2(a)
and 18.6.5, columns per Cl 18.7.4–18.7.6, joints per Cl 18.4.4.1.
**Precast** members satisfy those plus full-height ties, Cl 4.10 integrity
reinforcement and bearing length ≥ 50 mm more than Cl 16.2.6 requires (Cl 18.14.4).

`[code]` **Slab-column connections** of two-way slabs without beams (Cl 18.14.5):
slab shear reinforcement (per Cl 8.7.6/8.7.7) at the Cl 22.6.4.1 critical section is
required where `Δ_x/h_sx ≥ 0.035 − 0.05v_uv/(φv_c)` (nonprestressed) or `≥ 0.040 −
0.05v_uv/(φv_c)` (unbonded post-tensioned with Cl 8.6.2.1 `f_pc`), using only
combinations including `E`, the greater `Δ_x/h_sx` of adjacent stories, and `V_p = 0`
in `v_c` for post-tensioned slabs; not required if `Δ_x/h_sx ≤ 0.005` (nonprestressed)
or `0.01` (post-tensioned) (Cl 18.14.5.2). Required shear steel gives
`v_s ≥ 0.29√f'c` and extends ≥ 4× slab thickness from the support face (Cl 18.14.5.3):

![[aci318-fig-r18.14.5.1-slab-column-drift-limit.png]]
*Fig. R18.14.5.1 — criteria of Cl 18.14.5.1: design story drift ratio `Δ_x/h_sx`
against `v_uv/φv_c`, below which slab shear reinforcement is not required (lower
line nonprestressed, upper line post-tensioned) (ACI 318M-19).* **Wall piers** not in
the system satisfy Cl 18.10.8, with design shear permitted as `Ω_o ×` the shear induced
at `δ_u` where the general code accounts for overstrength (Cl 18.14.6).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-diaphragm-design]], [[aci318-foundation-design]] — the ordinary
  chapters these provisions tighten.
- [[aci318-special-moment-frames]], [[aci318-special-structural-walls]] — source of
  the column/wall-pier confinement reused here.
- [[aci318-earthquake-general-and-ordinary-intermediate-frames]] — SDC routing.
- [[as3600-diaphragm-design]], [[as3600-earthquake-design-basis]] — the AS 3600
  equivalents, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 18 Cl 18.12–18.14 (pp. 336–353),
  incl. Tables 18.12.7.6, 18.12.12.1, 18.13.5.7.1 and Fig. R18.14.5.1.
