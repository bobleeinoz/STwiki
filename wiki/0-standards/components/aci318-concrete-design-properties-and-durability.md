---
title: ACI 318M-19 concrete design properties and durability — f'c limits, Ec, fr, λ, exposure classes, mixture requirements
category: 0-standards
tags: [aci, concrete-properties, durability, exposure-classes, lightweight-concrete, freeze-thaw]
standards: [ACI 318M-19 Cl 19.1, ACI 318M-19 Cl 19.2, ACI 318M-19 Cl 19.3, ACI 318M-19 Cl 19.4]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 concrete design properties and durability

> Scope: ACI 318M-19 Chapter 19 in full — specified strength limits, modulus of
> elasticity and rupture, the lightweight-concrete factor λ, the F/S/W/C
> exposure classification, mixture requirements by exposure class, freeze–thaw
> air content, chloride limits and grout durability. This is an **ACI 318M-19
> page, kept separate from the AS 3600:2018 concept pages** elsewhere in
> `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why. The AS 3600
> counterparts are [[as3600-properties-of-concrete]] and
> [[as3600-durability-and-cover]]; exposure classification systems differ
> (ACI F/S/W/C vs AS 3600 A1–U), so classes are not interchangeable.

## Summary

`[code]` Chapter 19 gives (a) the concrete properties to use in design and
(b) durability requirements for concrete and for grout around bonded tendons
(Cl 19.1). Steel properties and cover are in Chapter 20 (see
[[aci318-reinforcement-properties-durability-and-embedments]]); mixture
production and acceptance are in Chapter 26.

## Detail

### Specified compressive strength `f'c` (Cl 19.2.1)

`[code]` `f'c` satisfies (a) the Table 19.2.1.1 minimum limits (both normalweight
and lightweight), (b) the durability requirements of Table 19.3.2.1, (c) structural
strength requirements, and (d) a **35 MPa cap** for lightweight concrete in special
moment frames, special structural walls and their foundations unless tests show
strength and toughness at least equal to comparable normalweight members
(Cl 19.2.1.1):

![[aci318-table-19.2.1.1-limits-for-fc.png]]
*Table 19.2.1.1 — minimum `f'c`: 17 MPa general and foundations in SDC A–C; 21 MPa for
SDC D–F foundations (other than light residential/utility stud-wall buildings of two
storeys or less, which stay at 17 MPa), special moment frames and special walls with
Grade 420/550 steel; 35 MPa special walls with Grade 690 steel; 28 MPa precast
nonprestressed driven piles and drilled shafts; 35 MPa precast prestressed driven piles
(ACI 318M-19).* `f'c` is used for mixture proportioning (Cl 26.4.3) and acceptance
(Cl 26.12.3); unless otherwise specified it is a **28-day** value, with any other test
age stated in the construction documents (Cl 19.2.1.2–19.2.1.3).

### Modulus of elasticity and rupture (Cl 19.2.2–19.2.3)

`[code]` `E_c` may be taken as `w_c^1.5 × 0.043√f'c` MPa for `1440 ≤ w_c ≤ 2560 kg/m³`
(Eq. 19.2.2.1.a), or `4700√f'c` MPa for normalweight concrete (Eq. 19.2.2.1.b), or
specified from mixture testing (mixture proportioned to it per Cl 26.4.3, verified
and reported with the mixture submittal, measured at 28 days unless stated)
(Cl 19.2.2.2). Modulus of rupture `f_r = 0.62λ√f'c` (Eq. 19.2.3.1) — used for
cracking moment and the 1.2×cracking-load minimum-steel rules (see
[[aci318-beam-reinforcement-limits-and-detailing]],
[[aci318-serviceability-deflection-and-cracking]]).

### Lightweight concrete factor λ (Cl 19.2.4)

![[aci318-table-19.2.4.1a-lambda-by-density.png]]
*Table 19.2.4.1(a) — λ from equilibrium density `w_c`: 0.75 (≤ 1600 kg/m³);
`0.0075w_c ≤ 1.0` (1600–2160); 1.0 (> 2160) (ACI 318M-19).*

![[aci318-table-19.2.4.1b-lambda-by-aggregate.png]]
*Table 19.2.4.1(b) — λ from aggregate composition: all-lightweight 0.75; lightweight
with fine blend 0.75–0.85; sand-lightweight 0.85; sand-lightweight with coarse blend
0.85–1.0 (linear interpolation on absolute volume of normalweight fine/coarse
aggregate) (ACI 318M-19).* Except as Table 25.4.2.5 requires, either table may be
used (Cl 19.2.4.1); it is permitted to take `λ = 0.75` for any lightweight concrete
(Cl 19.2.4.2) and `λ = 1.0` for normalweight (Cl 19.2.4.3).

