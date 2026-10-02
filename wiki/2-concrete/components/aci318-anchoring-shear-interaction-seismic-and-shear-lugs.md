---
title: ACI 318M-19 anchoring to concrete — shear strength, interaction, edge distances, seismic design and shear lugs
category: 2-concrete
tags: [aci, anchors, anchoring, shear, interaction, seismic, shear-lugs]
standards: [ACI 318M-19 Cl 17.7, ACI 318M-19 Cl 17.8, ACI 318M-19 Cl 17.9, ACI 318M-19 Cl 17.10, ACI 318M-19 Cl 17.11]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 anchoring to concrete — shear, interaction, seismic and shear lugs

> Scope: ACI 318M-19 Cl 17.7 (shear strength: steel, concrete breakout, pryout),
> 17.8 (tension–shear interaction), 17.9 (spacing, edge distances and thicknesses
> to preclude splitting), 17.10 (earthquake-resistant anchor design) and 17.11
> (attachments with shear lugs). Scope, φ factors and tension modes are on
> [[aci318-anchoring-general-and-tensile-strength]]. This is an **ACI 318M-19
> page, kept separate from the AS 3600:2018 concept pages** elsewhere in
> `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Anchor shear is checked for three modes — steel failure, concrete breakout
near an edge, and concrete pryout away from one (Cl 17.7; Table 17.5.2) — then
combined with tension by a trilinear interaction rule (Cl 17.8). Anchors in
SDC C, D, E or F carry extra requirements (Cl 17.10), and attachments with shear
lugs have their own bearing/breakout checks (Cl 17.11).

## Detail

### Steel strength in shear (Cl 17.7.1)

`[code]` `V_sa` depends on anchor type (Cl 17.7.1.2), with `f_uta ≤ 1.9f_ya` and
**860 MPa**: cast-in **headed stud** `V_sa = A_se,V f_uta` (Eq. 17.7.1.2a);
cast-in **headed/hooked bolts** and post-installed anchors whose sleeves don't
extend through the shear plane `V_sa = 0.6A_se,V f_uta` (Eq. 17.7.1.2b);
post-installed anchors with sleeves through the shear plane use ACI 355.2 test
fractiles or Eq. 17.7.1.2b. Anchors with a **built-up grout pad** have `V_sa`
multiplied by **0.80** (Cl 17.7.1.2.1).

### Concrete breakout strength in shear (Cl 17.7.2)

`[code]` Shear perpendicular to the edge: single `V_cb = (A_Vc/A_Vco) ψ_ed,V ψ_c,V
ψ_h,V V_b` (Eq. 17.7.2.1a); group `V_cbg = (A_Vc/A_Vco) ψ_ec,V ψ_ed,V ψ_c,V ψ_h,V
V_b` (Eq. 17.7.2.1b). Shear **parallel** to an edge may take twice the perpendicular
value with `ψ_ed,V = 1.0`; anchors at a **corner** are checked per edge and the
lesser governs (Cl 17.7.2.1(c)–(d)). `A_Vco = 4.5c_a1²` (Eq. 17.7.2.1.3) — the base
of a half-pyramid `3c_a1` long and `1.5c_a1` deep; `A_Vc` is the projected failure
area on the member side face, not exceeding `nA_Vco`:

![[aci318-fig-r17.7.2.1b-shear-breakout-projected-area.png]]
*Fig. R17.7.2.1(b) — calculation of `A_Vc` for single anchors and groups: the
`ha < 1.5c_a1` thin-member cases, spacing `s_1 < 3c_a1`, and Cases 1–3 for anchors
at different distances from the edge (half the shear on the front anchor, all the
shear on the rear anchor, or all on the front anchor if `s < c_a1,1`) (ACI
318M-19).* In narrow, thin members where both `c_a2` and `h_a` are `< 1.5c_a1`, the
`c_a1` used throughout is limited to the greatest of `c_a2,max/1.5`, `h_a/1.5` and
`s/3` (Cl 17.7.2.1.2; worked example Fig. R17.7.2.1.2).

`[code]` **Basic strength** `V_b` ≤ the lesser of `0.6(ℓ_e/d_a)^0.2 √d_a λ_a √f'c
c_a1^1.5` (Eq. 17.7.2.2.1a) and `3.7λ_a√f'c c_a1^1.5` (Eq. 17.7.2.2.1b), where
`ℓ_e = h_ef` for constant-stiffness anchors, `2d_a` for torque-controlled expansion
anchors with a distance sleeve, and `ℓ_e ≤ 8d_a` always. For cast-in headed
studs/bolts continuously welded to a steel attachment (thickness ≥ the greater of
`0.5d_a` and 10 mm, spacing ≥ 65 mm, corner reinforcement if `c_a2 ≤ 1.5h_ef`, and
group strength based on the row farthest from the edge) the `0.6` becomes `0.66`
(Eq. 17.7.2.2.2).

