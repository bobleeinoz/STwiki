---
title: Combined actions — member capacity (in-plane, out-of-plane, biaxial)
category: 0-standards
tags: [combined-actions, member-capacity, in-plane, out-of-plane, biaxial-bending, single-angle-truss-member, beam-column]
standards: [AS 4100:2020 Cl 8.4]
status: draft
reviewed: 2026-09-13
---

# Combined actions — member capacity

> Scope: AS 4100:2020 Cl 8.4 — beam-column member (buckling) capacity:
> in-plane capacity for elastically (8.4.2) and plastically (8.4.3)
> analysed members, out-of-plane capacity (8.4.4), biaxial bending member
> capacity (8.4.5), and eccentrically loaded single angles in trusses
> (8.4.6). Section capacity is on
> [[as4100-combined-actions-section-capacity]].

## Summary

`[code]` Routing (Cl 8.4.1): (a) bending about the x-axis with sufficient
restraint to prevent lateral buckling, or about the y-axis only — in-plane
only (Cl 8.4.2 elastic or 8.4.3 plastic); (b) bending about the x-axis with
**insufficient** restraint — both in-plane (8.4.2) **and** out-of-plane
(8.4.4); (c) non-principal-axis or biaxial bending — Cl 8.4.5.

## Detail

### In-plane capacity — elastic analysis (Cl 8.4.2)

`[code]` Applies to a member analysed elastically (Cl 4.4) or in a
statically determinate structure (8.4.2.1).

`[code]` **Compression members** (8.4.2.2): `M* ≤ φM_i`,
`M_i = M_s(1 − N*/φN_c) `, with `N_c` per Cl 6.3 for buckling about the
**same** principal axis as `M*`, using `k_e = 1.0` for both braced and sway
members unless a lower value is calculated for braced members from
Cl 4.6.3.2, 4.6.3.3 or 4.6.3.5 (subject to Cl 6.1 being satisfied for `N_c`
with that `l_e`).

`[code]` Alternative for compact doubly symmetric I-sections and compact
RHS/SHS with `k_f = 1.0`:

`M_i = M_s { [1 − ((1+β_m)/2)³](1 − N*/φN_c) + 1.18((1+β_m)/2)³ sqrt(1 − N*/φN_c) } ≤ M_rx or M_ry`

`β_m` = ratio of smaller to larger end moment (positive in reverse
curvature), or the Cl 4.4.2.2 value for members with transverse load.

`[code]` **Tension members** (8.4.2.3): satisfy Cl 8.3 (section capacity) —
no separate member buckling check (a tension member doesn't buckle
in-plane).

### In-plane capacity — plastic analysis (Cl 8.4.3)

`[code]` Applies only to **compact doubly symmetric I-sections**, for
members assumed to contain a plastic hinge in a plastically analysed frame
(8.4.3.1).

`[code]` **Member slenderness** (8.4.3.2) — `N*` in every plastic-hinge
member must satisfy:

`N*/φN_s ≤ [(0.60 + 0.40β_m)/sqrt(N_s/N_ol)]²` when `N*/φN_s ≤ 0.15`

`N*/φN_s ≤ [1 + β_m − sqrt(N_s/N_ol)] / [1 + β_m + sqrt(N_s/N_ol)]` when `N*/φN_s > 0.15`

with `N_ol = π²EI/l²` (`I` about the axis of the design moment, `l` = actual
member length). A member exceeding these limits must not contain a plastic
hinge (though it may still be designed elastically per Cl 8.4.2 within the
plastically analysed structure).

`[code]` **Web slenderness** (8.4.3.3) — `N*` in every plastic-hinge member
must also satisfy, by web slenderness band (`d_1/t · sqrt(f_y/250)`):

| Band | Limit on N*/φN_s |
|---|---|
| `45 ≤ d_1/t·sqrt(f_y/250) ≤ 82` | `≤ 0.60 − [d_1/t·sqrt(f_y/250)]/137` |
| `25 < d_1/t·sqrt(f_y/250) < 45` | `≤ 1.91 − [d_1/t·sqrt(f_y/250)]/27.4 ≤ 1.0` |
| `0 ≤ d_1/t·sqrt(f_y/250) ≤ 25` | `≤ 1.0` |

A member with `d_1/t·sqrt(f_y/250) > 82` must not contain a plastic hinge
(may still be designed elastically per Cl 8.4.2).

`[code]` **Plastic moment capacity reduced for axial force** (8.4.3.4):
`φM_prx = 1.18 φM_sx (1 − N*/φN_s) ≤ φM_sx` (major axis);
`φM_pry = 1.19 φM_sy [1 − (N*/φN_s)²] ≤ φM_sy` (minor axis).

### Out-of-plane capacity (Cl 8.4.4)

`[code]` **Compression members** (8.4.4.1): `M*_x ≤ φM_ox`,
`M_ox = M_bx(1 − N*/φN_cy)`, with `M_bx` = nominal member moment capacity
without full lateral restraint (Cl 5.6) using an `α_m` matching the actual
`M*_x` distribution, and `N_cy` = member axial capacity for buckling about
the **minor** principal y-axis (Cl 6.3).

`[code]` Alternative, members without transverse load, compact doubly
symmetric I-section, F/P at both ends, `k_f = 1.0`:

