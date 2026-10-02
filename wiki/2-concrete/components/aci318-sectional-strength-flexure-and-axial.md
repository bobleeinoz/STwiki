---
title: ACI 318M-19 sectional strength — flexure and axial strength design assumptions
category: 2-concrete
tags: [aci, flexure, axial-strength, stress-block, sectional-strength]
standards: [ACI 318M-19 Cl 22.1, ACI 318M-19 Cl 22.2, ACI 318M-19 Cl 22.3, ACI 318M-19 Cl 22.4]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 sectional strength — flexure and axial

> Scope: ACI 318M-19 Cl 22.1 (chapter scope), 22.2 (design assumptions for
> moment/axial strength — equilibrium, strain compatibility, the equivalent
> rectangular stress block and β₁, reinforcement stress assumptions), 22.3
> (flexural strength for prestressed/composite members) and 22.4 (axial
> strength — P_n,max cap, maximum axial tension). This is an **ACI 318M-19
> page, kept separate from the AS 3600:2018 concept pages** elsewhere in
> `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Chapter 22 is the single home for calculating nominal strength at a
section — flexure, axial, one-way shear, two-way shear, torsion, bearing and
shear friction (Cl 22.1.1) — **unless** the member/region is instead designed
by the strut-and-tie method of Chapter 23 (Cl 22.1.2). This page covers the
flexure (22.3) and axial (22.4) strands; shear, torsion, bearing and shear
friction are on their own pages (see Related).

## Detail

### Design assumptions for moment and axial strength (Cl 22.2)

`[code]` Two basic conditions must be satisfied at nominal strength:
**equilibrium** and **strain compatibility** (Cl 22.2.1.1). Strain in
concrete and nonprestressed reinforcement is assumed proportional to
distance from the neutral axis — i.e. plane sections remain plane
(Cl 22.2.1.2). Prestressed reinforcement strain additionally includes the
effective prestress strain, with *changes* in strain for bonded tendons
assumed proportional to distance from the neutral axis the same way
(Cl 22.2.1.3–22.2.1.4); unbonded tendon strain instead depends on overall
member elongation (Cl R22.2.1.4, Cl 20.3.2.4).

`[code]` **Concrete assumptions** (Cl 22.2.2): maximum usable strain at the
extreme compression fibre is fixed at **0.003** (Cl 22.2.2.1) — this is a
design convention, not a true crushing strain (which tests show ranges
0.003–0.008+, Cl R22.2.2.1). Concrete tensile strength is neglected in
flexural/axial strength calculations (Cl 22.2.2.2). Any stress-strain shape
(rectangular, trapezoidal, parabolic, etc.) is permitted provided it predicts
strength in substantial agreement with comprehensive test results
(Cl 22.2.2.3) — the Code's own **equivalent rectangular stress block**
(Cl 22.2.2.4) is one way of satisfying this, not the only way:

- Uniform stress of **0.85f'c** over a compression zone of depth
  `a = β₁c`, where `c` is the neutral-axis depth measured perpendicular to
  the neutral axis (Cl 22.2.2.4.1–22.2.2.4.2, Eq. 22.2.2.4.1).
- `β₁` depends on concrete strength:

![[aci318-table-22.2.2.4.3-beta1-factor.png]]
*Table 22.2.2.4.3 — values of β₁ for the equivalent rectangular concrete
stress distribution (ACI 318M-19).* `[derived]` The lower bound β₁ = 0.65
for f'c ≥ 55 MPa reflects experimental data specifically from
higher-strength concrete beams (Cl R22.2.2.4.3) — this is conceptually
parallel to AS 3600's own γ-factor stress-block depth reduction at high
f'c (see [[concrete-beam-strength-in-bending]]), but the two factors are
not numerically interchangeable.

`[code]` **Reinforcement assumptions** (Cl 22.2.3–22.2.4): deformed bar
stress-strain is idealised per Cl 20.2.2.1–20.2.2.2 (elastic-plastic,
effectively — see [[aci318-strength-reduction-factors]] for the `ε_ty = f_y/E_s`
yield-strain definition this feeds). Bonded prestressed reinforcement stress
at nominal strength, `f_ps`, comes from Cl 20.3.2.3; unbonded tendons from
Cl 20.3.2.4; a strand embedded shorter than its development length `ℓ_d` has
its design stress capped per Cl 25.4.8.3 (Cl 22.2.4.1–22.2.4.3).

### Flexural strength (Cl 22.3)

`[code]` Nominal flexural strength `M_n` is calculated using the Cl 22.2
assumptions (Cl 22.3.1.1). For prestressed members, ordinary deformed
reinforcement provided alongside prestressed reinforcement may be counted
toward tensile strength at stress `f_y` (Cl 22.3.2.1); other nonprestressed
reinforcement needs a full strain-compatibility analysis to justify its
contribution (Cl 22.3.2.2). For **composite concrete flexural members** (cast
in separate placements but acting as a unit): the entire composite section
may be used for `M_n` regardless of whether construction was shored or
unshored (Cl 22.3.3.1–22.3.3.3); where `f'c` differs between elements, either
use each element's own properties or conservatively use whichever single
`f'c` gives the most critical `M_n` (Cl 22.3.3.4). `[code]` Composite
*structural steel*-concrete beams are explicitly out of scope — that's
AISC 360 territory, not this Code (Cl R22.3.3.1).

