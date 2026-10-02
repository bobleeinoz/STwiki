---
title: ACI 318M-19 earthquake-resistant structures — SDC routing, general rules, ordinary and intermediate moment frames, intermediate precast walls
category: 2-concrete
tags: [aci, earthquake, seismic, sdc, ordinary-moment-frame, intermediate-moment-frame, precast-walls]
standards: [ACI 318M-19 Cl 18.1, ACI 318M-19 Cl 18.2, ACI 318M-19 Cl 18.3, ACI 318M-19 Cl 18.4, ACI 318M-19 Cl 18.5]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 earthquake-resistant structures — general, ordinary and intermediate systems

> Scope: ACI 318M-19 Cl 18.1–18.5 — scope and intent of Chapter 18, how
> Seismic Design Category (SDC) selects which provisions apply, general analysis
> and material rules shared by special systems, ordinary moment frames,
> intermediate moment frames (including two-way slabs without beams) and
> intermediate precast structural walls. Special moment frames are on
> [[aci318-special-moment-frames]], special structural walls on
> [[aci318-special-structural-walls]], diaphragms/foundations/non-SFRS members on
> [[aci318-earthquake-diaphragms-foundations-and-non-sfrs-members]]. This is an
> **ACI 318M-19 page, kept separate from the AS 3600:2018 concept pages**
> elsewhere in `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why.
> Australian earthquake design is by AS 1170.4/AS 3600 Section 14 — see
> [[concrete-earthquake-design-basis]]; ACI SDC/R/Ω_o concepts are **not**
> interchangeable with AS 1170.4's earthquake design category/μ/S_p.

## Summary

`[code]` Chapter 18 applies to nonprestressed and prestressed structures assigned
to **SDC B through F**, including (a) systems designated as part of the
seismic-force-resisting system (diaphragms, moment frames, structural walls,
foundations) and (b) members *not* designated as part of it but required to carry
other loads while undergoing earthquake deformations (Cl 18.1.1). Such structures
are intended to resist earthquake motion through **ductile inelastic response of
selected members** (Cl 18.1.2). SDC A structures are outside Chapter 18 (Cl 4.4.6.3,
see [[aci318-structural-system-requirements]]).

## Detail

### SDC routing and general rules (Cl 18.2)

`[code]` All structures are assigned an SDC per Cl 4.4.6.1 (Cl 18.2.1.1). All members
satisfy Chapters 1–17 and 19–26; Chapter 18 **governs** where it conflicts
(Cl 18.2.1.2). Which Chapter 18 sections apply:

- **SDC B**: Cl 18.2.2 (Cl 18.2.1.3).
- **SDC C**: Cl 18.2.2, 18.2.3 and 18.13 (Cl 18.2.1.4).
- **SDC D, E, F**: Cl 18.2.2 through 18.2.8 and 18.12–18.14 (Cl 18.2.1.5).

`[code]` Systems designated as seismic-force-resisting are restricted to those
permitted by the general building code. In addition to Cl 18.2.1.3–18.2.1.5
(Cl 18.2.1.6): ordinary moment frames satisfy Cl 18.3; ordinary reinforced
concrete structural walls need **no** Chapter 18 detailing beyond what
Cl 18.2.1.3/18.2.1.4 require; intermediate moment frames Cl 18.4; intermediate
precast walls Cl 18.5; special moment frames Cl 18.2.3–18.2.8 and 18.6–18.8;
precast special moment frames Cl 18.2.3–18.2.8 and 18.9; special structural walls
Cl 18.2.3–18.2.8 and 18.10; precast special structural walls Cl 18.2.3–18.2.8 and
18.11. A system not satisfying Chapter 18 may be used if experiment and analysis
show strength and toughness at least equal to a comparable compliant system
(Cl 18.2.1.7).

`[code]` **Analysis and proportioning** (Cl 18.2.2): the interaction of all
structural *and nonstructural* members affecting linear and nonlinear response
must be considered; rigid members assumed *not* part of the system are allowed if
their effect on system response is considered, and the consequences of their
failure are considered; members extending below the base to transmit earthquake
forces to the foundation comply with the Chapter 18 provisions consistent with
the system above. **Anchors** resisting earthquake forces in SDC C–F follow
Cl 17.10 (Cl 18.2.3.1 — see
[[aci318-anchoring-shear-interaction-seismic-and-shear-lugs]]); φ per Chapter 21
(Cl 18.2.4.1, including the Cl 21.2.4 seismic shear φ — see
[[aci318-strength-reduction-factors]]).

`[code]` **Special systems materials** (Cl 18.2.5–18.2.8): concrete strength per the
special seismic systems rows of Table 19.2.1.1; reinforcement per the special
seismic systems requirements of Cl 20.2.2. **Mechanical splices** are Type 1
(Cl 25.5.7) or Type 2 (Cl 25.5.7 *and* capable of developing the specified tensile
strength of the bars). Except Type 2 splices on Grade 420 bars, mechanical splices
may not lie within **twice the member depth** from the column/beam face (special
moment frames) or from critical yielding sections (Cl 18.2.7.2). **Welded splices**
conform to Cl 25.5.7 and likewise stay out of that zone; welding stirrups, ties,
inserts or similar elements to required longitudinal reinforcement is **not
permitted** (Cl 18.2.8).

### Ordinary moment frames (Cl 18.3)

`[code]` Beams have at least two continuous bars at top and bottom; continuous
bottom bars have area at least one-quarter of the maximum bottom-bar area along the
span and develop `f_y` at the support face (Cl 18.3.2). Columns with unsupported
length `ℓ_u ≤ 5c_1` need `φV_n` at least the lesser of (a) the shear from column
nominal moments at each restrained end in reverse curvature (flexural strength at
the factored axial force giving the highest strength), or (b) the maximum shear
from combinations with `E` replaced by `Ω_oE` (Cl 18.3.3). Beam-column joints
follow Chapter 15 with `V_u` at mid-height of the joint from beam nominal moments
(Cl 18.3.4 — see [[aci318-beam-column-and-slab-column-joints]]).

### Intermediate moment frames (Cl 18.4)

`[code]` Includes two-way slabs without beams that form part of the system
(Cl 18.4.1.1).

- **Beams** (Cl 18.4.2): two continuous top and bottom bars, continuous bottom
  steel ≥ ¼ the maximum bottom area, anchored for `f_y` at support; positive
  strength at the joint face ≥ **⅓** the negative strength there, and neither
  strength anywhere ≥ **⅕** the maximum strength at either joint face;
  `φV_n` ≥ the lesser of (a) shear from beam nominal moments at the ends (reverse
  curvature) plus factored gravity/vertical-earthquake shear, or (b) the maximum
  shear with `E` taken as **twice** the code value; hoops over **2h** from the
  support face at spacing ≤ the least of `d/4`, `8d_b` (smallest longitudinal bar),
  `24d_b` (hoop) and 300 mm, first hoop within 50 mm; transverse spacing ≤ `d/2`
  throughout; where factored axial compression exceeds `A_g f'c/10`, transverse
  steel conforms to Cl 25.7.2.2 and 25.7.2.3/25.7.2.4.
