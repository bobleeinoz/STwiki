---
title: ACI 318M-19 two-way slab design basis — scope, thickness, moment transfer, shear stress
category: 2-concrete
tags: [aci, two-way-slab, flat-plate, flat-slab, slab-design, thickness, moment-transfer]
standards: [ACI 318M-19 Cl 8.1, ACI 318M-19 Cl 8.2, ACI 318M-19 Cl 8.3, ACI 318M-19 Cl 8.4]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 two-way slab design basis

> Scope: ACI 318M-19 Cl 8.1–8.4 — scope and slab systems covered, design
> strip/panel definitions, minimum-thickness design limits (Tables 8.3.1.1
> and 8.3.1.2), and required strength: factored moment transfer between slab
> and column (`γ_f M_sc`) and the resulting factored two-way shear stress
> (`γ_v M_sc`). Design strength, openings, reinforcement limits/detailing,
> shear reinforcement, joist systems and lift-slab construction are covered
> on [[aci318-two-way-slab-reinforcement-and-shear-detailing]]. This is an
> **ACI 318M-19 page, kept separate from the AS 3600:2018 concept pages**
> elsewhere in `2-concrete` — see [[aci-318m-19-building-code-concrete]] for
> why.

## Summary

`[code]` Chapter 8 applies to slabs reinforced for flexure in **two
directions**, with or without beams between supports (Cl 8.1.1): solid
slabs, slabs on stay-in-place noncomposite steel deck, composite slabs of
separately-cast elements acting as a unit, and two-way joist systems per
Cl 8.8. `[derived]` This covers flat plates, flat slabs, waffle slabs, and
paneled-ceiling two-way wide-band-beam systems (Cl R8.1.1); slabs-on-ground
that don't transfer vertical load from the structure to the soil are
excluded. The chapter's explicit design procedures apply to slabs with
beams only where beams sit at panel edges on essentially non-deflecting
(column/girder) supports at the panel corners; slabs on walls treat the
wall as an infinitely-stiff beam spanning the full panel edge (Cl R8.1.1)
— narrower walls are instead treated as columns.

`[code]` **Any procedure satisfying equilibrium and geometric compatibility**
is permitted, provided design strength meets required strength everywhere
and serviceability is satisfied — the direct design method (DDM) and
equivalent frame method (EFM) are explicitly named as permitted (Cl 8.2.1).
`[derived]` Despite this mention, Chapter 8 itself gives **no** step-by-step
DDM/EFM procedure — both methods were removed from the Code's main body in
2014 and are only accessible by cross-reference to the 2014 Code's own text
(see [[aci318-structural-analysis-methods]] Cl 6.2.4.1, which records this
in more depth); both are limited to orthogonal frames under gravity loads
only (Cl R8.2.1).

## Detail

### General — panel geometry, drop panels, shear caps (Cl 8.2)

`[code]` Concentrated loads, slab openings and voids must be considered
(Cl 8.2.2) — same as Cl 7.2.1 for one-way slabs. Slabs prestressed with
average effective compressive stress `< 0.9 MPa` are designed as
nonprestressed (Cl 8.2.3).

`[code]` A **drop panel** (used to reduce minimum thickness per Cl 8.3.1.1
or negative-moment reinforcement per Cl 8.5.2.2) must project below the slab
≥1/4 of the adjacent slab thickness, and extend ≥1/6 of the span (support
centerline to centerline) from the support centerline in each direction
(Cl 8.2.4). A **shear cap** (increasing the critical section at a
slab-column joint) must project below the slab soffit and extend
horizontally from the column face a distance ≥ its own depth below the slab
soffit (Cl 8.2.5). `[derived]` A shear cap not meeting the Cl 8.2.4
drop-panel dimensions can still function as a shear cap to boost shear
strength, just not toward the thickness/reinforcement reductions a true drop
panel allows (Cl R8.2.4–R8.2.5). Materials (Chapters 19/20) and
beam-column/slab-column joints (Chapter 15) follow the usual provisions.

### Design strip and panel definitions (Cl 8.4.1.4–8.4.1.9)

`[code]` For slabs on columns/walls, `c_1`, `c_2`, `ℓ_n` are based on an
**effective support area** — the intersection of the slab/drop-panel/shear-cap
soffit with the largest right circular cone, right pyramid or tapered wedge
within the column (and capital/bracket) oriented ≤45° to the column axis
(Cl 8.4.1.4). A **column strip** is a design strip each side of a column
centerline, width = lesser of `0.25ℓ_2` and `0.25ℓ_1`, including any beam
within the strip (Cl 8.4.1.5). A **middle strip** is bounded by two column
strips (Cl 8.4.1.6). A **panel** is bounded by column, beam or wall
centerlines on all sides (Cl 8.4.1.7).

`[code]` For **monolithic or fully composite** construction, a beam includes
the portion of slab on each side extending a distance equal to the beam's
projection above/below the slab (whichever is greater), capped at `4×` the
slab thickness (Cl 8.4.1.8):

