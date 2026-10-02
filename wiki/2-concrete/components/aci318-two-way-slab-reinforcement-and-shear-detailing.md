---
title: ACI 318M-19 two-way slab reinforcement and shear detailing — minimum steel, bar extensions, stirrups, headed studs, joists
category: 2-concrete
tags: [aci, two-way-slab, reinforcement-detailing, punching-shear, shear-reinforcement, joist-slab, structural-integrity]
standards: [ACI 318M-19 Cl 8.5, ACI 318M-19 Cl 8.6, ACI 318M-19 Cl 8.7, ACI 318M-19 Cl 8.8, ACI 318M-19 Cl 8.9]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 two-way slab reinforcement and shear detailing

> Scope: ACI 318M-19 Cl 8.5–8.9 — design strength basis, openings in slab
> systems, minimum flexural reinforcement (nonprestressed and prestressed,
> incl. the punching-shear-triggered `A_s,min` of Cl 8.6.1.2), reinforcement
> detailing (spacing, corner restraint, bar termination/extensions,
> structural integrity), shear reinforcement (stirrups and headed studs),
> nonprestressed two-way joist systems, and lift-slab construction. Scope,
> thickness and factored-moment-transfer provisions (Cl 8.1–8.4) are covered
> on [[aci318-two-way-slab-design-basis]]. This is an **ACI 318M-19 page,
> kept separate from the AS 3600:2018 concept pages** elsewhere in
> `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Design strength must satisfy `φS_n ≥ U` for: `M_n ≥ M_u` at every
section each direction; `M_n ≥ γ_f M_sc` within `b_slab`; `V_n ≥ V_u` for
one-way shear each direction; and `v_n ≥ v_u` for two-way shear at the
Cl 8.4.4.1 critical sections (Cl 8.5.1.1). `[derived]` The Chapter 8-specific
content in this page is mostly about **where and how much steel** to put —
minimum areas driven by punching-shear ductility concerns (Cl 8.6), bar
extension/termination geometry calibrated against where punching-shear
cracks actually form (Cl 8.7.4), and the two shear-reinforcement systems
(stirrups, headed studs) that let a slab exceed the bare-concrete punching
capacity of [[aci318-two-way-shear-strength]].

## Detail

### Design strength and openings (Cl 8.5)

`[code]` `M_n` per Cl 22.3 ([[aci318-sectional-strength-flexure-and-axial]]).
For nonprestressed slabs with a drop panel, the drop panel's thickness below
the slab counted toward `M_n` is capped at 1/4 of the distance from the drop
panel edge to the column/capital face (Cl 8.5.2.2) — `[derived]` this
prevents an over-generous effective depth assumption where the drop panel
tapers or is disproportionately thin relative to its extent. External
tendons are unbonded for `M_n` purposes unless effectively bonded along
their full length (Cl 8.5.2.3, mirrors Cl 7.5.2.2).

`[code]` Shear strength is the **more severe** of one-way shear (`V_n` per
Cl 22.5, critical section spanning the full slab width — see
[[aci318-one-way-shear-strength]]) and two-way shear (`v_n` per Cl 22.6 —
see [[aci318-two-way-shear-strength]]) (Cl 8.5.3.1–8.5.3.1.2). Composite
slabs additionally check horizontal shear `V_nh` per Cl 16.4 (Cl 8.5.3.2).

`[code]` **Openings**: permitted at any size if analysis shows all strength
and serviceability (incl. deflection) requirements are satisfied
(Cl 8.5.4.1). As an alternative, for slab systems **without beams**
(Cl 8.5.4.2): any size within the area common to intersecting middle strips,
provided total panel reinforcement matches the no-opening case; ≤1/8 of
column-strip width in either span at two intersecting column strips, with
interrupted reinforcement replaced at the opening sides; ≤1/4 of either
strip's reinforcement at a column-strip/middle-strip intersection, similarly
replaced; and openings within `4h` of a column/load/reaction periphery must
satisfy the Cl 22.6.4.3 reduced-perimeter rule.

### Reinforcement limits (Cl 8.6)

`[code]` **Minimum flexural reinforcement, nonprestressed**: `A_s,min =
0.0018A_g` near the tension face in the span direction (Cl 8.6.1.1) —
identical in form to the one-way slab/S&T requirement.

![[aci318-fig-r8.6.1.1-min-reinforcement-top-two-way-slab.png]]
*Fig. R8.6.1.1 — arrangement of minimum top reinforcement over a centerline
bay of a two-way slab under uniform gravity load, keyed to the same cutoff
geometry as Fig. 8.7.4.1.3 below (ACI 318M-19).*

`[code]` **Punching-shear-triggered minimum** (Cl 8.6.1.2): if `v_uv >
φ2λ_sλ√f'c` on the two-way shear critical section around a column,
concentrated load or reaction area,

