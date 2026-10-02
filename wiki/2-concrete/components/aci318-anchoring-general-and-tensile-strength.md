---
title: ACI 318M-19 anchoring to concrete — scope, general design, φ factors, tensile strength modes
category: 2-concrete
tags: [aci, anchors, anchoring, tension, breakout, pullout, bond, adhesive-anchors]
standards: [ACI 318M-19 Cl 17.1, ACI 318M-19 Cl 17.2, ACI 318M-19 Cl 17.3, ACI 318M-19 Cl 17.4, ACI 318M-19 Cl 17.5, ACI 318M-19 Cl 17.6]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 anchoring to concrete — general and tension

> Scope: ACI 318M-19 Cl 17.1–17.6 — which anchors and loading the chapter covers,
> general design requirements, design limits, the failure-mode design-strength
> framework with its strength reduction factors, and the tensile strength
> models (steel, concrete breakout, pullout, side-face blowout, adhesive bond).
> Shear, interaction, spacing/edge distances, seismic and shear-lug provisions
> are on [[aci318-anchoring-shear-interaction-seismic-and-shear-lugs]]. This is an
> **ACI 318M-19 page, kept separate from the AS 3600:2018 concept pages**
> elsewhere in `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Chapter 17 designs anchors that transmit tension, shear, or both between
(a) connected structural elements or (b) safety-related attachments and
structural elements; safety levels are for **in-service** conditions, not
short-term handling or construction (Cl 17.1.1). Covered types: headed studs and
headed bolts (pullout in uncracked concrete ≥ `1.4N_p`), hooked bolts (≥ `1.4N_p`
without friction), post-installed expansion (torque- and displacement-controlled)
and undercut anchors meeting **ACI 355.2**, post-installed adhesive anchors
meeting **ACI 355.4M**, post-installed screw anchors meeting ACI 355.2, and
attachments with shear lugs (Cl 17.1.2). Removal and resetting of post-installed
mechanical anchors is **prohibited** (Cl 17.1.3). **Not covered**: predominantly
high-cycle fatigue or impact loading (Cl 17.1.4); specialty inserts, through-bolts,
multiple anchors connected to a single plate at the embedded end, grouted anchors,
power-driven (powder/pneumatic) fasteners (Cl 17.1.5). Reinforcement used as
anchorage follows development rules elsewhere, with concrete breakout considered
or anchor reinforcement per Cl 17.5.2.1 provided (Cl 17.1.6).

## Detail

### General (Cl 17.2) and design limits (Cl 17.3)

`[code]` Anchors and groups are designed for critical effects of factored loads
from **elastic analysis** (plastic analysis only if nominal strength is controlled
by ductile steel and deformation compatibility is considered) (Cl 17.2.1). Group
effects apply where two or more anchors loaded by a common element are spaced
closer than that for unreduced breakout; adjacent anchors not loaded by a common
element are checked for simultaneous maximum loading (Cl 17.2.1.1). Adhesive
anchors are installed in concrete aged ≥ **21 days**, and qualified per ACI 355.4M
for installation direction if horizontal or upwardly inclined (Cl 17.2.2–17.2.3).
Installation and inspection follow Cl 26.7 and 26.13 (Cl 17.2.5).

`[code]` **Lightweight concrete factor `λ_a`** (Table 17.2.4.1, Cl 17.2.4.1):
`1.0λ` for cast-in and undercut anchor concrete failure; `0.8λ` for expansion,
screw and adhesive anchor concrete failure; `0.6λ` for adhesive anchor bond failure
(Eq. 17.6.5.2.1), where `λ` per Cl 19.2.4; an alternative may be established by
ACI 355.2/355.4M tests.

`[code]` **Design limits** (Cl 17.3): `f'c` used in this chapter ≤ **70 MPa**
(cast-in) and **55 MPa** (post-installed), and post-installed anchors aren't used
in concrete above 55 MPa without verifying tests (Cl 17.3.1). For anchors with
`d_a ≤ 100 mm`, breakout requirements are satisfied by the Cl 17.6.2 and 17.7.2
procedures (Cl 17.3.2); adhesive anchors with `4d_a ≤ h_ef ≤ 20d_a` are covered by
Cl 17.6.5 (Cl 17.3.3); screw anchors with `5d_a ≤ h_ef ≤ 10d_a` and `h_ef ≥ 40 mm`
by Cl 17.6.2/17.7.2 (Cl 17.3.4). Anchors must meet the spacing, edge distance and
thickness limits of Cl 17.9 unless supplementary reinforcement controls splitting
(Cl 17.3.5).