![[aci318-fig-r8.4.1.8-beam-flange-portion-of-slab.png]]
*Fig. R8.4.1.8 — two worked examples of the beam-flange portion-of-slab rule:
`b_w + 2h_b ≤ b_w + 8h_f` for a beam with slab on both sides, `h_b ≤ 4h_f`
limiting the one-sided case (ACI 318M-19).* Gravity-load and lateral-load
analysis results may be combined (Cl 8.4.1.9).

### Design limits — minimum thickness (Cl 8.3)

`[code]` **Nonprestressed slabs without interior beams** (max long:short
span ratio 2), unless calculated deflections (Cl 8.3.2) are satisfied:

![[aci318-table-8.3.1.1-min-thickness-two-way-slabs-no-beams.png]]
*Table 8.3.1.1 — minimum `h` (mm), `ℓ_n`/33 to `ℓ_n`/40 depending on `f_y`
(280/420/550 MPa), drop panels and edge beams, interpolated linearly for
intermediate `f_y` (ACI 318M-19).* Absolute floor: 125 mm without drop
panels, 100 mm with drop panels per Cl 8.2.4 (Cl 8.3.1.1(a)/(b)).
`[derived]` For `f_y > 550 MPa`, deflection must additionally be checked
using a reduced modulus of rupture `f_r = 0.41√f'c` — `[code]` higher-grade
longitudinal steel can produce larger long-term deflections unless cracked
service stresses stay below 280 MPa (Cl R8.3.1.1).

`[code]` **Nonprestressed slabs with beams on all sides**:

![[aci318-table-8.3.1.2-min-thickness-two-way-slabs-with-beams.png]]
*Table 8.3.1.2 — minimum `h` by average beam stiffness ratio `α_fm`: Table
8.3.1.1 governs below `α_fm = 0.2`; between 0.2 and 2.0, greater of a
span/stiffness formula and 125 mm; above 2.0, greater of a simplified
span/stiffness formula and 90 mm (ACI 318M-19).* `[derived]` For
long:short span ratios `> 2`, the formula expressions can give unreasonable
results — the Commentary directs use of the Cl 7.3.1 one-way rules instead
(Cl R8.3.1.2). Discontinuous edges without an edge beam (`α_f ≥ 0.80`)
either need such a beam or a ≥10% increase to the formula thickness
(Cl 8.3.1.2.1).

`[code]` A monolithic/composite floor finish may count toward `h`
(Cl 8.3.1.3, mirroring Cl 7.3.1.2). Slabs using single-/multiple-leg
stirrups as shear reinforcement must have `d` sufficient to satisfy
Cl 22.6.7.1 (Cl 8.3.1.4). **Calculated deflection limits** (Cl 8.3.2) apply
to: slabs not satisfying Cl 8.3.1; slabs without interior beams and
long:short span ratio `> 2.0`; and all prestressed slabs — checked per
Cl 24.2/24.2.2 ([[aci318-serviceability-deflection-and-cracking]]).
Reinforcement strain limit (tension-controlled, Table 21.2.2) and prestressed
stress-class/limits (Class U with `f_t ≤ 0.5√f'c`, Cl 24.5.3/24.5.4) mirror
the one-way slab provisions (Cl 8.3.3, Cl 8.3.4).

### Required strength — factored moment transfer (Cl 8.4.1–8.4.2)

`[code]` Required strength follows Chapter 5 load combinations and Chapter 6
analysis (Cl 8.4.1.1–8.4.1.2); prestressing reactions per Cl 5.3.11
(Cl 8.4.1.3). `[derived]` For prestressed systems, numerical analysis (e.g.
the historical EFM) is required rather than simplified approaches like DDM,
since prismatic-section approximations have been shown to give erroneous,
unsafe results for prestressed slabs (Cl R8.4.1.2). `M_u` at the support may
be taken at the face of support for slabs built integrally with it
(Cl 8.4.2.1).

`[code]` **Moment transferred by flexure** (Cl 8.4.2.2), primarily for slabs
*without* beams (Cl R8.4.2.2.1): a fraction `γ_f M_sc` of the factored
slab-to-column moment `M_sc` transfers by flexure, where

**γ_f = 1 / (1 + (2/3)√(b₁/b₂))**  (Eq. 8.4.2.2.2)

over an effective slab width `b_slab` = column/capital width plus a distance
each side per:

![[aci318-table-8.4.2.2.3-effective-slab-width-limits.png]]
*Table 8.4.2.2.3 — effective slab width extends the lesser of `1.5h`
(slab or drop panel/shear cap) and the distance to the slab/drop/cap edge,
each side of the column (ACI 318M-19).*

`[code]` For **nonprestressed** slabs, `γ_f` may be increased to a maximum
modified value where `v_uv` and `ε_t` (within `b_slab`) satisfy limits that
depend on column location and span direction:

