---
title: ACI 318M-19 Appendix A — design verification using nonlinear response history analysis
category: 0-standards
tags: [aci, seismic, nonlinear-response-history, effective-stiffness, expected-strength, peer-review]
standards: [ACI 318M-19 Appendix A, ASCE/SEI 7 Chapter 16]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 Appendix A — design verification using nonlinear response history analysis

> Scope: ACI 318M-19 Appendix A (A.1–A.13). It supplements ASCE/SEI 7 Chapter 16 for new reinforced
> concrete earthquake-resistant structures (Cl A.2.1, A.2.3). **ACI 318M-19 page, kept separate from the
> AS 3600:2018 pages** (see [[aci-318m-19-building-code-concrete]]). Prescriptive seismic detailing is in
> [[aci318-earthquake-general-and-ordinary-intermediate-frames]], [[aci318-special-moment-frames]],
> [[aci318-special-structural-walls]].

## Summary

`[code]` Appendix A applies in addition to Chapters 1–26 (Cl A.2.2) to structural systems in the
seismic-force-resisting system (diaphragms, moment frames, walls, foundations) and members that carry
other loads while undergoing earthquake deformations (Cl A.2.3). Structures are still proportioned and
detailed per Chapter 18 and the Cl A.12 enhanced requirements (Cl A.2.4). It may be used to demonstrate
the adequacy of a system under Cl 18.2.1.7 (Cl A.2.5). **Independent structural design review (Cl A.13) is
mandatory** (Cl A.2.6). Interpretations are justified by the design professional, accepted by the
reviewers and then the building official (Cl A.2.7). The action classification and acceptance criteria of
Cl A.7, A.10 and A.11 take precedence over ASCE/SEI 7 Chapter 16 (Cl A.3.1).

## Detail

### Notation and terminology (A.1)

`[code]` Symbols include bias factor `B`, ultimate deformation capacity `D_u`, expected concrete strength
`f'ce`, expected steel yield/tensile strengths `f_ye`/`f_ue`, plastic-hinge length `ℓ_p`, expected strength
`R_ne`, expected shear `V_ne`, yield rotation `θ_y` and seismic resistance factor `φ_s` for force-controlled
actions (Cl A.1.1). Action classes (deformation-controlled, force-controlled, critical/ordinary/noncritical)
are as defined in ASCE/SEI 7 Chapter 16 (Cl A.1.2).

### Ground motions, loads, modelling (A.4–A.6)

`[code]` Horizontal ground motions are always included; vertical motion simultaneously where it substantially
affects design (Cl A.4.1–A.4.2). Histories are selected and modified per the general building code
(Cl A.4.3), as are load combinations (Cl A.5.1). Models are three-dimensional (Cl A.6.1); nonlinear
member behaviour (stiffness, expected strength, deformation capacity, hysteresis under reversal) is
substantiated by test data and not extrapolated beyond test limits (Cl A.6.2). Strength/stiffness
degradation is modelled unless demand is shown too small, and in finite-element models the deformation at the
onset of strength loss must not depend on mesh configuration (Cl A.6.3). For walls with `h_w/ℓ_w ≥ 2` the
model represents wall rotation and uplift kinematics, including neutral-axis migration, unless shown to be
irrelevant (Cl A.6.4).

### Action classification (A.7)

`[code]` Actions are deformation-controlled (checked per Cl A.10) or force-controlled (Cl A.11).
**Deformation-controlled:** moment in beams, structural walls, coupling beams and slab–column
connections; shear in diagonally reinforced coupling beams meeting Cl 18.10.7.4; moment in columns combined
with axial force where Cl 18.7.4–18.7.6 are met (Cl A.7.2.2). **Ordinary force-controlled:** shear and moment
in perimeter basement walls; in-plane shear in non-transfer diaphragms; in-plane normal forces in diaphragms
other than collectors; moment in shallow and deep foundation members (Cl A.7.3.2). **Noncritical:**
components whose failure causes no collapse, loss of earthquake resistance or falling hazard (Cl A.7.3.3).
All other actions are **critical force-controlled** (Cl A.7.3.4).

### Effective stiffness (A.8)

`[code]` Stiffness includes flexure, shear, axial and reinforcement-slip deformation (Cl A.8.1); cracking is modelled
where anticipated (Cl A.8.2); the model captures behaviour at and beyond the onset of inelastic response
(Cl A.8.3). Effective stiffness is either substantiated by test-based analysis or taken from Table A.8.4
(Cl A.8.4):

![[aci318-table-A.8.4-effective-stiffness-values.png]]
*Table A.8.4 — effective stiffness (axial / flexural / shear): nonprestressed beams `1.0E_cA_g` /
`0.3E_cI_g` / `0.4E_cA_g`; prestressed beams `1.0E_cA_g` / `1.0E_cI_g` / `0.4E_cA_g`; columns with
compression ≥ `0.5A_gf'c` flexure `0.7E_cI_g`, with ≤ `0.1A_gf'c` or tension `0.3E_cI_g` (interpolate between);
walls in-plane `0.35E_cI_g` / shear `0.2E_cA_g`, out-of-plane `0.25E_cI_g`; diaphragms nonprestressed
`0.25`, prestressed `0.5` flexure; coupling beams flexure `0.07(ℓ_n/h)E_cI_g ≤ 0.3E_cI_g`; mat foundations
`0.5` in-plane, `0.5E_cI_g` out-of-plane. Values apply jointly unless alternatives are justified
(ACI 318M-19).* Joint flexibility may be modelled implicitly via effective beam/column stiffness plus
rigid end offsets to the joint centre (Cl A.8.5); beams cast with slabs include the Cl 6.3.2 effective
flange width (Cl A.8.6). Compare: [[aci318-structural-analysis-methods]].

