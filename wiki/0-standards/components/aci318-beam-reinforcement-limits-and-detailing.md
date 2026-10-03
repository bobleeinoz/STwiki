---
title: ACI 318M-19 beam reinforcement limits and detailing — minimum steel, termination, torsion, stirrups, integrity
category: 0-standards
tags: [aci, beams, minimum-reinforcement, detailing, stirrups, structural-integrity]
standards: [ACI 318M-19 Cl 9.6, ACI 318M-19 Cl 9.7]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 beam reinforcement limits and detailing

> Scope: ACI 318M-19 Cl 9.6 (minimum flexural, shear and torsional
> reinforcement) and Cl 9.7 (cover/development/splice routing, bar spacing and
> skin reinforcement, flexural bar development and termination, prestressed
> detailing, longitudinal and transverse torsional steel, stirrup spacing,
> compression-bar support, structural integrity reinforcement). This is an
> **ACI 318M-19 page, kept separate from the AS 3600:2018 concept pages**
> elsewhere in `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Cl 9.6 sets minimum steel so a beam doesn't fail suddenly at first
cracking (flexure or torsion) or at first inclined cracking (shear); Cl 9.7
gives the arrangement rules. Anything that depends on bar development, splices,
hooks or tie/stirrup geometry is delegated to Chapter 25 (not yet ingested on
this wiki) and spacing/crack-control to Cl 24.3 (see
[[aci318-serviceability-deflection-and-cracking]]).

## Detail

### Minimum flexural reinforcement (Cl 9.6.1–9.6.2)

`[code]` **Nonprestressed**: provide `A_s,min` at every section where tension
steel is required by analysis (Cl 9.6.1.1), taken as the **larger** of
`0.25√f'c b_w d / f_y` and `1.4 b_w d / f_y` (`f_y` ≤ 550 MPa; for a statically
determinate beam with the flange in tension `b_w` is the smaller of `b_f` and
`2b_w`) (Cl 9.6.1.2). It need not be met if the steel provided at every section
is at least **one-third more** than analysis requires (Cl 9.6.1.3). `[derived]`
The purpose is flexural strength comfortably above the cracking strength so the
beam can sustain load after cracking with visible warning; a tension flange
roughly doubles the steel needed to match the uncracked section's strength,
which is why the flange-in-tension rule exists, notably for cantilevers and
other statically determinate beams that cannot redistribute (Cl R9.6.1.1,
R9.6.1.2).

`[code]` **Prestressed, bonded**: `A_s + A_ps` must develop a factored load of
at least **1.2 × the cracking load** (based on `f_r`, Cl 19.2.3) (Cl 9.6.2.1),
waived if both flexural and shear design strength are at least twice the
required strength (Cl 9.6.2.2). **Unbonded tendons**: bonded deformed
longitudinal reinforcement `A_s,min = 0.004 A_ct` (`A_ct` = area between the
tension face and the gross-section centroid) (Cl 9.6.2.3) — `[derived]` to
ensure true flexural behaviour at ultimate rather than tied-arch behaviour and
to control crack width/spacing once tension exceeds the modulus of rupture
(Cl R9.6.2.3).

### Minimum shear reinforcement (Cl 9.6.3)

`[code]` **Nonprestressed**: `A_v,min` wherever `V_u > 0.083 φ λ √f'c b_w d`,
except the cases in Table 9.6.3.1, where it is only needed when `V_u > φV_c`
(Cl 9.6.3.1):

![[aci318-table-9.6.3.1-cases-avmin-not-required.png]]
*Table 9.6.3.1 — cases where `A_v,min` is not required if `V_u ≤ φV_c`: shallow
beams (`h ≤ 250 mm`), beams integral with a slab (`h ≤ max(2.5t_f, 0.5b_w)` and
`h ≤ 600 mm`), steel-fibre-reinforced normalweight beams (`h ≤ 600 mm`,
`f'c ≤ 40 MPa`, `V_u ≤ 0.17φ√f'c b_w d`), and one-way joists per Cl 9.8
(ACI 318M-19).* **Prestressed**: `A_v,min` wherever `V_u > 0.5 φ V_c` with the
same exceptions (Cl 9.6.3.2). Testing that demonstrates the required `M_n` and
`V_n` (simulating differential settlement, creep, shrinkage, temperature) can
waive both (Cl 9.6.3.3).