### Required and design strength framework (Cl 17.4–17.5)

`[code]` Required strength from Chapter 5 (Cl 17.4.1); anchors in SDC C–F also
satisfy Cl 17.10 (Cl 17.4.2). Design strength `φS_n ≥ U` for each anchor and group
with tension–shear interaction per Cl 17.8 (Cl 17.5.1). Nominal strengths must come
from models in substantial agreement with comprehensive tests, using the **5%
fractile** of basic single-anchor strength, with concrete-related strengths
modified for size effect, number of anchors, close spacing, edge proximity, member
depth, eccentric loading and cracking (Cl 17.5.1.2). The failure modes to be
designed against:

![[aci318-fig-r17.5.1.2-anchor-failure-modes.png]]
*Fig. R17.5.1.2 — failure modes for anchors. Tension: (i) steel failure,
(ii) pullout, (iii) concrete breakout, (iv) concrete splitting, (v) side-face
blowout, (vi) bond failure (single/group). Shear: (i) steel failure preceded by
concrete spall, (ii) concrete pryout for anchors far from a free edge,
(iii) concrete breakout (ACI 318M-19).*

`[code]` **Critical spacing for group effects** (Table 17.5.1.3.1): concrete
breakout in tension `3h_ef`; bond strength in tension `2c_Na`; concrete breakout
in shear `3c_a1` — only anchors susceptible to the failure mode in question count
toward the group (Cl 17.5.1.3.1). Strength may instead be test-based using the 5%
fractile (Cl 17.5.1.4).

`[code]` Each failure mode is checked by `φN ≥ N_ua` / `φV ≥ V_ua` (single anchor)
or `φN_g ≥ N_ua,g` (group; steel and pullout use the **most highly stressed**
anchor) for: steel in tension, concrete breakout in tension, pullout, side-face
blowout, adhesive bond, steel in shear, concrete breakout in shear and pryout in
shear (Table 17.5.2, Cl 17.5.2). **Anchor reinforcement** may replace the concrete
breakout strength if developed per Chapter 25 on both sides of the breakout
surface (tension), or — for shear — developed on both sides or enclosing and
contacting the anchor and developed beyond the breakout surface (Cl 17.5.2.1);
its φ is **0.75**.

`[code]` **Sustained tension on adhesive anchors**: `0.55φN_ba ≥ N_ua,s`
(Eq. 17.5.2.2, `N_ba` = basic bond strength, `N_ua,s` = factored sustained tension)
for the anchor taking the highest sustained tension (Cl 17.5.2.2).

`[code]` **Strength reduction factors φ** (Cl 17.5.3):

![[aci318-table-17.5.3a-phi-anchor-steel-strength.png]]
*Table 17.5.3(a) — steel-governed: ductile 0.75 tension / 0.65 shear; brittle
0.65 / 0.60 (ACI 318M-19).*

![[aci318-table-17.5.3b-phi-anchor-concrete-breakout-bond-blowout.png]]
*Table 17.5.3(b) — concrete breakout, bond, side-face blowout (tension) and
breakout (shear): with supplementary reinforcement cast-in 0.75, post-installed
Category 1/2/3 = 0.75/0.65/0.55 (tension), shear 0.75; without supplementary
reinforcement cast-in 0.70, Category 1/2/3 = 0.65/0.55/0.45, shear 0.70 (ACI
318M-19).*