### Expected material strength (A.9)

`[code]` Use project data, else Table A.9.1 (Cl A.9.1):

![[aci318-table-A.9.1-expected-material-strengths.png]]
*Table A.9.1 — concrete `f'ce = 1.3f'c` (strength at about 1 year or more); A615 Gr 420 `f_ye` 480 MPa,
`f_ue` 730 MPa; A706 Gr 420 475/655 MPa; A706 Gr 550 590/770 MPa (ACI 318M-19).*

### Deformation-controlled acceptance (A.10)

`[code]` Computed deformations stay within the ultimate capacity `D_u` in every analysis unless the strength
in that mode is assumed negligible thereafter and the structure remains stable and strong enough, or the response
is deemed unacceptable per ASCE/SEI 7 (Cl A.10.1). `D_u` is (Cl A.10.2): (a) the valid modelling range demonstrated
against test hysteresis including gravity load; (b) for special walls with fibre models, evaluated from the
average vertical strain over the plastic-hinge length `ℓ_p`, the longer of `0.2ℓ_w + 0.03h_w` and
`0.08h_w + 0.022f_yd_b`, not exceeding the storey height; (c) per ACI 369.1M or tests for lumped-plasticity or
fibre component models.

![[aci318-figure-RA.10.2-ultimate-deformation-capacity.png]]
*Fig. RA.10.2 — `D_u` identified in the response hysteresis of an analysis model (ACI 318M-19 commentary).*

### Force-controlled acceptance (A.11)

`[code]` Expected strength is `φ_sBR_n` evaluated per the general building code (Cl A.11.1), with `φ_s` per
Table A.11.2 (φ per Chapter 21, excluding Cl 21.2.4.1) (Cl A.11.2):

![[aci318-table-A.11.2-seismic-resistance-factor.png]]
*Table A.11.2 — critical `φ_s = φ`; ordinary `φ/0.9 ≤ 1.0`; noncritical `φ/0.85 ≤ 1.0` (ACI 318M-19).*

`[code]` Bias factor `B = 1.0`, or `B = 0.9R_ne/R_n ≥ 1.0` (Eq. A.11.3) with `R_n` per Chapter 18, 22 or 23
(Cl A.11.3–A.11.3.1). `R_ne` uses `f'ce` and `f_ye` in place of `f'c`, `f_y`/`f_yt` (Cl A.11.3.2). For walls with
`h_w/ℓ_w ≥ 2` modelled with fibres (Cl A.10.2(b)), strains taken as the mean of maximum demands across the
analysis suite, compressive strain < 0.005 and tensile strain < 0.01: `V_ne = 1.5A_cv(0.17λ√f'ce + ρ_tf_ye)`,
limited to `1.0A_cv√f'ce` for all wall segments sharing a lateral force and `1.25A_cv√f'ce` for an individual
segment (Cl A.11.3.2.1). Wall panel zones: `V_ne` per Cl A.11.3.2.1(a), not above `2.1A_cv√f'ce`
(Cl A.11.3.2.2).

### Enhanced detailing (A.12)

`[code]` Triggered where the mean maximum deformation across the analyses exceeds `0.5D_u` of confined
concrete (Cl A.12.1). **Special moment frames:** transversely supported flexural bar spacing in beams ≤ 200 mm
(replacing Cl 18.6.4.2 limit); column strength sum at a joint ≥ **1.4×** beam strength sum; every
longitudinal column bar supported by a hoop corner or seismic hook regardless of load or `f'c`; where beam
deformations exceed `0.5D_u`, the column dimension parallel to beam bars required by Cl 18.8.2.3 is increased
by 20 % (Cl A.12.2). **Special walls:** boundary elements per Cl 18.10.6 with transverse steel per Cl A.12.2.3; if
boundary elements are required, shear-reinforcement splices are mechanical/welded or laps enclosed by transverse
steel at the smaller of `6d_b` and 150 mm; slab flexural bars extended through slab–wall joints that analysis shows
yielding; where shear exceeds `0.33A_cvλ√f'c`, enhanced construction-joint detailing (roughening, shear keys)
(Cl A.12.3).

### Independent structural design review (A.13)

`[code]` The reviewer acts under the building official's direction, is acceptable to the official and has
knowledge of ground-motion selection/scaling, structural system behaviour, analytical modelling (including
physical-test calibration and soil–structure interaction), and Appendix A (Cl A.13.1–A.13.2). Minimum scope: basis
of design document and performance objectives; structural system; hazard and ground motions; component
modelling; analysis model; results versus acceptance criteria; design and detailing; drawings,
specifications and QA/inspection provisions (Cl A.13.3). Documentation: reviewer comments, written responses,
and a summary letter to the building official with a log and any unresolved items explained (Cl A.13.4).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[aci-318m-19-building-code-concrete]] — source register.
- [[aci318-earthquake-general-and-ordinary-intermediate-frames]], [[aci318-special-moment-frames]],
  [[aci318-special-structural-walls]], [[aci318-earthquake-diaphragms-foundations-and-non-sfrs-members]]
  — Chapter 18 provisions that Appendix A verifies.
- [[aci318-structural-analysis-methods]] — Chapter 6 linear-analysis stiffness values for comparison.
- [[aci318-strength-reduction-factors]] — φ used in Table A.11.2.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Appendix A (printed pp. 567–579).