`[code]` Where shear steel is required and torsion can be neglected, `A_v,min/s`
is:

![[aci318-table-9.6.3.4-required-avmin.png]]
*Table 9.6.3.4 — required `A_v,min/s`: for nonprestressed beams and prestressed
beams with `A_ps f_se < 0.4(A_ps f_pu + A_s f_y)`, the greater of
`0.062√f'c b_w/f_yt` and `0.35 b_w/f_yt`; for heavily prestressed beams
(`A_ps f_se ≥ 0.4(...)`), the lesser of that same greater-of expression and
`A_ps f_pu /(80 f_yt d) · √(d/b_w)` (ACI 318M-19).* `[derived]` The `√f'c`
term makes minimum shear steel grow with concrete strength, because tests show
the sudden-failure risk at inclined cracking increases for higher-strength
concrete (Cl R9.6.3.4).

### Minimum torsional reinforcement (Cl 9.6.4)

`[code]` Required wherever `T_u ≥ φT_th` (Cl 9.6.4.1). Minimum transverse steel
`(A_v + 2A_t)_min/s` is the greater of `0.062√f'c b_w/f_yt` and `0.35 b_w/f_yt`
(Cl 9.6.4.2). Minimum longitudinal steel `A_ℓ,min` is the **lesser** of
`0.42√f'c A_cp/f_y − (A_t/s) p_h (f_yt/f_y)` and
`0.42√f'c A_cp/f_y − (0.175 b_w/f_yt) p_h (f_yt/f_y)` (Cl 9.6.4.3) —
`[derived]` shear lowers the torsional cracking moment, so torsion steel can be
reduced when shear is also present (Cl R9.6.4.3). `A_v` is the area of **two**
stirrup legs whereas `A_t` is **one** leg (Cl R9.6.4.2).

### General detailing and spacing (Cl 9.7.1–9.7.2)

`[code]` Cover per Cl 20.5.1; development per Cl 25.4; splices per Cl 25.5;
bundled bars per Cl 25.6 (Cl 9.7.1.1–9.7.1.5). For longitudinal bars with
`f_y ≥ 550 MPa`, transverse reinforcement along development and lap lengths must
give `K_tr ≥ 0.5d_b` (Cl 9.7.1.4). Minimum bar spacing per Cl 25.2; maximum
spacing of bonded bars nearest the tension face per Cl 24.3 for nonprestressed
and Class C prestressed beams (Cl 9.7.2.1–9.7.2.2).

`[code]` **Skin reinforcement** (Cl 9.7.2.3): nonprestressed and Class C
prestressed beams with `h > 900 mm` need longitudinal skin reinforcement
uniformly distributed on both side faces for a distance `h/2` from the tension
face, at spacing `≤ s` from Cl 24.3.2 (with `c_c` measured from the skin bars
to the side face); it may be counted in strength calculations if a strain
compatibility analysis is done.

![[aci318-fig-r9.7.2.3-skin-reinforcement.png]]
*Fig. R9.7.2.3 — skin reinforcement for beams and joists with `h > 900 mm`
(ACI 318M-19).*

### Flexural reinforcement in nonprestressed beams (Cl 9.7.3)

`[code]` The calculated bar force at every section must be **developed on each
side** of that section (Cl 9.7.3.1). Critical locations are points of maximum
stress and points where terminated/bent tension bars are no longer required for
flexure (Cl 9.7.3.2). Bars extend past the point no longer needed for flexure
by at least the **greater of `d` and `12d_b`** (except at simple supports and
cantilever free ends) (Cl 9.7.3.3); continuing tension bars must have embedment
`ℓ_d` beyond that point (Cl 9.7.3.4):