**A_s,min = 5v_uv b_slab b_o / (φα_s f_y)**  (Eq. 8.6.1.2)

must be provided over `b_slab` (the Cl 8.4.2.2.3 effective width), using
`α_s` from Cl 22.6.5.3 and `λ_s` from Cl 22.5.5.1.3. `[derived]` This exists
because lightly-reinforced slab-column connections can fail in a
**flexure-driven** punching mode: yielding of the tension steel near the
column opens an existing inclined crack, and sliding along it triggers
punching at a lower shear than the Table 22.6.5.2/22.6.6.3 capacities
predict (Cl R8.6.1.2, citing Peiris and Ghali 2012, Hawkins and Ospina
2017). Shear reinforcement does **not** rescue a slab with `A_s < A_s,min`
from this failure mode — it may only increase plastic rotation beforehand.
Eq. 8.6.1.2 was derived for an interior column from the shear force
associated with local yielding, `8A_s,min f_y d / b_slab`, generalised to
`(α_s/5)A_s,min f_y d / b_slab` for edge/corner conditions — `A_s,min` is
also required at the periphery of drop panels and shear caps.

`[code]` **Minimum flexural reinforcement, prestressed**: effective
prestress `A_ps f_se` must provide ≥0.9 MPa average compressive stress on
the tributary slab section, checked at **every** cross section along the
span where thickness varies (Cl 8.6.2.1); bonded `A_s`+`A_ps` must develop
≥1.2× cracking load (waived if flexural+shear `φ`-strength ≥2× required,
Cl 8.6.2.2–8.6.2.2.1, mirrors Cl 7.6.2.1–7.6.2.2). `[code]` **Minimum bonded
deformed longitudinal reinforcement** in the precompressed tension zone,
bonded or unbonded tendons:

![[aci318-table-8.6.2.3-min-bonded-reinforcement-prestressed-slabs.png]]
*Table 8.6.2.3 — `A_s,min`: not required where calculated `f_t ≤ 0.17√f'c`;
`N_c/(0.5f_y)` for positive moment where `0.17√f'c < f_t ≤ 0.5√f'c`
(`N_c` = service-load tensile force on an uncracked homogeneous section);
`0.00075A_cf` for negative moment at columns where `f_t ≤ 0.5√f'c`
(ACI 318M-19).* `[derived]` This is a crack-control/ductility backstop, not
a strength requirement — it limits crack width/spacing when tensile stress
exceeds the modulus of rupture, and for unbonded tendons ensures the slab
fails as a flexural member rather than a "tied arch" (Cl R8.6.2.3).

### Reinforcement detailing — spacing and corner restraint (Cl 8.7.1–8.7.3)

`[code]` Cover, development length, splice length and bundled bars follow
the usual Cl 20.5.1/25.4/25.5/25.6 provisions (Cl 8.7.1). **Spacing**:
minimum per Cl 25.2; nonprestressed solid-slab deformed longitudinal
reinforcement ≤ lesser of `2h`/450 mm at critical sections, lesser of
`3h`/450 mm elsewhere (Cl 8.7.2.2) — `[derived]` this limit applies only to
solid slabs, not joists/waffle slabs, and exists to ensure genuine two-way
action, control cracking, and handle loads concentrated on small slab areas
(Cl R8.7.2.2). Prestressed tendon spacing (uniformly distributed loads) ≤
lesser of `8h`/1.5 m in at least one direction, with concentrated
loads/openings considered separately (Cl 8.7.2.3–8.7.2.4).

