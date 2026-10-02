---
title: ACI 318M-19 beam design basis — scope, minimum depth, required and design strength
category: 2-concrete
tags: [aci, beams, design-basis, minimum-depth, t-beam, torsion]
standards: [ACI 318M-19 Cl 9.1, ACI 318M-19 Cl 9.2, ACI 318M-19 Cl 9.3, ACI 318M-19 Cl 9.4, ACI 318M-19 Cl 9.5]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 beam design basis and strength

> Scope: ACI 318M-19 Cl 9.1–9.5 — beam scope, general requirements
> (stability, T-beam construction and torsional flange width), design limits
> (minimum depth, deflection, strain and stress limits), required strength
> (critical sections for moment, shear, torsion) and the design-strength
> checklist (`φM_n`, `φV_n`, `φT_n`, `φP_n`). Reinforcement limits and detailing
> are on [[aci318-beam-reinforcement-limits-and-detailing]]; one-way joists and
> deep beams are on [[aci318-joists-and-deep-beams]]. This is an **ACI 318M-19
> page, kept separate from the AS 3600:2018 concept pages** elsewhere in
> `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Chapter 9 applies to nonprestressed and prestressed beams, including
composite beams cast in separate placements but acting as a unit, one-way
joist systems (Cl 9.8) and deep beams (Cl 9.9) (Cl 9.1.1). Composite
structural steel–concrete beams are **out of scope** — that is AISC 360 territory
(Cl R9.1.1). The chapter is a hub: it sets limits and checklists, then
delegates the actual strength calculations to Chapter 22 and the φ values to
Chapter 21 (see [[aci318-sectional-strength-flexure-and-axial]],
[[aci318-one-way-shear-strength]], [[aci318-torsional-strength]],
[[aci318-strength-reduction-factors]]).

## Detail

### General requirements (Cl 9.2)

`[code]` Concrete properties follow Chapter 19, reinforcement Chapter 20,
embedments Cl 20.6 (Cl 9.2.1). Cast-in-place beam-column and slab-column joints
satisfy Chapter 15; precast connections satisfy the force-transfer rules of
Cl 16.2 (Cl 9.2.2).

`[code]` **Stability** (Cl 9.2.3): a beam that is not continuously laterally
braced needs lateral bracing at no more than **50 × the least width of the
compression flange or face**, taking eccentric loads into account (Cl 9.2.3.1);
thin webs/flanges in prestressed beams, and member buckling between contact
points where a tendon touches an oversize duct only intermittently, must also
be considered (Cl 9.2.3.2). `[derived]` Tests show reinforced concrete beams —
even very deep and narrow ones — do not fail prematurely by lateral buckling
if loaded without lateral eccentricity that would induce torsion
(Cl R9.2.3.1), which is why the bracing limit is a generous multiple of flange
width rather than a slenderness-ratio check.

`[code]` **T-beam construction** (Cl 9.2.4): flange and web concrete must be
placed monolithically or made composite per Cl 16.4; effective flange width per
Cl 6.3.2 (see [[aci318-structural-analysis-methods]]); where the primary slab
reinforcement is parallel to the beam axis, perpendicular top slab
reinforcement is required per Cl 7.5.2.3 (see [[aci318-one-way-slab-design]]).
For **torsional** design, the overhanging flange used to compute `A_cp`, `A_g`
and `p_cp` extends on each side by the beam's projection above/below the slab
(whichever is greater), but not more than `4 ×` slab thickness — and the
flanges are **neglected altogether** if including them would give a *smaller*
`A_cp²/p_cp` (solid) or `A_g²/p_cp` (hollow) than ignoring them (Cl 9.2.4.4):

![[aci318-fig-r9.2.4.4-torsion-flange-sections.png]]
*Fig. R9.2.4.4 — examples of the portion of slab included with the beam for
torsional design: `h_b ≤ 4h_f` on each side, giving `b_w + 2h_b ≤ b_w + 8h_f`
for a two-sided flange (ACI 318M-19).*

### Minimum beam depth and deflection limits (Cl 9.3.1–9.3.2)

`[code]` For nonprestressed beams **not** supporting or attached to partitions or
other construction likely to be damaged by large deflections, overall depth `h`
must satisfy Table 9.3.1.1, unless calculated deflections satisfy Cl 9.3.2
(Cl 9.3.1.1):

| Support condition | Minimum `h` |
|---|---|
| Simply supported | `ℓ/16` |
| One end continuous | `ℓ/18.5` |
| Both ends continuous | `ℓ/21` |
| Cantilever | `ℓ/8` |

*(Table 9.3.1.1 — valid for normalweight concrete and `f_y = 420 MPa`;
transcribed directly as a four-row table.)* For other `f_y` multiply by
`(0.4 + f_y/700)` (Cl 9.3.1.1.1); for lightweight concrete with
`1440 ≤ w_c ≤ 1840 kg/m³` multiply by the greater of `1.65 − 0.0003w_c` and
`1.09` (Cl 9.3.1.1.2), also applicable to shored composite beams whose
lightweight concrete is in compression (Cl 9.3.1.1.3). A floor finish counts
toward `h` only if placed monolithically or designed composite per Cl 16.4
(Cl 9.3.1.2).

`[code]` Nonprestressed beams that don't satisfy Table 9.3.1.1 and **all**
prestressed beams need calculated immediate and time-dependent deflections per
Cl 24.2 against the Table 24.2.2 limits (Cl 9.3.2.1 — see
[[aci318-serviceability-deflection-and-cracking]]). For nonprestressed composite
beams that satisfy Cl 9.3.1, deflections after composite action need not be
calculated, but pre-composite deflections do unless the pre-composite depth also
satisfies Table 9.3.1.1 (Cl 9.3.2.2).

### Strain and stress limits (Cl 9.3.3–9.3.4)

`[code]` Nonprestressed beams with `P_u < 0.10 f'c A_g` **must be
tension-controlled** per Table 21.2.2 (Cl 9.3.3.1) — i.e. `ε_t ≥ ε_ty + 0.003`
(see [[aci318-strength-reduction-factors]]). `[derived]` This replaced the
pre-2019 minimum net tensile strain of 0.004; its purpose is to restrict the
reinforcement ratio and so avoid brittle flexural behaviour under overload, and
it does not apply to prestressed beams (Cl R9.3.3.1). Prestressed beams are
classified Class U/T/C per Cl 24.5.2 and must satisfy the transfer and service
stress limits of Cl 24.5.3/24.5.4 (Cl 9.3.4).

