---
title: Web stiffeners — load bearing, intermediate transverse, end posts and longitudinal
category: 0-standards
tags: [webs, stiffeners, load-bearing-stiffener, intermediate-stiffener, end-post, longitudinal-stiffener, plate-girder]
standards: [AS 4100:2020 Cl 5.14, AS 4100:2020 Cl 5.15, AS 4100:2020 Cl 5.16]
status: draft
reviewed: 2026-09-13
---

# Web stiffeners

> Scope: AS 4100:2020 Cl 5.14 (load bearing stiffeners: yield, buckling,
> outstand, fitting, torsional end restraint), Cl 5.15 (intermediate
> transverse web stiffeners: spacing, minimum area, buckling, minimum
> stiffness, outstand, external forces, connection to web, end posts),
> Cl 5.16 (longitudinal stiffeners). When a stiffener is needed at all is
> decided on [[as4100-web-shear-and-bearing]] (Cl 5.10.2, 5.13).

## Summary

`[code]` A load bearing stiffener must satisfy both `R* ≤ φR_sy` (yield,
Cl 5.14.1) and `R* ≤ φR_sb` (buckling, Cl 5.14.2), `φ = 0.9`, where
`R_sy = R_by + A_s f_ys` and `R_sb` is the Section 6 capacity of a cruciform
"column" made of the stiffener plus a length of web each side of
`min(17.5t_w/sqrt(f_y/250), s/2)`, with `α_b = 0.5`, `k_f = 1.0`, radius of
gyration about the axis parallel to the web, and `l_e = 0.7d_1` (flanges
restrained against rotation in the stiffener plane) or `d_1` otherwise.

`[code]` An intermediate transverse stiffener must satisfy
`V* ≤ φ(R_sb + V_b)` (Cl 5.15.4) with `V_b` computed using `α_d = α_f = 1.0`,
plus minimum area (Cl 5.15.3) and minimum stiffness (Cl 5.15.5).

## Detail

### Load bearing stiffeners (Cl 5.14)

`[code]`
- **Yield** (5.14.1): `R_sy = R_by + A_s f_ys`; `R_by` per Cl 5.13.3; `A_s` =
  stiffener area in contact with the flange; `f_ys` = stiffener yield
  stress. `R*` includes any shear applied directly to the stiffener.
- **Buckling** (5.14.2): as in the Summary. Effective section = stiffener +
  web strip each side ≤ lesser of `17.5t_w/sqrt(f_y/250)` and `s/2` (if
  available).
- **Outstand** (5.14.3): `b_es ≤ 15t_s/sqrt(f_ys/250)` unless the outer
  edge is continuously stiffened.
- **Fitting** (5.14.4): tight, uniform bearing against the loaded flange
  unless flange-to-stiffener welds transmit the force; over a support this
  applies to both flanges. Provide welds/bolts to transmit the stiffener's
  share of `R*` to the web.
- **Torsional end restraint** (5.14.5): where load bearing stiffeners are
  the only torsional end restraint at a support, the pair must have
  `I_s ≥ (α_t/1000)(d³ t_f R*/F*)` about the web centreline, with
  `α_t = 230/(l_e/r_y) − 0.60`, `0 ≤ α_t ≤ 4`; `R*` = design reaction at
  the bearing; `F*` = total design load on the member between supports;
  `t_f` = critical flange thickness; `l_e/r_y` = the stiffener slenderness
  used in Cl 5.14.2.

`[derived]` The Cl 5.14.5 rule is what makes a pair of end stiffeners count
as an "F" restraint at a simple support (Cl 5.4.2.1(a), Figure 5.4.2.1(a)).
Without it, or without a bolted end plate/cleat that prevents twist, the
support may only be "P" or unrestrained for lateral-torsional buckling.

### Intermediate transverse web stiffeners (Cl 5.15)

`[code]`
- **General** (5.15.1): extend between flanges, terminating no further than
  `4t_w` from a flange; one or both sides of the web.
- **Spacing** (5.15.2): interior panels satisfy Cl 5.10.4 or 5.10.5. End
  panels need an end post per Cl 5.15.9, unless the end panel width `s` is
  reduced so that `V_b` with `α_d = 1.0` (no tension field) satisfies
  Cl 5.11.1 and 5.12.
- **Minimum area** (5.15.3), stiffener without external loads:
  `A_s ≥ 0.5γ A_w (1 − α_v)(V*/φV_u) · [ (s/d_p) − (s/d_p)² / sqrt(1 + (s/d_p)²) ]`
  with `γ` = 1.0 (pair), 1.8 (single angle), 2.4 (single plate); `α_v` per
  Cl 5.11.5.2.
- **Buckling** (5.15.4): `V* ≤ φ(R_sb + V_b)`, `R_sb` per Cl 5.14.2 with
  `l_e = d_1`; `V_b` per Cl 5.11.5.2 with `α_d = 1.0`, `α_f = 1.0`.
- **Minimum stiffness** (5.15.5), about the web centreline:
  `I_s ≥ 0.75 d_1 t_w³` for `s/d_1 ≤ sqrt(2)`; `I_s ≥ 1.5 d_1³ t_w³ / s²` for
  `s/d_1 > sqrt(2)`.
- **Outstand** (5.15.6): per Cl 5.14.3.
- **External forces** (5.15.7): where the stiffener transfers forces `F*_n`
  normal to the web or moments `M* + F*_p e` normal to the web, increase the
  Cl 5.15.5 minimum `I_s` by `d_1⁴ {2F*_n + [(M* + F*_p e)/d_1]} / (φ E d_1 t_w)`;
  a stiffener carrying transverse load parallel to the web is designed as a
  load bearing stiffener (Cl 5.14).
- **Connection to web** (5.15.8): design shear per unit length ≥
  `0.0008 t_w² f_y / b_es` kN/mm (`t_w`, `b_es` in mm).
- **End posts** (5.15.9): a load bearing stiffener (Cl 5.14, no smaller
  than the end plate) plus a parallel end plate with area
  `A_ep ≥ d_1 [(V*/φ) − α_v V_w] / (8 e f_y)`, `e` = distance between end
  plate and load bearing stiffener.

### Longitudinal web stiffeners (Cl 5.16)

`[code]` Continuous, or extending between and attached to transverse
stiffeners (5.16.1). Minimum stiffness about the face of the web (5.16.2):
at `0.2d_2` from the compression flange,
`I_s ≥ 4 d_2 t_w³ [1 + (4A_s/(d_2 t_w))(1 + A_s/(d_2 t_w))]`; a second stiffener
at the neutral axis, `I_s ≥ d_2 t_w³`. `A_s` = stiffener area.

`[derived]` Longitudinally stiffened webs are rare in mining structural
steelwork (they belong to deep plate girders and box girders, where AS 4100
itself points to AS/NZS 5100.6). Transverse stiffeners at crane runway
girder supports and under heavy machine loads are the usual case.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as4100-web-shear-and-bearing]] — `R_by`, `V_b`, `α_v`, when stiffeners
  are required (Cl 5.10.2), Appendix I combined checks.
- [[as4100-compression-member-capacity]] — Section 6 method used for
  `R_sb` (α_b = 0.5, k_f = 1.0).
- [[as4100-beam-lateral-restraint]] — end stiffeners as torsional restraint
  (Cl 5.4.2.1, 5.4.3.2).

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Cl 5.14–5.16
  (pp. 81–86).