![[aci318-table-17.5.3c-phi-anchor-pullout-pryout.png]]
*Table 17.5.3(c) — concrete pullout (tension) and pryout (shear): cast-in 0.70;
post-installed Category 1/2/3 = 0.65/0.55/0.45 for pullout, pryout 0.70
(ACI 318M-19).* `[derived]` Anchor Category 1 = low installation sensitivity and
high reliability, 2 = medium, 3 = high sensitivity and lower reliability (Table
17.5.3 note), per the ACI 355.2/355.4M product evaluation.

### Steel strength in tension (Cl 17.6.1)

`[code]` `N_sa = A_se,N f_uta` (Eq. 17.6.1.2), with `f_uta` not exceeding
`1.9f_ya` or **860 MPa**.

### Concrete breakout strength in tension (Cl 17.6.2)

`[code]` Single anchor `N_cb = (A_Nc/A_Nco) ψ_ed,N ψ_c,N ψ_cp,N N_b`
(Eq. 17.6.2.1a); group `N_cbg = (A_Nc/A_Nco) ψ_ec,N ψ_ed,N ψ_c,N ψ_cp,N N_b`
(Eq. 17.6.2.1b). `A_Nco = 9h_ef²` is the projected failure area of a single anchor
with edge distance ≥ `1.5h_ef`; `A_Nc` projects the failure surface `1.5h_ef` out
from the anchor centreline(s) and may not exceed `nA_Nco`:

![[aci318-fig-r17.6.2.1-tension-breakout-projected-area.png]]
*Fig. R17.6.2.1 — (a) the ≈35° breakout cone and `A_Nco = (2×1.5h_ef)² = 9h_ef²`,
critical edge distance `1.5h_ef`; (b) `A_Nc` for single anchors and groups near
edges (ACI 318M-19).* If anchors lie within `1.5h_ef` of three or more edges, `h_ef`
is replaced by the greater of `c_a,max/1.5` and `s/3` (Cl 17.6.2.1.2); a plate or
washer may enlarge the projected area within limits (Cl 17.6.2.1.3).

`[code]` **Basic strength** `N_b = k_c λ_a √f'c h_ef^1.5` (Eq. 17.6.2.2.1),
`k_c = 10` cast-in, `7` post-installed (up to 24 from product tests); for cast-in
headed studs/bolts with `280 ≤ h_ef ≤ 635 mm`, `N_b = 3.9λ_a√f'c h_ef^(5/3)`
(Eq. 17.6.2.2.3).

`[code]` **Modification factors**: eccentricity `ψ_ec,N = 1/(1 + 2e'_N/(3h_ef)) ≤ 1`
(Eq. 17.6.2.3.1, each orthogonal axis separately); edge `ψ_ed,N = 1.0` if
`c_a,min ≥ 1.5h_ef`, else `0.7 + 0.3 c_a,min/(1.5h_ef)`; cracking `ψ_c,N = 1.25`
(cast-in) or `1.4` (post-installed, `k_c = 7`) in uncracked regions, `1.0` where
cracked; splitting `ψ_cp,N = 1.0` for cast-in or if `c_a,min ≥ c_ac`, else
`c_a,min/c_ac ≥ 1.5h_ef/c_ac` for post-installed anchors designed for uncracked
concrete without splitting reinforcement (Cl 17.6.2.3–17.6.2.6). Post-installed
anchors in cracked regions must be qualified for cracked concrete, with cracking
controlled per Cl 24.3.2 or equivalent confinement (Cl 17.6.2.5.2).

### Pullout strength (Cl 17.6.3)