`[code]` **Corner restraint** (Cl 8.7.3): at exterior corners restrained by
edge walls or edge beams with `α_f > 1.0`, top and bottom reinforcement must
resist a factored moment per unit width equal to the panel's maximum
positive `M_u`, for a distance each direction from the corner equal to 1/5
the longer span:

![[aci318-fig-r8.7.3.1-slab-corner-reinforcement.png]]
*Fig. R8.7.3.1 — two permitted layouts: Option 1 places top steel parallel
to the diagonal and bottom steel perpendicular to it; Option 2 instead uses
two orthogonal layers top and bottom, both at max. 2h bar spacing
(ACI 318M-19).* `[derived]` Unrestrained slab corners lift when loaded; where
that lift is restrained, the resulting bending needs explicit reinforcement
(Cl R8.7.3.1) — ordinary primary-direction flexural steel may double as this
requirement.

### Flexural reinforcement termination and structural integrity (Cl 8.7.4)

`[code]` **Spandrel-beam/wall-supported edges**: positive-moment steel
extends to the slab edge with ≥150 mm embedment into the support; negative-
moment steel is bent/hooked/anchored and developed at the support face
(Cl 8.7.4.1.1–8.7.4.1.2). **Slabs without beams**:

![[aci318-fig-8.7.4.1.3-minimum-reinforcement-extensions.png]]
*Fig. 8.7.4.1.3 — minimum reinforcement extensions by strip/location, with
and without drop panels: column-strip top bars at `0.30ℓ_n`/`0.33ℓ_n` (50%)
and `0.20ℓ_n` (remainder, not less than `5d`), column-strip bottom bars
100% continuous/spliced per the splice-region band shown, middle-strip top
bars at `0.22ℓ_n`, middle-strip bottom bars at max. `0.15ℓ_n` (ACI 318M-19).*
`[code]` For unequal adjacent spans, negative-moment extensions follow the
**longer** span; bent bars are permitted only where depth-to-span allows
bends ≤45° (Cl 8.7.4.1.3(b)–(c)).

`[derived]` The `0.30ℓ_n`/`5d` pairing exists specifically to intercept
**punching-shear cracks**, which the Commentary notes can form at angles as
low as ~20°:

![[aci318-fig-r8.7.4.1.3-punching-shear-cracks-ordinary-thick-slab.png]]
*Fig. R8.7.4.1.3 — in an ordinary slab, top reinforcement terminating at
`0.3ℓ_n` already intercepts the potential punching crack; in a thick slab,
the same crack geometry requires the reinforcement to extend to `5d` instead
(ACI 318M-19).* `[code]` The Code therefore requires at least half the
column-strip top bars to extend to `5d` — this `5d` extension governs where
`ℓ_n/h < ~15` (Cl R8.7.4.1.3); for slabs acting as primary lateral-load
members, or under combined lateral+gravity loading, these minimums may not
be sufficient and analysis governs instead (Cl 8.7.4.1.3(a)).

`[code]` **Structural integrity** (Cl 8.7.4.2): all bottom deformed bars/wires
within the column strip, each direction, must be continuous or spliced
(mechanical/welded per Cl 25.5.7, or Class B tension lap per Cl 25.5.2),
spliced per the Fig. 8.7.4.1.3 region; ≥2 column-strip bottom bars/wires each
direction must pass within the region bounded by the column's longitudinal
reinforcement, anchored at exterior supports. `[derived]` This "integrity
reinforcement" gives the slab residual load-path ability to span to adjacent
supports after a single punching-shear failure (Cl R8.7.4.2.1,
Mitchell and Cook 1984).

### Flexural reinforcement in prestressed slabs (Cl 8.7.5)