`[code]` **Factors**: eccentricity `ψ_ec,V = 1/(1 + 2e'_V/(3c_a1)) ≤ 1`; edge
`ψ_ed,V = 1.0` if `c_a2 ≥ 1.5c_a1`, else `0.7 + 0.3 c_a2/(1.5c_a1)` (using the lesser
`c_a2`); cracking `ψ_c,V = 1.4` in uncracked regions, otherwise per Table 17.7.2.5.1
— `1.0` (no supplementary steel, or edge bar smaller than No. 13), `1.2` (≥ No. 13
bar between anchor and edge), `1.4` (same, enclosed in stirrups at ≤ 100 mm);
member-thickness `ψ_h,V = √(1.5c_a1/h_a) ≥ 1.0` where `h_a < 1.5c_a1`
(Cl 17.7.2.3–17.7.2.6).

### Pryout strength in shear (Cl 17.7.3)

`[code]` `V_cp = k_cp N_cp` (single) and `V_cpg = k_cp N_cpg` (group), with
`k_cp = 1.0` for `h_ef < 65 mm` and `2.0` for `h_ef ≥ 65 mm`. `N_cp` is the
tension breakout `N_cb` (Eq. 17.6.2.1a) for cast-in and post-installed mechanical
anchors; for adhesive anchors, the lesser of bond `N_a` and breakout `N_cb`
(groups: `N_ag`/`N_cbg`) (Cl 17.7.3.1).

### Tension and shear interaction (Cl 17.8)

`[code]` Interaction may be neglected if either `N_ua/(φN_n) ≤ 0.2` or
`V_ua/(φV_n) ≤ 0.2`; if both exceed 0.2, then
`N_ua/(φN_n) + V_ua/(φV_n) ≤ 1.2` (Eq. 17.8.3) — `φN_n`/`φV_n` being the governing
tension and shear strengths (Cl 17.8.2–17.8.3):

![[aci318-fig-r17.8-tension-shear-interaction.png]]
*Fig. R17.8 — trilinear interaction approach (solid) against the
`(N_ua/φN_n)^(5/3) + (V_ua/φV_n)^(5/3) = 1` curve (dashed): flat to
`0.2φV_n`, a straight line to `(φV_n, 0.2φN_n)`, then vertical (ACI 318M-19).*

### Edge distances, spacings and thicknesses (Cl 17.9)

`[code]` Unless supplementary reinforcement controls splitting (or product-specific
ACI 355.2/355.4M tests allow less), spacing and edge distances follow Table 17.9.2(a)
(Cl 17.9.1–17.9.2):