![[aci318-fig-r9.7.3.2-development-flexural-reinforcement-continuous-beam.png]]
*Fig. R9.7.3.2 — development of flexural reinforcement in a typical continuous
beam: bar cutoffs, points of inflection (P.I.), `x`/`c` critical sections,
and the `d`/`12d_b`/`ℓ_n/16` extension requirements (ACI 318M-19).*

`[code]` Flexural tension steel may **not** be terminated in a tension zone
unless one of: (a) `V_u ≤ (2/3)φV_n` at the cutoff; (b) for No. 36 bars and
smaller, continuing steel provides double the area required for flexure at the
cutoff **and** `V_u ≤ (3/4)φV_n`; or (c) stirrup/hoop area in excess of that
needed for shear and torsion is provided over `3d/4` from the cutoff, at least
`0.41 b_w s/f_yt` with `s ≤ d/(8β_b)` (Cl 9.7.3.5). `[derived]` Cutting a bar
in a tension zone lowers shear strength and ductility because flexural cracks
open early wherever steel stops (Cl R9.7.3.5). Adequate anchorage is also
required where bar stress isn't proportional to moment (sloped/stepped/tapered
beams, or tension bars not parallel to the compression face) (Cl 9.7.3.6); bars
may be developed by bending across the web to the opposite face (Cl 9.7.3.7).

`[code]` **Termination at supports** (Cl 9.7.3.8): at simple supports, at least
**one-third** of the maximum positive-moment steel extends along the bottom into
the support at least 150 mm (precast: to the centre of bearing); at other
supports at least **one-quarter** extends ≥ 150 mm, and develops `f_y` at the
support face if the beam is part of the primary lateral-load-resisting system.
At simple supports and points of inflection, positive-moment bar diameter is
limited so `ℓ_d ≤ 1.3M_n/V_u + ℓ_a` (end confined by a compressive reaction) or
`ℓ_d ≤ M_n/V_u + ℓ_a` (not confined) — waived if the bar ends beyond the
support centreline in a standard hook or equivalent mechanical anchorage. At
least **one-third** of the negative-moment steel at a support extends past the
inflection point by at least the greatest of `d`, `12d_b` and `ℓ_n/16`.

### Prestressed beams (Cl 9.7.4)

`[code]` External tendons must keep the specified eccentricity through the full
range of anticipated deflection (Cl 9.7.4.1); nonprestressed steel needed for
flexural strength follows Cl 9.7.3 (Cl 9.7.4.2); post-tensioning anchorage zones
and anchorages/couplers follow Cl 25.9 and 25.8 (Cl 9.7.4.3). Deformed steel
required for unbonded-tendon beams (Cl 9.6.2.3) extends at least `ℓ_n/3` and is
centred in positive-moment areas, and at least `ℓ_n/6` each side of the support
face in negative-moment areas (Cl 9.7.4.4).

### Torsional reinforcement detailing (Cl 9.7.5, 9.7.6.3)

`[code]` **Longitudinal** torsional steel is distributed round the perimeter of
closed stirrups (or hoops) at spacing ≤ 300 mm, inside the stirrup, with at
least one bar in each corner; its diameter is at least `0.042 ×` the transverse
spacing but not under 10 mm; it extends at least `(b_t + d)` beyond the point
required by analysis and is developed at the support face at both ends
(Cl 9.7.5.1–9.7.5.4). **Transverse** torsional steel is closed stirrups or hoops
(Cl 9.7.6.3.1), extending `(b_t + d)` beyond the required point
(Cl 9.7.6.3.2), at spacing ≤ the lesser of `p_h/8` and 300 mm (Cl 9.7.6.3.3); in
hollow sections its centreline sits at least `0.5A_oh/p_h` from the inside face
of the wall (Cl 9.7.6.3.4). `[derived]` The longer `(b_t + d)` extension (vs `d`
for shear/flexure) reflects the helical form of torsional diagonal cracks
(Cl R9.7.5.3, R9.7.6.3.2). Closed stirrups are required because torsional cracks
can form on every face (Cl R9.7.6.3.1).

### Shear reinforcement detailing (Cl 9.7.6.1–9.7.6.2)