### Axial strength or combined flexural and axial strength (Cl 22.4)

`[code]` Nominal flexural and axial strength both use the Cl 22.2
assumptions (Cl 22.4.1.1).

`[code]` **Maximum axial compressive strength** (Cl 22.4.2): `P_n` is capped
at `P_n,max` from Table 22.4.2.1 — a fixed fraction of the pure-axial squash
load `P_o`, applied regardless of how small the actual eccentricity is. This
accounts for *unavoidable* construction eccentricity rather than any
calculated eccentricity (Cl R22.4.2.1):

![[aci318-table-22.4.2.1-maximum-axial-strength.png]]
*Table 22.4.2.1 — maximum axial strength `P_n,max` as a fraction of `P_o`, by
member type and transverse reinforcement (ACI 318M-19).* Spiral confinement
earns the higher 0.85 fraction (vs 0.80 for ties) in every row where it
appears — consistent with Chapter 21's own higher φ for spiral columns (see
[[aci318-strength-reduction-factors]]).

`[code]` `P_o` (pure axial squash load) is calculated as:

- Nonprestressed: `P_o = 0.85 f'c (A_g − A_st) + f_y A_st` (Eq. 22.4.2.2).
- Prestressed: `P_o = 0.85 f'c (A_g − A_st − A_pd) + f_y A_st − (f_se −
  0.003 E_p) A_pt` (Eq. 22.4.2.3) — the extra term subtracts the loss of
  column capacity from the prestress force itself, and `A_pd` (duct +
  tendon area) reduces the effective concrete area; `f_se` is taken as at
  least `0.003 E_p` (Cl R22.4.2.3).

`[code]` `f_y` used in `P_o`/`P_n,max` is capped at **550 MPa** regardless of
the reinforcement's actual yield strength, because concrete's compression
capacity is expected to govern before a higher steel stress could be reached
(Cl 22.4.2.1, Cl R22.4.2.1). Deep foundation members are exempt from the
ordinary tie/spiral transverse-reinforcement requirements of Cl 22.4.2.4–
22.4.2.5 — they instead follow Chapter 13's own detailing (Table 22.4.2.1 row
(e)).

`[code]` **Maximum axial tensile strength** (Cl 22.4.3): `P_nt ≤ P_nt,max =
f_y A_st + (f_se + Δf_p) A_pt` (Eq. 22.4.3.1), where `(f_se + Δf_p)` is
capped at the tendon's yield strength `f_py`, and `A_pt = 0` for a
nonprestressed member.

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-strength-reduction-factors]] — Chapter 21, the φ that converts every
  `S_n` calculated here into a design strength `φS_n`.
- [[aci318-one-way-shear-strength]] — Cl 22.5, same chapter's shear provisions.
- [[aci318-one-way-slab-design]], [[aci318-two-way-slab-design-basis]] —
  Chapters 7–8, which invoke this page's `M_n` for the slab moment design
  strength check.
- [[concrete-beam-strength-in-bending]] — the AS 3600 equivalent (rectangular
  stress block, γ factor), for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 22 Cl 22.1–22.4 (pp. 397–401),
  incl. Tables 22.2.2.4.3 and 22.4.2.1.