`M_ox = α_bc M_bxo sqrt[(1 − N*/φN_cy)(1 − N*/φN_oz)] ≤ M_rx`

`1/α_bc = (1−β_m)/2 + [(1+β_m)/2]³ (0.4 − 0.23 N*/φN_cy)`

with `M_bxo` = member moment capacity with uniform moment (`α_m = 1`,
Cl 5.6), `N_oz` = elastic torsional buckling capacity:

`N_oz = [GJ + π²EI_w/l_z²] / [(I_x + I_y)/A]`

(`l_z` = distance between torsional restraints; section constants per
App H).

`[code]` **Tension members** (8.4.4.2): `M*_x ≤ φM_ox`,
`M_ox = M_bx(1 + N*/φN_t) ≤ M_rx` — note the **plus** sign: axial tension
*increases* the out-of-plane (lateral-torsional buckling) capacity by
straightening the member, unlike compression which reduces it.

### Biaxial bending capacity (Cl 8.4.5)

`[code]` **Compression members** (8.4.5.1), A1 amendment:

`(M*_x/φM_cx)^1.4 + (M*_y/φM_iy)^1.4 ≤ 1`

`M_cx` = lesser of `M_ix` (in-plane, Cl 8.4.2) and `M_ox` (out-of-plane,
Cl 8.4.4) for the major axis; `M_iy` = in-plane capacity for the minor axis
(Cl 8.4.2).

`[code]` **Tension members** (8.4.5.2), A1 amendment:

`(M*_x/φM_tx)^1.4 + (M*_y/φM_ry)^1.4 ≤ 1`

`M_tx` = lesser of `M_rx` (Cl 8.3.2) and `M_ox` (Cl 8.4.4.2); `M_ry` per
Cl 8.3.3.

### Eccentrically loaded single angles in trusses (Cl 8.4.6, A1)

`[code]` Single-angle web compression members connected by ≥ 2 bolts or
welded at both ends, loaded through one leg (Figure 8.4.6), satisfy Cl 8.3
and either Cl 8.4.5 or:

`N*/φN_ch + M*_h/(φM_bx cos α) ≤ 1`

- `N_ch` = member axial compression capacity (Cl 6.3) buckling about the
  rectangular h-axis parallel to the loaded leg, with `l_e = l`.
- `M_bx` = member moment capacity without full lateral restraint (Cl 5.6),
  bent about the major principal x-axis, `α_m` matching the actual moment
  distribution.
- `α` = angle between the x- and h-axes.
- For **equal-leg angles** with `l/t ≤ (210 + 175β_m)(250/f_y)`
  (the Cl 5.3.2.4 angle length limit), `M_bx` may be taken as `M_sx`.
- For other equal-leg angles, `M_bx` may use `M_o = (525t/l)(250/f_y) M_s`
  in Cl 5.6.1.1.
- `M*_h` = design end moment about the h-axis, from a rational elastic
  truss analysis or taken as ≥ `N*e`, with eccentricity
  `e = c_h − t/2` (angles on the same side of the truss chord) or
  `e = e_c + e_t` (angles on opposite sides), per Figure 8.4.6.

![[as4100-fig-8.4.6-single-angles-loaded-through-one-leg.png]]
*Figure 8.4.6 — single angles loaded through one leg: (a) angles on same side of chord, e = c_h − t/2; (b) angles on opposite sides, e = e_c + e_t (AS 4100:2020).*

`[derived]` Cl 8.4.6 is the standard route for hand-designing single-angle
web members in bolted trusses (a very common mining/conveyor-gantry
bracing detail) without running a full biaxial-bending check; it trades
some conservatism in the interaction exponent (linear, not 1.4-power) for
a simpler eccentricity model built into `M*_h`.

## Worked reference

None yet.

## Contradictions

None recorded. **Flag**: Cl 8.4.5.1, 8.4.5.2 and 8.4.6 (biaxial bending
and eccentric single-angle equations) all carry Amendment-No.-1 tags in
the source, and the source's "Appendix Former Wording" preserves the
pre-amendment text for each. The NCC's current reference edition of AS
4100:2020 is unamended, so for strict NCC-unamended compliance the former
wording governs — cross-check against the source PDF's Appendix Former
Wording before final sign-off on a biaxial-bending or eccentric-angle
check. See [[as-4100-2020-steel-structures]] "NCC compliance trap".

## Related

- [[as4100-combined-actions-section-capacity]] — `M_rx`, `M_ry`, `N_s`
  feeding this page.
- [[as4100-beam-member-moment-capacity]] — `M_bx`, `α_m` (Cl 5.6).
- [[as4100-compression-member-capacity]] — `N_cy`, `N_ch` (Cl 6.3).
- [[as4100-tension-member-capacity]] — `N_t` (Cl 7.2), single-angle
  eccentric connections (Cl 7.3.2, Table 7.3.2) as an alternative simpler
  path for statically-loaded bracing.
- [[as4100-member-effective-length-and-frame-buckling]] — `N_oz` section
  constants (App H).
- [[asi-design-capacity-tables-vol1-open-sections]] — Part 8 eccentrically
  loaded single-angle and angle-bending design load tables.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Cl 8.4 (pp. 105–112).
  Figure 8.4.6 reproduced in `wiki/0-standards/assets/`. Eq 8.4.5.1(1),
  8.4.5.2(1) and Cl 8.4.6 carry A1 amendment tags in the source.