`[code]` External tendons maintain eccentricity through the deflection
range (Cl 8.7.5.1); bonded steel required for strength follows Cl 7.7.3
(Cl 8.7.5.2). The Table 8.6.2.3(c) negative-moment bonded steel is placed in
the slab top, distributed between lines `1.5h` outside the column support
faces, ≥4 bars/wires/strands each direction, spacing ≤300 mm
(Cl 8.7.5.3). Post-tensioned anchorage zones/anchorages follow Cl 25.9/25.8
(Cl 8.7.5.4). Deformed reinforcement required by the Cl 8.6.2.3 unbonded
minimum extends ≥`ℓ_n/3` (centered) in positive-moment areas, ≥`ℓ_n/6` each
side of the support face in negative-moment areas (Cl 8.7.5.5.1).

`[code]` **Prestressed structural integrity** (Cl 8.7.5.6): ≥2 tendons
(≥12.7 mm strand) pass through or anchor within the column's longitudinal-
reinforcement region, each direction, passing under orthogonal tendons from
adjacent spans outside the column/shear-cap faces (Cl 8.7.5.6.1–8.7.5.6.2).
`[derived]` This mirrors the nonprestressed integrity-reinforcement logic —
tendons continuous through the column suspend the slab after a punching
failure, provided they can't burst through the top surface (Cl R8.7.5.6.1).
Where layout constraints make this impractical, bonded bottom deformed bars
may substitute: `A_s` = greater of `0.37√f'c c₂d/f_y` and `2.1c₂d/f_y` (`f_y`
capped at 550 MPa), passing within the column's reinforcement region,
anchored at exterior supports and developed to `f_y` beyond the column/shear-
cap face (Cl 8.7.5.6.3.1–8.7.5.6.3.3).

### Shear reinforcement — stirrups (Cl 8.7.6)

`[code]` Single-leg, simple-U, multiple-U and closed stirrups are permitted;
anchorage/geometry per Cl 25.7.1 (Cl 8.7.6.1–8.7.6.2). **Location/spacing**:
first stirrup at ≤`d/2` from the column face, stirrup spacing ≤`d/2`
(perpendicular to column face), vertical-leg spacing ≤`2d` (parallel to
column face) (Table 8.7.6.3). `[derived]` These spacing limits correspond to
details research has shown effective (Cl R8.7.6); anchorage per Cl 25.7.1 is
difficult in slabs thinner than 250 mm, which is why mechanically-anchored
vertical bars (plate or head) are an established alternative (ACI 421.1R).

![[aci318-fig-r8.7.6d-stirrup-shear-reinforcement-interior-column.png]]
*Fig. R8.7.6(d) — interior-column stirrup layout: the inner critical section
runs through the first line of stirrup legs, the outer section `d/2` beyond
the outermost line, shear reinforcement symmetric about the critical
section's centroid where moment transfer is negligible (ACI 318M-19).*

![[aci318-fig-r8.7.6e-stirrup-shear-reinforcement-edge-column.png]]
*Fig. R8.7.6(e) — edge-column layout: closed stirrups are recommended in as
symmetric a pattern as possible, since the closed legs extending from the
slab edge faces still provide useful torsional strength along the edge even
though their average shear stress is lower than on the inner face
(ACI 318M-19, Cl R8.7.6).*

`[code]` `v_s = A_v f_yt / (b_o s)` per [[aci318-two-way-shear-strength]]
Cl 22.6.7.2, where `A_v` is the total leg area on one peripheral line.

### Shear reinforcement — headed studs (Cl 8.7.7)

`[code]` Headed shear stud reinforcement is placed perpendicular to the slab
plane (Cl 8.7.7.1); overall assembly height ≥ slab thickness minus (top
flexural cover + base-rail cover + half the flexural bar diameter)
(Cl 8.7.7.1.1). **Location/spacing**:

