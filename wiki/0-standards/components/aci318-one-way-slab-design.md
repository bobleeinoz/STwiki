---
title: ACI 318M-19 one-way slab design — thickness, strength, reinforcement detailing
category: 0-standards
tags: [aci, one-way-slab, slab-design, thickness, reinforcement-detailing]
standards: [ACI 318M-19 Cl 7.1, ACI 318M-19 Cl 7.2, ACI 318M-19 Cl 7.3, ACI 318M-19 Cl 7.4, ACI 318M-19 Cl 7.5, ACI 318M-19 Cl 7.6, ACI 318M-19 Cl 7.7]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 one-way slab design

> Scope: ACI 318M-19 Chapter 7 (Cl 7.1–7.7) in full — scope and systems
> covered, minimum-thickness/deflection design limits, required and design
> strength (cross-referencing Chapter 22 for the actual `M_n`/`V_n`
> calculations), reinforcement limits (minimum flexural, shear, shrinkage
> and temperature), and reinforcement detailing (spacing, termination,
> structural integrity). This is an **ACI 318M-19 page, kept separate from
> the AS 3600:2018 concept pages** elsewhere in `2-concrete` — see
> [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Chapter 7 applies to slabs reinforced for flexure in **one
direction** (Cl 7.1.1): solid slabs, slabs on stay-in-place noncomposite
steel deck, composite slabs of separately-cast concrete elements acting as a
unit, and precast prestressed hollow-core slabs. `[derived]` One-way **joist**
systems are explicitly carved out of this chapter — the Commentary points to
Chapter 9 (Beams) instead (Cl R7.1.1); composite steel-deck design itself is
deferred to SDI publication "C" rather than given in the Code.

`[code]` Chapter 7 follows the same seven-section skeleton used throughout
Part 3 of the Code (scope, general, design limits, required strength, design
strength, reinforcement limits, reinforcement detailing) — the same skeleton
as [[aci318-two-way-slab-design-basis]] and [[aci318-two-way-slab-reinforcement-and-shear-detailing]]
for Chapter 8, and the beam/column chapters once ingested.

## Detail

### General (Cl 7.2)

`[code]` Concentrated loads, slab openings and voids within the slab must be
considered in design (Cl 7.2.1) — `[derived]` these can locally create
two-way behaviour in an otherwise one-way slab (Cl R7.2.1). Concrete/steel
material properties follow Chapters 19/20 as usual; cast-in-place
beam-column/slab-column joints follow Chapter 15, precast connections follow
the force-transfer requirements of Cl 16.2.

### Design limits (Cl 7.3)

`[code]` **Minimum thickness** (Cl 7.3.1.1), solid nonprestressed slabs not
supporting/attached to deflection-sensitive partitions, unless calculated
deflections satisfy Cl 7.3.2:

| Support condition   | Minimum `h` |
| -------------------- | ----------- |
| Simply supported     | `ℓ/20`      |
| One end continuous   | `ℓ/24`      |
| Both ends continuous | `ℓ/28`      |
| Cantilever            | `ℓ/10`      |

(Table 7.3.1.1, normalweight concrete and `f_y = 420 MPa`.) `[code]` For
other `f_y`, multiply by `(0.4 + f_y/700)` (Cl 7.3.1.1.1); for lightweight
concrete (`w_c` 1440–1840 kg/m³), multiply by the greater of `1.65 − 0.0003w_c`
and `1.09` (Cl 7.3.1.1.2, also applied to shored nonprestressed composite
slabs with lightweight concrete in compression per Cl 7.3.1.1.3). A
monolithic or composite floor finish thickness may count toward `h`
(Cl 7.3.1.2).

`[code]` **Calculated deflection limits** (Cl 7.3.2): required for
nonprestressed slabs not satisfying Cl 7.3.1 and for all prestressed slabs,
per Cl 24.2/24.2.2 — see [[aci318-serviceability-deflection-and-cracking]].
Composite nonprestressed slabs satisfying Cl 7.3.1 need only check
deflections occurring **before** composite action, unless the precomposite
thickness alone also satisfies Cl 7.3.1 (Cl 7.3.2.2).

`[code]` **Reinforcement strain limit**: nonprestressed one-way slabs must be
tension-controlled per Table 21.2.2 (Cl 7.3.3.1) — see
[[aci318-strength-reduction-factors]]. **Prestressed stress limits**:
classified Class U/T/C per Cl 24.5.2, with transfer/service stresses per
Cl 24.5.3/24.5.4 (Cl 7.3.4).

### Required strength (Cl 7.4)

`[code]` Required strength follows the Chapter 5 load combinations and
Chapter 6 analysis procedures; prestressing reaction effects are considered
per Cl 5.3.11 (Cl 7.4.1). For slabs built integrally with supports, `M_u`
and `V_u` may be taken at the face of support (Cl 7.4.2.1, Cl 7.4.3.1).
`[code]` The shear **critical section** may be taken at `d` from the face of
support (nonprestressed) or `h/2` (prestressed) if: the support reaction
introduces compression into the slab end, loads are applied at/near the top
surface, and no concentrated load falls between the face of support and the
critical section (Cl 7.4.3.2(a)–(c)) — `[derived]` the same three-condition
test used for beams (see R9.4.3.2, not yet ingested).

### Design strength (Cl 7.5)

`[code]` `φM_n ≥ M_u` and `φV_n ≥ V_u` at every section, with load-effect
interaction considered (Cl 7.5.1.1); `φ` per Chapter 21
([[aci318-strength-reduction-factors]]). `M_n` per Cl 22.3
([[aci318-sectional-strength-flexure-and-axial]]); `V_n` per Cl 22.5
([[aci318-one-way-shear-strength]]); composite slabs additionally check
horizontal shear `V_nh` per Cl 16.4.

`[code]` External tendons are treated as **unbonded** for flexural strength
unless effectively bonded to the concrete along their full length
(Cl 7.5.2.2). `[code]` **T-beam perpendicular reinforcement** (Cl 7.5.2.3):
where a slab's primary flexural steel runs parallel to a T-beam's
longitudinal axis (the slab acting as the beam's flange), perpendicular
reinforcement must be designed for the factored load on the overhanging slab
width acting as a cantilever, using the Cl 6.3.2 effective flange width.
`[derived]` This is not joist construction, and is distinct from ordinary
shrinkage-and-temperature steel — it is intended to catch "unintended"
negative moments over the beam exceeding what S&T reinforcement alone would
resist (Cl R7.5.2.3).

### Reinforcement limits (Cl 7.6)

`[code]` **Minimum flexural reinforcement, nonprestressed**: `A_s,min =
0.0018A_g` (Cl 7.6.1.1) — `[derived]` numerically identical to the Cl 24.4.3.2
shrinkage-and-temperature requirement, but placed close to the tension face
rather than distributed between faces (Cl R7.6.1.1).

`[code]` **Minimum flexural reinforcement, prestressed**: bonded `A_s`+`A_ps`
must develop ≥1.2× the cracking load from `f_r` (Cl 19.2.3) (Cl 7.6.2.1),
waived if both flexural and shear `φ`-strength are ≥2× required strength
(Cl 7.6.2.2). For slabs with **unbonded** tendons, bonded deformed
`A_s,min ≥ 0.004A_ct` (`A_ct` = area between the tension face and the gross
section centroid) (Cl 7.6.2.3).

`[code]` **Minimum shear reinforcement**: `A_v,min` required wherever `V_u >
φV_c` (or `V_u > 0.5φV_cw` for untopped precast prestressed hollow-core
slabs `h > 315 mm`) (Cl 7.6.3.1) — `[derived]` solid slabs/footings get more
lenient minimum-shear rules than beams because of load-sharing between weak
and strong areas, **but** deep, lightly-reinforced one-way slabs (especially
high-strength concrete or small aggregate) have been shown to fail below the
calculated `V_c`, particularly under concentrated loads (Cl R7.6.3.1 — tests
cited: Angelakos et al. 2001, Lubell et al. 2004, Brown et al. 2006).
Testing-based strength evaluation may substitute per Cl 7.6.3.2 (simulating
differential settlement, creep, shrinkage, temperature effects); if shear
reinforcement is required, `A_v,min` follows the beam provision Cl 9.6.3.4.

`[code]` **Minimum shrinkage and temperature reinforcement** per Cl 24.4
(Cl 7.6.4.1). For prestressed S&T reinforcement (Cl 24.4.4), monolithic
cast-in-place post-tensioned beam-and-slab construction defines gross
concrete area as the beam area (incl. slab thickness) plus slab area within
half the clear distance to adjacent beam webs, beam tendon force countable
toward total prestress (Cl 7.6.4.2.1); non-monolithic/wall-supported slabs
use the tributary slab section instead (Cl 7.6.4.2.2); at least one tendon
is required between faces of adjacent beams/walls (Cl 7.6.4.2.3):

![[aci318-fig-r7.6.4.2-beam-slab-section-shrinkage-temp-tendons.png]]
*Fig. R7.6.4.2 — monolithic post-tensioned beam-and-slab construction: beam
and slab tendons within the orange tributary area must together provide
0.9 MPa minimum average compressive stress on that area (ACI 318M-19).*

### Reinforcement detailing (Cl 7.7)

`[code]` Cover (Cl 20.5.1), development length (Cl 25.4), splices (Cl 25.5)
and bundled bars (Cl 25.6) follow the usual Code-wide provisions.
**Spacing**: minimum per Cl 25.2; for nonprestressed and Class C prestressed
slabs, bonded longitudinal reinforcement closest to the tension face follows
the Cl 24.3 crack-control spacing; for nonprestressed and Class T/C
prestressed slabs with unbonded tendons, deformed longitudinal spacing ≤
lesser of `3h`/450 mm (Cl 7.7.2.1–7.7.2.3) — `[derived]` this unbonded-tendon
spacing rule was extended to Class T/C slabs only in 2019, since those slabs
rely solely on deformed reinforcement for crack control (Cl R7.7.2.3).
Reinforcement required by the Cl 7.5.2.3 T-beam rule has its own spacing cap:
lesser of `5h`/450 mm (Cl 7.7.2.4).

`[code]` **Termination of nonprestressed flexural reinforcement**
(Cl 7.7.3): calculated tension/compression force must be developed on each
side of the critical section (points of max stress, or where bent/terminated
bars are no longer needed for flexure); continuing bars extend ≥ greater of
`d`/`12d_b` past where no longer needed (Cl 7.7.3.1–7.7.3.4). Termination in
a tension zone requires one of: `V_u ≤ (2/3)φV_n` at the cutoff; for No. 36
bars or smaller, continuing steel provides double the required flexural area
**and** `V_u ≤ (3/4)φV_n`; or excess stirrup area `≥ 0.41b_w s/f_yt` over
`3/4d` from the cutoff, spaced `≤ d/(8β_b)` (Cl 7.7.3.5(a)–(c)). `[code]`
**Termination at supports/inflection points** (Cl 7.7.3.8): ≥1/3 of max
positive-moment steel extends along the slab bottom into a simple support
(≥1/4, ≥150 mm, at other supports); `d_b` at simple supports/inflection
points is limited by `d ≥ 1.3M_n/V_u + ℓ_a` (confined end) or `d ≥
M_n/V_u + ℓ_a` (unconfined), waived with a standard hook/equivalent
mechanical anchorage; ≥1/3 of negative-moment steel at a support extends
past the inflection point by the greatest of `d`, `12d_b`, `ℓ_n/16`.

`[code]` **Prestressed reinforcement termination** (Cl 7.7.4): external
tendons attached to maintain specified eccentricity through the full
deflection range; nonprestressed steel required for flexural strength
follows the Cl 7.7.3 rules above; post-tensioned anchorage zones/anchorages
follow Cl 25.9/25.8. Deformed reinforcement required by the Cl 7.6.2.3
unbonded-tendon minimum extends ≥`ℓ_n/3` in positive-moment areas (centered)
and ≥`ℓ_n/6` each side of the support face in negative-moment areas
(Cl 7.7.4.4.1).

`[code]` **Shrinkage and temperature reinforcement detailing** (Cl 7.7.6):
placed perpendicular to flexural reinforcement; nonprestressed deformed S&T
spacing ≤ lesser of `5h`/450 mm. For prestressed S&T tendons: spacing (and
distance from beam/wall face to the nearest tendon) ≤1.8 m (Cl 7.7.6.3.1);
if tendon spacing exceeds 1.4 m, additional deformed S&T reinforcement
parallel to the tendons is required, extending from the slab edge a distance
≥ the tendon spacing:

![[aci318-fig-r7.7.6.3.2-slab-edge-added-shrinkage-temp-reinforcement.png]]
*Fig. R7.7.6.3.2 — plan view at a slab edge showing added deformed S&T
reinforcement where tendon spacing `s` exceeds 1.4 m (ACI 318M-19).*
`[derived]` Widely-spaced tendons leave non-uniform compressive stress near
slab edges — the added bars reinforce the under-compressed regions between
tendons (Cl R7.7.6.3.2).

`[code]` **Structural integrity reinforcement** (Cl 7.7.7): ≥1/4 of the
maximum positive-moment reinforcement runs continuous; anchored to develop
`f_y` at noncontinuous-support faces; splices (if needed) located near
supports, using mechanical/welded splices (Cl 25.5.7) or Class B tension lap
splices (Cl 25.5.2).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-sectional-strength-flexure-and-axial]], [[aci318-one-way-shear-strength]]
  — the Chapter 22 `M_n`/`V_n` provisions this chapter's design strength
  section (Cl 7.5) invokes.
- [[aci318-strength-reduction-factors]] — Chapter 21 `φ`-factors and the
  Table 21.2.2 tension-controlled strain limit.
- [[aci318-serviceability-deflection-and-cracking]] — Cl 24.2 deflection
  limits and Cl 24.3/24.4 crack-control/shrinkage-temperature provisions
  cross-referenced throughout this page.
- [[aci318-two-way-slab-design-basis]], [[aci318-two-way-slab-reinforcement-and-shear-detailing]]
  — Chapter 8, the two-way slab counterpart with the same seven-section
  structure.
- [[as3600-slab-strength-in-bending]], [[as3600-slab-deflection]],
  [[as3600-slab-crack-control]], [[as3600-beam-detailing]] — the AS 3600
  equivalents, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 7 Cl 7.1–7.7 (pp. 89–99), incl.
  Figs. R7.6.4.2 and R7.7.6.3.2.