`[code]` `N_pn = ψ_c,P N_p` (Eq. 17.6.3.1), `ψ_c,P = 1.4` in uncracked regions,
`1.0` in cracked. For post-installed expansion, screw and undercut anchors `N_p`
comes from ACI 355.2 test fractiles and **may not be calculated**; for cast-in
headed studs/bolts `N_p = 8A_brg f'c` (Eq. 17.6.3.2.2a); for J-/L-bolts
`N_p = 0.9f'c e_h d_a` with `3d_a ≤ e_h ≤ 4.5d_a` (Eq. 17.6.3.2.2b).

### Side-face blowout (Cl 17.6.4)

`[code]` For a single headed anchor with deep embedment close to an edge
(`h_ef > 2.5c_a1`): `N_sb = 13c_a1√A_brg λ_a√f'c` (Eq. 17.6.4.1), multiplied by
`(1 + c_a2/c_a1)/4` if `c_a2 < 3c_a1` (`1 ≤ c_a2/c_a1 ≤ 3`); for groups with
spacing `s < 6c_a1`: `N_sbg = (1 + s/(6c_a1)) N_sb` (Eq. 17.6.4.2).

### Bond strength of adhesive anchors (Cl 17.6.5)

`[code]` Single: `N_a = (A_Na/A_Nao) ψ_ed,Na ψ_cp,Na N_ba` (Eq. 17.6.5.1a); group:
`N_ag = (A_Na/A_Nao) ψ_ec,Na ψ_ed,Na ψ_cp,Na N_ba` (Eq. 17.6.5.1b). Influence
area `A_Nao = (2c_Na)²` with `c_Na = 10d_a√(τ_uncr/7.6)` (7.6 carries MPa units);
basic bond strength `N_ba = λ_a τ_cr π d_a h_ef` (Eq. 17.6.5.2.1) with `τ_cr`
the 5% fractile characteristic bond stress from ACI 355.4M tests (`τ_uncr` may be
used where analysis shows no cracking at service load). Where no test data are
used, the minimum characteristic bond stresses of Table 17.6.5.2.5 are permitted,
provided ACI 355.4M compliance, rotary-impact or rock drilled holes, concrete
`f'c ≥ 17 MPa`, age ≥ 21 days and temperature ≥ 10 °C at installation:

![[aci318-table-17.6.5.2.5-min-characteristic-bond-stress.png]]
*Table 17.6.5.2.5 — minimum characteristic bond stresses: outdoor (dry to fully
saturated, peak concrete temperature 79 °C) `τ_cr` 1.4 / `τ_uncr` 4.5 MPa; indoor
(dry, 43 °C) 2.1 / 7.0 MPa; multiply by 0.4 for sustained tension, and by 0.8 (`τ_cr`)
/ 0.4 (`τ_uncr`) for seismic design in SDC C–F (ACI 318M-19).*

`[code]` Bond factors: `ψ_ec,Na = 1/(1 + e'_N/c_Na) ≤ 1`; `ψ_ed,Na = 1.0` if
`c_a,min ≥ c_Na`, else `0.7 + 0.3 c_a,min/c_Na`; `ψ_cp,Na = 1.0` if `c_a,min ≥ c_ac`,
else `c_a,min/c_ac ≥ c_Na/c_ac`, only for anchors designed for uncracked concrete
without splitting reinforcement (Cl 17.6.5.3–17.6.5.5). Adhesive anchors in
cracked regions must be qualified for cracked concrete per ACI 355.4M
(Cl 17.6.5.2.3).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-anchoring-shear-interaction-seismic-and-shear-lugs]] — Cl 17.7–17.11.
- [[aci318-connections-between-members]] — precast base connections that invoke
  Chapter 17.
- [[aci318-serviceability-deflection-and-cracking]] — Cl 24.3.2 crack control
  referenced for post-installed anchors.
- [[concrete-joints-embedded-items-and-fixings]] — the AS 3600 equivalent
  treatment of embedded items and fixings, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 17 Cl 17.1–17.6 (pp. 233–260),
  incl. Tables 17.5.3(a)–(c), 17.6.5.2.5 and Figs. R17.5.1.2, R17.6.2.1.