![[aci318-fig-r8.7.7-headed-shear-stud-arrangements.png]]
*Fig. R8.7.7 — typical stud arrangements and shear critical sections for
interior, edge and corner columns, plus the Section A-A base-rail detail
(ACI 318M-19).* `[derived]` First peripheral line at `d/2` from the column
face (all cases); constant spacing between peripheral lines `3d/4`
(nonprestressed, `v_u ≤ 0.5√f'c`) or `d/2` (nonprestressed, `v_u > 0.5√f'c`)
or `3d/4` (prestressed per Cl 22.6.5.4); adjacent-stud spacing on the
nearest peripheral line ≤`2d` (Table 8.7.7.1.2). `[code]` Compared with a
stirrup leg's bent-end anchorage, a stud head shows smaller slip and smaller
shear crack widths — the basis for headed studs getting both a higher
strength allowance (Table 22.6.6.1) and wider peripheral-line spacing than
stirrups (Cl R8.7.7, citing ACI 421.1R).

### Nonprestressed two-way joist systems (Cl 8.8)

`[code]` A monolithic combination of regularly-spaced ribs and a top slab
spanning two orthogonal directions (Cl 8.8.1.1). Rib width ≥100 mm anywhere
along depth; rib depth ≤3.5× minimum width; clear rib spacing ≤750 mm
(Cl 8.8.1.2–8.8.1.4) — `[derived]` the spacing cap exists because the rules
below permit **higher** shear strength and **less** cover than an ordinary
beam would get, justified by load redistribution to adjacent joists in
these small, repetitive members (Cl R8.8.1.4–R8.8.1.5). `[code]` `V_c` may
be taken as **1.1×** the Cl 22.5 value (Cl 8.8.1.5). Structural integrity:
≥1 continuous bottom bar per joist, anchored to develop `f_y` at supports
(Cl 8.8.1.6). Perpendicular-to-rib reinforcement satisfies slab moment
strength (considering load concentrations) and is ≥ the Cl 24.4
shrinkage-temperature area (Cl 8.8.1.7). Joist construction outside these
limits is designed as ordinary slabs and beams (Cl 8.8.1.8).

`[code]` With permanent burned-clay/concrete-tile fillers (unit compressive
strength ≥`f'c`): slab thickness over fillers ≥ greater of `1/12` clear rib
distance and 40 mm; filler vertical shells in contact with ribs may count
toward shear/negative-moment strength, other filler portions may not
(Cl 8.8.2). With other fillers or removable forms: slab thickness ≥ greater
of `1/12` clear rib distance and 50 mm (Cl 8.8.3).

### Lift-slab construction (Cl 8.9)

`[code]` Where it is impractical to pass the Cl 8.7.5.6.1 tendons or
Cl 8.7.4.2/8.7.5.6.3 bottom bars through the column, ≥2 post-tensioned
tendons or ≥2 bonded bottom bars/wires each direction instead pass through
the lifting collar as close to the column as practicable, continuous or
spliced per Cl 25.5.7/25.5.2, anchored at the lifting collar at exterior
columns (Cl 8.9.1).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-two-way-slab-design-basis]] — Cl 8.1–8.4: scope, thickness,
  design-strip definitions, factored moment transfer and two-way shear
  stress that feed into this page's design-strength checks.
- [[aci318-two-way-shear-strength]] — Cl 22.6, the `v_c`/`v_s` capacity
  calculations this page's stirrup/headed-stud provisions size reinforcement
  against.
- [[aci318-sectional-strength-flexure-and-axial]], [[aci318-one-way-shear-strength]]
  — Cl 22.3/22.5, the `M_n`/`V_n` calculations behind Cl 8.5.
- [[aci318-one-way-slab-design]] — Chapter 7, incl. the structural-integrity
  and S&T reinforcement provisions this page's detailing mirrors.
- [[concrete-slab-punching-shear]], [[concrete-slab-crack-control]],
  [[concrete-beam-detailing]] — the AS 3600 equivalents, for structural
  comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 8 Cl 8.5–8.9 (pp. 109–128), incl.
  Table 8.6.2.3, Figs. R8.6.1.1, R8.7.3.1, 8.7.4.1.3, R8.7.4.1.3, R8.7.6(d),
  R8.7.6(e), R8.7.7.
