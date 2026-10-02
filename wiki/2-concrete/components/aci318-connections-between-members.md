---
title: ACI 318M-19 connections between members — precast connections, foundation connections, composite horizontal shear, brackets and corbels
category: 2-concrete
tags: [aci, precast, connections, integrity-ties, composite, corbels, brackets]
standards: [ACI 318M-19 Cl 16.1, ACI 318M-19 Cl 16.2, ACI 318M-19 Cl 16.3, ACI 318M-19 Cl 16.4, ACI 318M-19 Cl 16.5]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 connections between members

> Scope: ACI 318M-19 Chapter 16 in full — precast member connections
> (strength, integrity ties, bearing dimensions), connections to foundations,
> horizontal shear transfer in composite concrete flexural members, and
> brackets and corbels. This is an **ACI 318M-19 page, kept separate from the
> AS 3600:2018 concept pages** elsewhere in `2-concrete` — see
> [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Chapter 16 covers joints and connections at the intersection of concrete
members and load transfer between concrete surfaces: (a) connections of precast
members, (b) connections between foundations and cast-in-place or precast
members, (c) horizontal shear strength of composite concrete flexural members,
(d) brackets and corbels (Cl 16.1.1). Anchors in concrete (cast-in/post-installed
bolts, studs) are Chapter 17 — see [[aci318-anchoring-general-and-tensile-strength]].

## Detail

### Connections of precast members (Cl 16.2)

`[code]` **General** (Cl 16.2.1): force transfer by grouted joints, shear keys,
bearing, anchors, mechanical connectors, reinforcement, reinforced topping or a
combination is permitted; adequacy must be verified by analysis or test;
connection details relying **solely on friction from gravity loads are not
permitted**; connections and adjacent regions resist forces and accommodate
deformations from all load effects in the precast system, consider restraint of
volume change (Cl 5.3.6) and the effects of fabrication/erection tolerances, and
for multi-component connections consider differences in component stiffness,
strength and ductility; **integrity ties** are provided in the vertical,
longitudinal and transverse directions and around the perimeter per Cl 16.2.4 or
16.2.5.

`[code]` **Required strength** (Cl 16.2.2): from Chapters 5 and 6 combinations.
For bearing connections the restraint force `N_uc` is (a) for connections **not**
on bearing pads, calculated with `V_u` per Cl 5.3.6 treating restraint as a live
load, or (b) for connections **on bearing pads**, **20%** of the sustained
unfactored vertical reaction × load factor **1.6**; `N_uc` need not exceed
`N_uc,max`, the maximum restraint force the bearing load path can transmit × the
live-load factor. If the bearing friction coefficient is established by test,
`N_uc,max` = sustained unfactored vertical reaction × friction coefficient ×
1.6 (Cl 16.2.2.3–16.2.2.4).

`[code]` **Design strength** (Cl 16.2.3): `φS_n ≥ U` with φ per Cl 21.2; bearing
strength `B_n` at contact surfaces per Cl 22.8 (the lesser of supported/supporting
surface strengths, not exceeding any intermediate bearing element); where shear
dominates across a plane `V_n` may use shear-friction Cl 22.9 (see
[[aci318-bearing-and-shear-friction]]).

`[code]` **Minimum connection strength and integrity ties** (Cl 16.2.4): unless
Cl 16.2.5 governs, longitudinal and transverse integrity ties connect precast
members to a lateral-force-resisting system and vertical ties connect adjacent
floor/roof levels. Diaphragm-to-supported-member connections have nominal tensile
strength ≥ **4.4 kN/m** (Cl 16.2.4.2). **Vertical integrity ties** at horizontal
joints between vertical precast members (except cladding): precast **columns** —
nominal tensile strength ≥ `1.4A_g` (N, `A_g` in mm²; reduced effective area
allowed but ≥ half the gross area); precast **wall panels** — at least two ties,
each ≥ **44 kN** (Cl 16.2.4.3).

`[code]` **Precast bearing wall structures of three or more storeys** (Cl 16.2.5):
floor/roof longitudinal and transverse ties ≥ **22 kN per metre** of width/length,
over interior wall supports and between floor/roof and exterior walls, within
600 mm of the floor/roof plane; longitudinal ties parallel to slab span at
≤ 3 m centres with provision to transfer forces around openings; transverse ties
perpendicular to span at ≤ bearing-wall spacing; perimeter ties within 1.2 m of
the edge ≥ **71 kN** (Cl 16.2.5.1). Vertical ties in all wall panels, continuous
over the building height, ≥ **44 kN per horizontal metre** of wall, with at least
two per panel (Cl 16.2.5.2):

![[aci318-fig-r16.2.5-integrity-ties-large-panel-structures.png]]
*Fig. R16.2.5 — typical arrangement of integrity ties in large-panel structures:
transverse (T), longitudinal (L), vertical (V) and perimeter (P) ties (ACI
318M-19).*

`[code]` **Minimum bearing dimensions** (Cl 16.2.6), unless analysis or test shows
less is acceptable: from face of support to end of precast member, considering
tolerances, **solid/hollow-core slabs** the greater of `ℓ_n/180` and **50 mm**;
**beams/stemmed members** the greater of `ℓ_n/180` and **75 mm** (Table 16.2.6.2);
bearing pads next to unarmoured faces are set back at least **13 mm** (or the
chamfer dimension) from the support face and member end (Cl 16.2.6.3):

![[aci318-fig-r16.2.6-bearing-connection-dimensions.png]]
*Fig. R16.2.6 — bearing length on support: 13 mm minimum setback and not less than
the chamfer size; `ℓ_n/180 ≥ 50 mm` (slabs) or `75 mm` (beams) (ACI 318M-19).*

### Connections to foundations (Cl 16.3)

`[code]` Factored forces and moments at the base of columns, walls or pedestals
transfer to foundations by bearing on concrete and by reinforcement, dowels,
anchor bolts or mechanical connectors; the steel/connectors must transfer (a)
compression exceeding the lesser bearing strength (Cl 22.8) of the supported
member or foundation, and (b) any calculated tension across the interface
(Cl 16.3.1.1–16.3.1.2). A composite column with a structural steel core has its
steel base designed either for total member forces or for the core's share with
the remainder by concrete compression and reinforcement (Cl 16.3.1.3).

`[code]` Design strength `φS_n ≥ U` for flexure, shear, axial, torsion or bearing,
with combined moment/axial per Cl 22.4, bearing per Cl 22.8 and shear by
shear-friction Cl 22.9 or other appropriate means (Cl 16.3.3). Anchor bolts and
anchors for mechanical connections at precast bases follow Chapter 17 (with
erection forces considered), and mechanical connectors must reach design strength
before anchorage or surrounding-concrete failure (Cl 16.3.3.6–16.3.3.7).

`[code]` **Cast-in-place** column/pedestal-to-foundation reinforcement across the
interface is at least **0.005A_g** (of the supported member); wall-to-foundation
vertical steel meets Cl 11.6.1 (Cl 16.3.4); it's provided by extended longitudinal
bars or dowels, splices/connectors per Cl 10.7.5 (and Cl 18.13.2.2 if applicable),
and compression lap splices of No. 43/No. 57 bars in compression under all
combinations are permitted per Cl 25.5.5.3 (Cl 16.3.5). **Precast** bases satisfy
the vertical-tie rules of Cl 16.2.4.3/16.2.5.2; vertical wall ties may be
developed into a reinforced slab-on-ground if no base tension results
(Cl 16.3.6).

### Horizontal shear transfer in composite flexural members (Cl 16.4)

`[code]` Full horizontal shear transfer is provided across contact surfaces
(Cl 16.4.1.1); where tension acts across the interface, contact transfer is
permitted only with transverse reinforcement per Cl 16.4.6–16.4.7 (Cl 16.4.1.2);
the assumed surface preparation is specified in construction documents
(Cl 16.4.1.3). Design strength `φV_nh ≥ V_u` at all locations (Cl 16.4.3.1), or by
the alternative `φV_nh ≥ V_uh` with `V_uh` from the change in flexural
compressive/tensile force in any segment (Cl 16.4.5).

`[code]` If `V_u > φ(3.5 b_v d)`, `V_nh` is the shear-friction `V_n` of Cl 22.9
(Cl 16.4.4.1). Otherwise Table 16.4.4.2 applies (Cl 16.4.4.2):

![[aci318-table-16.4.4.2-nominal-horizontal-shear-strength.png]]
*Table 16.4.4.2 — nominal horizontal shear strength `V_nh` (N): with
`A_v ≥ A_v,min` and the surface intentionally roughened to ≈6 mm amplitude, the
lesser of `λ(1.8 + 0.6 A_v f_yt/(b_v s)) b_v d` and `3.5 b_v d`; with
`A_v ≥ A_v,min` on an unroughened surface, `0.55 b_v d`; other cases (roughened,
`A_v < A_v,min`), `0.55 b_v d` (ACI 318M-19).* `d` is measured from the extreme
compression fibre of the whole composite section to the centroid of longitudinal
tension steel (≥ `0.8h` for prestressed members) (Cl 16.4.4.3); transverse steel
in the earlier-cast section that extends into the new concrete and is anchored on
both sides of the interface may count as ties (Cl 16.4.4.4). Minimum interface ties
`A_v,min` is the greater of `0.062√f'c b_w s/f_y` and `0.35 b_w s/f_y`
(Cl 16.4.6.1); shear-transfer steel is single bars/wire, multiple-leg stirrups or
vertical legs of welded wire, at longitudinal spacing ≤ the lesser of **600 mm**
and **4×** the least dimension of the supported element, developed in both
elements per Cl 25.7.1 (Cl 16.4.7).

### Brackets and corbels (Cl 16.5)

`[code]` The Cl 16.5 method applies to brackets/corbels with shear span-to-depth
ratio `a_v/d ≤ 1.0` and factored restraint force `N_uc ≤ V_u` (Cl 16.5.1.1);
strut-and-tie design (Chapter 23) is permitted regardless of shear span
(Cl R16.5.1.1):

![[aci318-fig-r16.5.1a-structural-action-of-corbel.png]]
*Fig. R16.5.1(a) — structural action of a corbel: shear plane at the support face,
primary tension steel `φA_sc f_y`, restraint force `N_uc`, and a compression strut
from the load to the support (ACI 318M-19).*

![[aci318-fig-r16.5.1b-bracket-corbel-notation.png]]
*Fig. R16.5.1(b) — notation used in Cl 16.5: bearing plate, anchor bar, framing bar,
primary reinforcement `A_sc`, closed stirrups/ties `A_h` within `(2/3)d`, depth `d`,
overall depth `h`, shear span `a_v` (ACI 318M-19).*

`[code]` **Dimensional limits** (Cl 16.5.2): `d` at the support face; overall depth
at the outside bearing edge ≥ `0.5d`; no part of the bearing area projects beyond
the end of the straight primary tension steel or the inside face of any transverse
anchor bar; for normalweight concrete `V_u/φ` ≤ the least of `0.2f'c b_w d`,
`(3.3 + 0.08f'c) b_w d` and `11 b_w d`; lightweight concrete has its own
(lesser-of) limits `[0.2 − 0.07a_v/d]f'c b_w d` and `[5.5 − 1.9a_v/d] b_w d`.

`[code]` **Required and design strength** (Cl 16.5.3–16.5.4): the support-face
section is designed for `V_u`, `N_uc` and `M_u` **simultaneously**; `φN_n ≥ N_uc`
with `N_n = A_n f_y`, `φV_n ≥ V_u` with `V_n` from shear-friction (`A_vf`, Cl 22.9),
`φM_n ≥ M_u` from the Cl 22.2 assumptions (`A_f`). **Reinforcement limits**
(Cl 16.5.5): primary tension steel `A_sc` ≥ the greatest of `A_f + A_n`,
`(2/3)A_vf + A_n` and `0.04(f'c/f_y) b_w d`; closed stirrups/ties parallel to
primary steel `A_h ≥ 0.5(A_sc − A_n)`, distributed uniformly within `(2/3)d` from
the primary tension steel (Cl 16.5.6.6).

`[code]` **Detailing** (Cl 16.5.6): at the front face the primary tension steel is
anchored by (a) a weld to an equal-size transverse bar designed to develop `f_y`,
(b) bending back to form a horizontal loop, or (c) other means developing `f_y`;
it is developed at the support face, with development accounting for stress not
proportional to moment:

![[aci318-fig-r16.5.6.3a-member-dependent-on-support-anchorage.png]]
*Fig. R16.5.6.3(a) — member largely dependent on support and anchorages: standard
90°/180° hook development `ℓ_dh` (ACI 318M-19).*

![[aci318-fig-r16.5.6.3b-weld-details-mattock-tests.png]]
*Fig. R16.5.6.3(b) — weld details used in the Mattock et al. (1976a) tests: weld
length `ℓ_weld = (3/4)d_b`, throat `t_weld = d_b/2` between the primary bar and the
transverse anchor bar (ACI 318M-19).*

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-bearing-and-shear-friction]] — Cl 22.8/22.9 bearing and shear-friction.
- [[aci318-strut-and-tie-method]] — alternative design route for brackets/corbels.
- [[aci318-structural-system-requirements]] — precast system requirements
  (Cl 4.12.1), Table 4.10.2.1 integrity.
- [[aci318-anchoring-general-and-tensile-strength]],
  [[aci318-anchoring-shear-interaction-seismic-and-shear-lugs]] — Chapter 17.
- [[concrete-corbels-nibs-and-stepped-joints]],
  [[concrete-beam-longitudinal-shear-composite]],
  [[concrete-construction-prefabricated-structures]] — the AS 3600 equivalents,
  for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 16 Cl 16.1–16.5 (pp. 217–232),
  incl. Tables 16.2.6.2, 16.4.4.2 and Figs. R16.2.5, R16.2.6, R16.5.1a/b,
  R16.5.6.3a/b.