`[code]` Where required, shear reinforcement is stirrups, hoops or
longitudinal bent bars (Cl 9.7.6.2.1); details per Cl 25.7, with the most
restrictive requirement governing (Cl 9.7.6.1). Maximum leg spacing:

![[aci318-table-9.7.6.2.2-max-spacing-shear-legs-beams.png]]
*Table 9.7.6.2.2 — maximum spacing of shear reinforcement legs along the member
length and across its width: for `V_s ≤ 0.33√f'c b_w d`, the lesser of
(`d/2` along / `d` across, nonprestressed; `3h/4` / `3h/2`, prestressed) and
600 mm; for `V_s > 0.33√f'c b_w d`, half those values and 300 mm (ACI
318M-19).* `[derived]` Reduced leg spacing across the width gives more uniform
transfer of diagonal compression through the web; tests on wide members with
widely spaced legs show the nominal shear capacity isn't always achieved
(Cl R9.7.6.2.2). Inclined stirrups and bent bars must be spaced so every 45°
line extending `d/2` toward the reaction from mid-depth to the longitudinal
tension steel crosses at least one line of shear steel (Cl 9.7.6.2.3); bent
longitudinal bars extending into tension continue with the longitudinal steel,
and into compression anchor `d/2` beyond mid-depth (Cl 9.7.6.2.4). Where a beam
frames into the side of a supporting beam, extra **hanger reinforcement** is
needed to transfer shear to the top of the supporting beam (Cl R9.7.6.2.1):

![[aci318-fig-r9.7.6.2.1-hanger-reinforcement.png]]
*Fig. R9.7.6.2.1 — hanger reinforcement for shear transfer to a supported beam
(ACI 318M-19).*

### Lateral support of compression reinforcement (Cl 9.7.6.4)

`[code]` Transverse steel is required throughout the length where longitudinal
compression steel is required, as closed stirrups or hoops at least No. 10
(for longitudinal bars up to No. 32) or No. 13 (for No. 36 and larger, and
bundled bars), spaced at most the least of `16d_b` (longitudinal), `48d_b`
(transverse) and the least beam dimension, with every corner and alternate
compression bar enclosed by a corner of included angle ≤ 135° and no bar more
than 150 mm clear from such an enclosed bar (Cl 9.7.6.4.1–9.7.6.4.4).

### Structural integrity reinforcement (Cl 9.7.7)

`[code]` In cast-in-place beams, **perimeter beams** need: at least one-quarter
of the maximum positive-moment steel (not less than two bars/strands) continuous;
at least one-sixth of the negative-moment steel at the support (not less than two
bars/strands) continuous; and that steel enclosed by closed stirrups or hoops
along the clear span (Cl 9.7.7.1). **Other beams** need either the one-quarter
positive-moment steel (≥ 2 bars) continuous or closed stirrups/hoops enclosing
the longitudinal steel along the span (Cl 9.7.7.2). Integrity steel passes
through the column's longitudinal-reinforcement region (Cl 9.7.7.3), anchors to
develop `f_y` at the face of noncontinuous supports (Cl 9.7.7.4), and is spliced
near the support (positive) or near midspan (negative) using mechanical/welded
splices or Class B lap splices (Cl 9.7.7.5–9.7.7.6). `[derived]` The aim is a
continuous tie around the structure — not a constant-size bar all round the
perimeter — so a damaged support leaves localised damage rather than collapse
(Cl R9.7.7.1); see also [[aci318-structural-system-requirements]] (Table 4.10.2.1).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-beam-design-basis-and-strength]] — Cl 9.1–9.5.
- [[aci318-joists-and-deep-beams]] — Cl 9.8–9.9.
- [[aci318-torsional-strength]] — the Chapter 22 torsion model these rules
  reinforce.
- [[as3600-beam-detailing]] — the AS 3600 equivalent, for structural
  comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 9 Cl 9.6–9.7 (pp. 135–150),
  incl. Tables 9.6.3.1, 9.6.3.4, 9.7.6.2.2 and Figs. R9.7.2.3, R9.7.3.2,
  R9.7.6.2.1.