- **Columns** (Cl 18.4.3): `φV_n` ≥ the lesser of column-nominal-moment shear
  (as in Cl 18.3.3) and the maximum shear with `Ω_oE`; spirally reinforced per
  Chapter 10 or hoops over length `ℓ_o` from each joint face at spacing `s_o`
  ≤ the least of — Grade 420: smaller of `8d_b` and 200 mm; Grade 550: smaller of
  `6d_b` and 150 mm; and half the smallest column dimension — with `ℓ_o` ≥ the
  longest of one-sixth of the column clear span, the maximum cross-section
  dimension and 450 mm; first hoop within `s_o/2`; elsewhere per Cl 10.7.6.5.2. Columns
  supporting discontinuous stiff members (walls) have `s_o` transverse steel over
  the full height below if the earthquake axial force exceeds `A_g f'c/10`
  (`A_g f'c/4` if forces were amplified for overstrength).
- **Joints** (Cl 18.4.4): detailing of Cl 15.3.1.2, 15.3.1.3 plus Cl 18.4.4.2–18.4.4.5
  — strut-and-tie for beams deeper than twice the column depth; longitudinal bars
  extend to the far face of the joint core and are developed per Cl 18.8.5
  (tension) / Cl 25.4.9 (compression); joint spacing ≤ the Cl 18.4.3.3(a)–(c)
  values within the deepest beam; headed top beam bars need the column to extend
  one joint depth `h` above the joint (or equivalent added vertical joint steel).
  Joint shear strength `φV_n ≥ V_u` with `V_n` per Cl 18.8.4.3 (Table 18.8.4.3 — see
  [[aci318-special-moment-frames]]).
- **Two-way slabs without beams** (Cl 18.4.5): `M_sc` from combinations
  Eq. 5.3.1e/5.3.1g, steel in the column strip; reinforcement in the effective width
  (Cl 8.4.2.2.3) designed for `γ_f M_sc` (width not beyond `c_t` from the face at
  exterior/corner connections); ≥ half of column-strip support steel within that
  width; ≥ ¼ of column-strip top steel at the support continuous over the span;
  continuous bottom column-strip steel ≥ ⅓ of top steel at the support; ≥ half of
  bottom middle-strip and all bottom column-strip midspan steel continuous and
  developed for `f_y` at supports; all top and bottom steel at discontinuous edges
  developed at the support face. Two-way shear from factored gravity loads without
  moment transfer must not exceed `0.4φv_c` (nonprestressed) or `0.5φv_c` (unbonded
  post-tensioned with Cl 8.6.2.1 `f_pc`) at the Cl 22.6.4.1 critical section — waived
  if Cl 18.14.5 is satisfied (see
  [[aci318-earthquake-diaphragms-foundations-and-non-sfrs-members]]).

### Intermediate precast structural walls (Cl 18.5)

`[code]` In connections between wall panels, or between panels and foundation,
**yielding is restricted to steel elements or reinforcement** (Cl 18.5.2.1);
connection elements not designed to yield are proportioned for **1.5 S_y** of the
yielding portion (Cl 18.5.2.2). In SDC D–F, wall piers follow Cl 18.10.8 or
Cl 18.14 (Cl 18.5.2.3).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-structural-system-requirements]] — Cl 4.4.6 SDC and seismic-force-
  resisting-system routing.
- [[aci318-special-moment-frames]], [[aci318-special-structural-walls]],
  [[aci318-earthquake-diaphragms-foundations-and-non-sfrs-members]] — the rest of
  Chapter 18.
- [[concrete-earthquake-design-basis]], [[concrete-earthquake-imrf-detailing]] —
  the AS 3600 equivalents, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 18 Cl 18.1–18.5 (pp. 285–299).