![[aci318-table-8.4.2.2.4-max-modified-gamma-f.png]]
*Table 8.4.2.2.4 — maximum modified `γ_f`: 1.0 for corner columns and for
edge columns perpendicular to the edge; up to `1.25/(1 + (2/3)√(b₁/b₂)) ≤ 1.0`
for edge columns parallel to the edge and interior columns, conditional on
`v_uv` staying below a fraction of `φv_c` and `ε_t ≥ ε_ty + 0.003` or
`ε_ty + 0.008` (ACI 318M-19).* `[derived]` This flexibility exists because
interior/exterior slab-column connections can redistribute `M_sc` between
flexure and shear transfer somewhat — interior columns up to 25% more by
flexure if factored shear (excluding moment-transfer shear) stays `≤ 40%` of
`φv_c`; exterior columns similarly at 75%/50% of `φv_c` for edge/corner
columns (Cl R8.4.2.2.4). The `ε_ty + 0.003`/`ε_ty + 0.008` strain limits
replaced flat 0.004/0.010 constants in 2019 specifically to extend the rule
to higher-grade nonprestressed reinforcement (Cl R8.4.2.2.4). Reinforcement
resisting `γ_f M_sc` is concentrated over the effective width by closer
spacing or added steel (Cl 8.4.2.2.5); the `M_sc` fraction not transferred by
flexure is assumed transferred by eccentricity of shear per Cl 8.4.4.2
(Cl 8.4.2.2.6).

### Required strength — factored one-way and two-way shear (Cl 8.4.3–8.4.4)

`[code]` **One-way shear**: `V_u` at face of support for integral
construction (Cl 8.4.3.1); the same three-condition critical-section shift
(to `d` nonprestressed / `h/2` prestressed from the face of support) used for
one-way slabs applies here too (Cl 8.4.3.2, mirrors Cl 7.4.3.2).

`[code]` **Two-way shear critical section**: per Cl 22.6.4 generally, or
Cl 22.6.4.2 for slabs with stirrup/headed-stud shear reinforcement
(Cl 8.4.4.1 — see [[aci318-two-way-shear-strength]]).

`[code]` **Factored shear stress with moment transfer** (Cl 8.4.4.2):
`v_u` combines `v_uv` (direct shear stress) and the stress from `γ_v M_sc`,
where

**γ_v = 1 − γ_f**  (Eq. 8.4.4.2.2)

applied at the critical section's centroid, assumed to vary **linearly**
about that centroid:

![[aci318-fig-r8.4.4.2.3-assumed-shear-stress-distribution.png]]
*Fig. R8.4.4.2.3 — assumed linear shear stress distribution for interior and
edge columns: `v_u,AB = v_uv + γ_v M_sc c_AB/J_c`, `v_u,CD = v_uv − γ_v M_sc
c_CD/J_c`, with `J_c` an assumed-critical-section property analogous to
polar moment of inertia (ACI 318M-19).* `[derived]` The 60%/40%
flexure/eccentric-shear split underlying Eq. 8.4.2.2.2 and 8.4.4.2.2 traces
to Hanson and Hanson (1968) testing, predominantly on square columns — round
columns are approximated as an equal-area square (Cl R8.4.4.2.2). For an
**interior** column, `J_c = d(c₁+d)³/6 + (c₁+d)d³/6 + d(c₂+d)(c₁+d)²/2`;
analogous expressions apply for edge/corner columns (Cl R8.4.4.2.3). Where
shear reinforcement is present, the critical section beyond it is generally
**polygonal** rather than rectangular (Fig. R8.7.6(d)/(e), see
[[aci318-two-way-slab-reinforcement-and-shear-detailing]]) — stress
equations for such sections are given in ACI 421.1R, outside this Code.

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-two-way-slab-reinforcement-and-shear-detailing]] — Cl 8.5–8.9:
  design strength, openings, reinforcement limits/detailing, shear
  reinforcement, joist systems, lift-slab construction.
- [[aci318-structural-analysis-methods]] — Cl 6.2.4.1, why DDM/EFM are
  "permitted" by Cl 8.2.1 but not detailed in Chapter 8 itself.
- [[aci318-two-way-shear-strength]] — Cl 22.6, the `v_c`/`v_s` capacity
  calculations that `v_u` from this page's Cl 8.4.4.2 is checked against.
- [[aci318-one-way-slab-design]] — Chapter 7, the one-way counterpart with
  the same seven-section structure.
- [[concrete-slab-punching-shear]], [[concrete-slab-strength-in-bending]],
  [[concrete-slab-deflection]] — the AS 3600 equivalents, for structural
  comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 8 Cl 8.1–8.4 (pp. 99–109), incl.
  Tables 8.3.1.1, 8.3.1.2, 8.4.2.2.3, 8.4.2.2.4 and Figs. R8.4.1.8,
  R8.4.4.2.3.