### Required strength (Cl 9.4)

`[code]` Required strength comes from the Chapter 5 factored load combinations
(see [[aci318-loads-and-load-combinations]]) and Chapter 6 analysis (see
[[aci318-structural-analysis-methods]]); prestress-induced reactions are
included per Cl 5.3.11 (Cl 9.4.1). For beams built integrally with supports,
`M_u` may be taken at the face of support (Cl 9.4.2.1), as may `V_u`
(Cl 9.4.3.1).

`[code]` **Shear critical section** (Cl 9.4.3.2): between the support face and
a section `d` from the face (nonprestressed) or `h/2` from the face
(prestressed), the beam may be designed for the `V_u` at that critical section
if (a) the support reaction introduces compression into the beam end region,
(b) loads are applied at or near the top surface, and (c) no concentrated load
occurs between the face and the critical section:

![[aci318-fig-r9.4.3.2-critical-section-shear-beams.png]]
*Fig. R9.4.3.2(a) — free-body diagrams at the end of a beam: the stirrups
crossing the closest inclined crack need only resist shear from loads beyond
`d` from the support face (ACI 318M-19).*

`[code]` **Torsion** (Cl 9.4.4): torsional loading from a slab may be taken as
uniformly distributed along the beam unless a more detailed analysis is made
(Cl 9.4.4.1); `T_u` may be taken at the support face (Cl 9.4.4.2) or at the
`d`/`h/2` critical section unless a concentrated torque acts within that
distance, in which case the critical section is the support face (Cl 9.4.4.3);
and `T_u` may be reduced per Cl 22.7.3 for compatibility torsion (Cl 9.4.4.4 —
see [[aci318-torsional-strength]]).

### Design strength (Cl 9.5)

`[code]` For each load combination, `φS_n ≥ U` at every section for `M`, `V`,
`T` and `P` as applicable, with interaction between load effects considered
(Cl 9.5.1.1); φ per Cl 21.2 (Cl 9.5.1.2). `M_n` comes from Cl 22.3 if
`P_u < 0.10 f'c A_g`, otherwise from Cl 22.4 (Cl 9.5.2.1–9.5.2.2); external
tendons count as unbonded unless effectively bonded along their full length
(Cl 9.5.2.3). `V_n` is from Cl 22.5, and horizontal shear `V_nh` of composite
beams from Cl 16.4 (Cl 9.5.3). `[derived]` A beam carrying significant axial
force isn't required to satisfy Chapter 10 but must meet the tie/spiral
requirements of Table 22.4.2.1, and slender beams with large axial load should
be checked for slenderness like columns (Cl R9.5.2.2).

`[code]` **Torsion** (Cl 9.5.4): torsional effects may be neglected if
`T_u < φT_th` (then the Cl 9.6.4 minimum reinforcement and Cl 9.7.5/9.7.6.3
detailing need not be provided) (Cl 9.5.4.1); `T_n` from Cl 22.7 (Cl 9.5.4.2).
Torsional longitudinal and transverse reinforcement is **added to** that
required for `V_u`, `M_u` and `P_u` acting with it (Cl 9.5.4.3) —
`[derived]` because shear steel area `A_v` counts *all* stirrup legs while
torsion steel area `A_t` counts only *one* leg, the combined requirement is
`A_v/s + 2A_t/s` and only the legs adjacent to the beam sides are credited for
torsion (Cl R9.5.4.3). In prestressed beams the longitudinal steel `A_s + A_ps`
at each section must resist `M_u` plus an extra concentric tension `A_ℓ f_y`
based on `T_u` (Cl 9.5.4.4); in nonprestressed beams the torsional longitudinal
steel in the flexural compression zone may be reduced by `M_u/(0.9 d f_y)`,
but never below the Cl 9.6.4 minimum (Cl 9.5.4.5). Two alternative-procedure
permissions exist for slender sections — solid sections with `h/b_t ≥ 3`
(Cl 9.5.4.6) and solid **precast** sections with `h/b_t ≥ 4.5`, which may use
open-web reinforcement (Cl 9.5.4.7) — in each case only where the procedure is
shown by analysis and comprehensive tests to be adequate.

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-beam-reinforcement-limits-and-detailing]] — Cl 9.6–9.7.
- [[aci318-joists-and-deep-beams]] — Cl 9.8–9.9.
- [[aci318-sectional-strength-flexure-and-axial]],
  [[aci318-one-way-shear-strength]], [[aci318-torsional-strength]] — the
  Chapter 22 strength calculations Chapter 9 calls.
- [[concrete-beam-strength-in-bending]], [[concrete-beam-shear-and-torsion-design]]
  — the AS 3600 equivalents, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 9 Cl 9.1–9.5 (pp. 127–135),
  incl. Table 9.3.1.1 and Figs. R9.2.4.4, R9.4.3.2.