### Exposure categories and classes (Cl 19.3.1)

`[code]` The licensed design professional assigns an exposure class for each
category per member (Cl 19.3.1.1):

![[aci318-table-19.3.1.1-exposure-categories-and-classes.png]]
*Table 19.3.1.1 — exposure categories/classes: **F** freeze–thaw (F0–F3), **S**
water-soluble sulfate in soil/water (S0–S3), **W** contact with water (W0–W2), **C**
corrosion protection of reinforcement (C0–C2) (ACI 318M-19).* `[derived]` Each
member can carry up to four classes at once (one per category); the mixture then
has to satisfy the most restrictive requirement among them (Cl 19.3.2.1).

### Requirements for concrete mixtures (Cl 19.3.2)

![[aci318-table-19.3.2.1-requirements-by-exposure-class.png]]
*Table 19.3.2.1 — requirements by exposure class: maximum `w/cm` and minimum `f'c` (F1
0.55/24 MPa, F2 0.45/31, F3 0.40/35; S1 0.50/28, S2 0.45/31, S3 0.45/31 or 0.40/35;
W2 0.50/28; C2 0.40/35), air-content, cementitious-material type and calcium-chloride
restrictions for S classes, and maximum water-soluble chloride ion content (C0 1.00,
C1 0.30, C2 0.15 % by mass of cementitious material for nonprestressed; 0.06 for
prestressed) (ACI 318M-19).* Footnotes: `w/cm` counts all cementitious and
supplementary materials; the limits don't apply to lightweight concrete; plain
concrete in F3 uses `w/cm ≤ 0.45` and `f'c ≥ 31 MPa`; alternative sulfate-resistant
cementitious combinations are permitted when tested per Cl 26.4.2.2(c); chloride
mass of supplementary cementitious materials counted doesn't exceed the portland
cement mass.

### Freeze–thaw air content and chloride rules (Cl 19.3.3–19.3.4)

`[code]` Concrete in F1, F2, F3 is **air entrained**, with target air content from:

![[aci318-table-19.3.3.1-air-content-freezing-thawing.png]]
*Table 19.3.3.1 — total air content (%): for nominal maximum aggregate size 9.5 / 12.5 /
19 / 25 / 37.5 / 50 / 75 mm, F1 = 6.0 / 5.5 / 5.0 / 4.5 / 4.5 / 4.0 / 3.5 and F2–F3 = 7.5
/ 7.0 / 6.0 / 6.0 / 5.5 / 5.0 / 4.5 (ACI 318M-19).* Sampling per ASTM C172, measurement
per ASTM C231 or C173 (Cl 19.3.3.2). For `f'c ≥ 35 MPa` the target may be reduced by
**1.0 percentage point** (Cl 19.3.3.6). Wet-mix shotcrete in F1–F3 and dry-mix
shotcrete in F3 are air entrained to Table 19.3.3.3 (wet-mix 5.0/6.0/6.0 % before
placement; dry-mix 4.5 % in-place for F3 only) (Cl 19.3.3.3–19.3.3.5). Maximum
pozzolan and slag content in F3 per Cl 26.4.2.2(b) (Cl 19.3.3.7). Nonprestressed
concrete cast against stay-in-place **galvanized steel forms** meets the C1 chloride
limit unless project conditions demand tighter (Cl 19.3.4.1).

### Grout durability (Cl 19.4)

`[code]` Water-soluble chloride ion content of grout for bonded tendons ≤ **0.06%**
by mass of cementitious materials, tested per ASTM C1218 (Cl 19.4.1).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-reinforcement-properties-durability-and-embedments]] — Chapter 20,
  cover and corrosion protection that pair with these exposure classes.
- [[aci318-structural-system-requirements]] — Cl 4.8 durability philosophy.
- [[aci318-strength-reduction-factors]], [[aci318-sectional-strength-flexure-and-axial]]
  — consume `f'c`, `E_c`, `f_r`, λ.
- [[as3600-properties-of-concrete]], [[as3600-durability-and-cover]] — the AS
  3600 equivalents, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 19 Cl 19.1–19.4 (pp. 355–369),
  incl. Tables 19.2.1.1, 19.2.4.1(a)/(b), 19.3.1.1, 19.3.2.1, 19.3.3.1, 19.3.3.3.