![[aci318-table-17.9.2a-min-spacing-edge-distance.png]]
*Table 17.9.2(a) — minimum anchor spacing: cast-in not torqued `4d_a`, torqued
`6d_a`; post-installed expansion/undercut `6d_a`; screw the greater of `0.6h_ef` and
`6d_a`. Minimum edge distance: cast-in per Cl 20.5.1.3 cover (torqued `6d_a`);
post-installed the greatest of cover, twice the maximum aggregate size, and the
ACI 355 / Table 17.9.2(b) value (ACI 318M-19).* In the absence of product data
Table 17.9.2(b) gives minimum edge distances of `8d_a` (torque-controlled), `10d_a`
(displacement-controlled), `6d_a` (screw, undercut, adhesive). Where installation
causes no splitting force and the anchor won't be torqued, a reduced `d_a'` may be
substituted if forces are limited to those for that smaller diameter (Cl 17.9.3).
`h_ef` of post-installed expansion, screw or undercut anchors is not more than the
greater of `2/3` of member thickness `h_a` and `h_a − 100 mm` unless tested
(Cl 17.9.4). **Critical edge distance** `c_ac` (Table 17.9.5): `4h_ef` for
torque-controlled, displacement-controlled and screw anchors; `2.5h_ef` undercut;
`2h_ef` adhesive.

### Earthquake-resistant anchor design (Cl 17.10)

`[code]` Applies to anchors in **SDC C, D, E or F** (Cl 17.10.1); the chapter does
**not** apply to anchors in plastic hinge zones (Cl 17.10.2). Post-installed anchors
must be qualified for seismic forces per ACI 355.2/355.4M, with `N_p`, `V_sa` (and,
for adhesive anchors, `τ_uncr`, `τ_cr`) based on the Simulated Seismic Tests
(Cl 17.10.3); anchor reinforcement is deformed bar per Cl 20.2.2 (Cl 17.10.4).

`[code]` **Tension**: if the earthquake tensile component of the strength-level
force is **≤ 20%** of the total factored anchor tension in the same combination,
design by Cl 17.6 and Table 17.5.2 as usual (Cl 17.10.5.1). Otherwise the anchor
and attachment satisfy one of (Cl 17.10.5.2–17.10.5.3): (a) **ductile anchor
steel governs** — concrete-governed strength exceeds steel strength taken as
`1.2 ×` nominal, anchors transmit tension through a ductile steel element with a
**stretch length ≥ 8d_a** (Fig. R17.10.5.3), buckling protection under load
reversal, `f_uta/f_ya ≥ 1.3` for threaded connections unless upset, and deformed
bars to Cl 20.2.2; (b) design for the maximum tension from a ductile yield
mechanism in the attachment (with overstrength and strain hardening); (c) the
maximum tension from a non-yielding attachment; or (d) the maximum tension from
combinations with `E_h` increased by **Ω_o**. In (b)–(d) the design strength per
Cl 17.10.5.4 uses `φN_sa` and **0.75** × `φN_cb`/`φN_cbg`, `φN_pn`, `φN_sb`/`φN_sbg`,
`φN_a`/`φN_ag` assuming cracked concrete unless shown uncracked (no reduction if
anchor reinforcement per Cl 17.5.2.1(a) is provided, Cl 17.10.5.5):

![[aci318-fig-r17.10.5.3-stretch-length.png]]
*Fig. R17.10.5.3 — illustrations of stretch length: (a) anchor chair, (b) sleeve
(ACI 318M-19).*

`[code]` **Shear**: if the earthquake shear component is ≤ 20% of the total factored
shear, design by Cl 17.7 and Table 17.5.2 (Cl 17.10.6.1); otherwise one of the same
three alternatives (ductile attachment yield, non-yielding attachment, or `E_h × Ω_o`)
(Cl 17.10.6.2–17.10.6.3), with no further reduction if shear anchor reinforcement
per Cl 17.5.2.1(b) is provided (Cl 17.10.6.4). Combined tension and shear use
Cl 17.8 with the Cl 17.10.5.4 tension strength (Cl 17.10.7.1).

### Attachments with shear lugs (Cl 17.11)

`[code]` Shear lugs are rectangular plates (or plate-element shapes) welded to the
base plate; the design route of Cl 17.11.1.1.1–17.11.1.1.9 or alternative methods
justified by analysis/test is permitted:

![[aci318-fig-r17.11.1.1a-attachments-with-shear-lugs.png]]
*Fig. R17.11.1.1(a) — examples of attachments with shear lugs: (a) cast-in-place
and (b) post-installed (with grout and inspection/vent holes); lug depth `h_sl`,
embedment `h_ef`, edge distance `c_sl` (ACI 318M-19).*

`[code]` Requirements (Cl 17.11.1.1): at least **four anchors** meeting Chapter 17
(excluding the shear-mode checks of Cl 17.5.1.2(f)–(h)); tension–shear interaction
(Cl 17.8) includes the share of shear on welded anchors; bearing strength in shear
`φV_brg,sl ≥ V_u` and lug concrete breakout `φV_cb,sl ≥ V_u`, both with **φ = 0.65**;
for anchors in tension `h_ef/h_sl ≥ 2.5` and `h_ef/c_sl ≥ 2.5`; the moment from the
bearing-reaction/shear couple is included in anchor tension design; horizontally
installed base plates have a **25 mm** minimum hole along each long lug side.
**Bearing**: `V_brg,sl = 1.7f'c A_ef,sl ψ_brg,sl` (Eq. 17.11.2.1), `A_ef,sl` the
bearing area below the concrete surface perpendicular to shear (lug area within
`2t_sl` of the base-plate bottom/concrete surface/stiffener interface, plus
stiffener leading-edge area); `ψ_brg,sl = 1 + P_u/(nN_sa) ≤ 1.0` (axial tension,
Cl 17.11.2.2.1a), `1` (none), or `1 + 4P_u/(A_bp f'c) ≤ 2.0` (axial compression);
stiffener length in the shear direction ≥ `0.5h_sl`; multiple lugs add only if the
shear stress on the concrete plane between them ≤ `0.2f'c`. **Breakout**: `V_cb,sl`
from Eq. 17.7.2.1a with `V_b` from Eq. 17.7.2.2.1b and `c_a1` measured from the lug
bearing face to the free edge; `A_vc` projects `1.5c_a1` horizontally and vertically
excluding `A_ef,sl`; parallel-to-edge, corner and multi-lug cases follow Cl 17.11.3.

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-anchoring-general-and-tensile-strength]] — Cl 17.1–17.6.
- [[aci318-connections-between-members]] — precast connection anchors.
- [[aci318-structural-system-requirements]] — Cl 4.4.6 seismic design category
  routing (SDC C–F) that triggers Cl 17.10.
- [[concrete-joints-embedded-items-and-fixings]] — the AS 3600 equivalent, for
  structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 17 Cl 17.7–17.11 (pp. 261–283),
  incl. Tables 17.7.2.5.1, 17.9.2(a)/(b), 17.9.5 and Figs. R17.7.2.1b, R17.8,
  R17.10.5.3, R17.11.1.1a.
