---
title: ACI 318M-19 special moment frames — beams, columns, joints and precast frames
category: 2-concrete
tags: [aci, earthquake, seismic, special-moment-frame, confinement, capacity-design]
standards: [ACI 318M-19 Cl 18.6, ACI 318M-19 Cl 18.7, ACI 318M-19 Cl 18.8, ACI 318M-19 Cl 18.9]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 special moment frames

> Scope: ACI 318M-19 Cl 18.6 (beams), 18.7 (columns), 18.8 (joints) and 18.9
> (precast special moment frames) — dimensional limits, flexural strength
> hierarchy, confinement and shear design using probable moment strength. SDC
> routing and general materials/splice rules are on
> [[aci318-earthquake-general-and-ordinary-intermediate-frames]]. This is an
> **ACI 318M-19 page, kept separate from the AS 3600:2018 concept pages**
> elsewhere in `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Special moment frames get the highest ductility provisions: beams
(Cl 18.6) frame into columns (Cl 18.7) that satisfy their own limits
(Cl 18.6.1.2), joints (Cl 18.8) are detailed for forces computed with **1.25f_y**
steel stress, and member shears are derived from **probable flexural strength
`M_pr`** (capacity design) rather than analysis. Precast versions (Cl 18.9)
must also satisfy the cast-in-place provisions or be proven by testing.

## Detail

### Beams (Cl 18.6)

`[code]` Beams are proportioned primarily for flexure and shear (Cl 18.6.1.1).
**Dimensional limits**: clear span `ℓ_n ≥ 4d`; width `b_w ≥` the lesser of `0.3h` and
250 mm; beam width projecting beyond the column on each side ≤ the lesser of `c_2`
and `0.75c_1` (Cl 18.6.2.1). **Longitudinal steel** (Cl 18.6.3): at least two
continuous bars top and bottom; steel at least Cl 9.6.1.2 minimum with `ρ ≤ 0.025`
(Grade 420) or `0.02` (Grade 550); positive-moment strength at the joint face ≥
**½** the negative-moment strength there, and neither strength at any section
< **¼** the maximum at either joint face. Lap splices only if hoops/spirals cover
the lap at spacing ≤ the lesser of `d/4` and 100 mm, and **never** within the joint,
within `2×` beam depth of the joint face, or within `2×` beam depth of critical
yielding sections; mechanical/welded splices per Cl 18.2.7/18.2.8. Prestressing
(unless permitted by Cl 18.9.2.3) is limited: average `f_pc ≤` the lesser of 3.5 MPa
and `f'c/10`; unbonded in plastic hinge regions with strain under design
displacement < 0.01; contributes ≤ ¼ of positive or negative flexural strength at
the critical section; anchorages capable of 50 load cycles between 40% and 85%
of tensile strength (Cl 18.6.3.5).

`[code]` **Transverse steel** (Cl 18.6.4): hoops over **2× beam depth** from the
column face at each end, and over 2× beam depth on both sides of any section where
flexural yielding is likely beyond the elastic range. Primary longitudinal bars
nearest the tension/compression faces are laterally supported (Cl 25.7.2.3/
25.7.2.4) at spacing ≤ 350 mm; hoops may be a stirrup with seismic hooks closed by
a crosstie, 90° hooks alternated side to side. First hoop within **50 mm** of the
column face; spacing ≤ the least of `d/4`, 150 mm, `6d_b` (Grade 420) or `5d_b`
(Grade 550) of the smallest primary flexural bar. Where hoops aren't required,
stirrups with seismic hooks at ≤ `d/2`. Beams with factored axial compression above
`A_g f'c/10` use column-type hoops (Cl 18.7.5.2–18.7.5.4) along the Cl 18.6.4.1
lengths and tighter spacing elsewhere, with extra cover steel if cover over hoops
exceeds 100 mm.

`[code]` **Design shear `V_e`** (Cl 18.6.5): from the free body of the beam between
joint faces, with moments of opposite sign equal to **probable flexural strength
`M_pr`** (steel stress 1.25f_y) acting at the joint faces and factored gravity and
vertical earthquake load along the span:

![[aci318-fig-r18.6.5-design-shears-beams-columns.png]]
*Fig. R18.6.5 — design shears for beams and columns: `V_e = (M_pr1 + M_pr2)/ℓ_n ±
w_uℓ_n/2` for beams with `w_u = (1.2 + 0.2S_DS)D + 1.0L + 0.2S`; column
`V_e3,4 = (M_pr3 + M_pr4)/ℓ_u` (ACI 318M-19).* Transverse steel over the Cl 18.6.4.1
lengths is designed with **`V_c = 0`** when both (a) the earthquake-induced shear
is at least half the maximum required shear strength in those lengths and (b)
`P_u < A_g f'c/20` (Cl 18.6.5.2).

### Columns (Cl 18.7)

`[code]` **Dimensional limits**: shortest cross-section dimension ≥ **300 mm** and
ratio of shortest to perpendicular dimension ≥ **0.4** (Cl 18.7.2.1).
**Strong-column/weak-beam**: `ΣM_nc ≥ (6/5)ΣM_nb` at each joint, column strengths
computed at the factored axial force giving the **lowest** column strength and
summed so column moments oppose beam moments, for both beam moment directions;
slab steel within the Cl 6.3.2 effective width counts toward `M_nb` if developed at
the critical section (Cl 18.7.3.2). Exempt where the column is discontinuous above
and `P_u < A_g f'c/10`; if not satisfied, those columns' lateral strength/stiffness
is ignored and they satisfy Cl 18.14 (Cl 18.7.3.1, 18.7.3.3).

`[code]` **Longitudinal steel**: `0.01A_g ≤ A_st ≤ 0.06A_g`; at least six bars with
circular hoops; selected so `1.25ℓ_d ≤ ℓ_u/2` over the clear height; lap splices only
in the **centre half** of the member, as tension splices, within Cl 18.7.5.2/18.7.5.3
transverse steel (Cl 18.7.4).

`[code]` **Transverse reinforcement** (Cl 18.7.5), over length `ℓ_o` from each joint
face and both sides of any likely-yielding section, `ℓ_o ≥` the greatest of the
column depth at that section, one-sixth of the clear span, and 450 mm: single or
overlapping spirals, circular hoops, or rectilinear hoops with/without crossties
(bends engage peripheral bars; consecutive crossties alternate end for end);
spacing `h_x` of laterally supported longitudinal bars ≤ **350 mm**, and ≤ **200 mm**
with every perimeter bar supported when `P_u > 0.3A_g f'c` or `f'c > 70 MPa`.
Spacing ≤ the least of ¼ the minimum column dimension, `6d_b` (Grade 420) or `5d_b`
(Grade 550) of the smallest longitudinal bar, and `s_o = 100 + (350 − h_x)/3`
(limited to 100–150 mm) (Eq. 18.7.5.3). Amount per:

![[aci318-table-18.7.5.4-transverse-reinforcement-special-moment-frame-columns.png]]
*Table 18.7.5.4 — transverse reinforcement for special moment frame columns:
rectilinear `A_sh/sb_c` = greater of `0.3(A_g/A_ch − 1)f'c/f_yt` and `0.09f'c/f_yt`
(and `0.2k_f k_n P_u/(f_yt A_ch)` when `P_u > 0.3A_g f'c` or `f'c > 70 MPa`); spiral/
circular `ρ_s` = greater of `0.45(A_g/A_ch − 1)f'c/f_yt` and `0.12f'c/f_yt` (and
`0.35k_f P_u/(f_yt A_ch)` in the high-load/strength case) (ACI 318M-19).*
`k_f = f'c/175 + 0.6 ≥ 1.0` and `k_n = n_l/(n_l − 2)` (confinement effectiveness,
`n_l` = laterally supported bars) (Eq. 18.7.5.4a/b).

`[code]` Beyond `ℓ_o`: spiral or hoop+crosstie at ≤ 150 mm, `6d_b` (G420) or `5d_b`
(G550) (Cl 18.7.5.5). Columns supporting discontinued stiff members (walls)
carry Cl 18.7.5.2–18.7.5.4 steel over the full height below if earthquake axial
compression exceeds `A_g f'c/10` (`A_g f'c/4` with overstrength-amplified forces),
extending `ℓ_d` into the discontinued member (300 mm into a footing/mat)
(Cl 18.7.5.6). If cover outside the confining steel exceeds 100 mm, extra
transverse steel with cover ≤ 100 mm at ≤ 300 mm is required (Cl 18.7.5.7).

`[code]` **Shear** (Cl 18.7.6): `V_e` from `M_pr` at each column end over the range of
factored `P_u`, not exceeding the shear from the framing beams' `M_pr` at the joint,
and not less than analysis shear (Cl 18.7.6.1.1); transverse steel over `ℓ_o` designed
with `V_c = 0` when the earthquake shear is ≥ half the maximum required in `ℓ_o`
**and** `P_u < A_g f'c/20` (Cl 18.7.6.2.1).

### Joints (Cl 18.8)

`[code]` Beam longitudinal steel force at the joint face assumes stress **1.25f_y**
(Cl 18.8.2.1); bars terminating in the joint extend to the far face of the core and
develop per Cl 18.8.5 (tension) and Cl 25.4.9 (compression) (Cl 18.8.2.2). Where
beam bars run through the joint, joint depth `h` parallel to them is at least the
greatest of `20d_b/λ` (largest Grade 420 bar), `26d_b` (largest Grade 550 bar) and
half the depth of any beam generating joint shear (Cl 18.8.2.3); joints with
Grade 550 longitudinal steel use normalweight concrete (Cl 18.8.2.3.1).

`[code]` Joint transverse steel meets Cl 18.7.5.2–18.7.5.4 and 18.7.5.7, but where
beams frame into all four sides and each is ≥ ¾ the column width, the amount may be
halved and spacing relaxed to 150 mm within the shallowest beam depth (Cl 18.8.3);
beam steel outside the column core is confined by transverse steel through the
column unless a framing beam does so (Cl 18.8.3.3). **Joint shear** `V_u` is taken on
a mid-height plane from beam forces using 1.25f_y and column shear consistent with
beam `M_pr` (Cl 18.8.4.1), with φ per Cl 21.2.4.4 (0.85, see
[[aci318-strength-reduction-factors]]) and `V_n` from:

![[aci318-table-18.8.4.3-nominal-joint-shear-strength-special-moment-frame.png]]
*Table 18.8.4.3 — nominal joint shear strength `V_n` (`λ√f'c A_j`, N): 1.7 (column
and beam continuous/extended, confined) down to 0.7 (neither continuous, not
confined), with 1.2 and 1.0 intermediate cases (ACI 318M-19).* `A_j` per
Cl 15.4.2.4. `[derived]` Every coefficient is lower than the matching entry of
Table 15.4.2.3 (e.g. 1.7 vs 2.0 for the best-confined case) — the special-frame
joint is allowed less shear stress because it must survive inelastic reversals.

`[code]` **Development** (Cl 18.8.5): hooked bars No. 10–36: `ℓ_dh = f_y d_b/(5.4λ√f'c)`
but not less than `8d_b` and 150 mm (normalweight; `10d_b` and 190 mm lightweight),
hook inside the confined core turned into the joint (Eq. 18.8.5.1); headed bars per
Cl 25.4.4 with 1.25f_y; straight bars at least **2.5×** (≤ 300 mm concrete below) or
**3.25×** (> 300 mm below) the hooked length, passing through the confined core with
any portion outside it increased by **1.6** (Cl 18.8.5.3–18.8.5.4); epoxy-coated
factors per Cl 25.4.

### Precast special moment frames (Cl 18.9)

`[code]` Ductile-connection frames satisfy Cl 18.6–18.8, with connection `V_n`
(shear-friction, Cl 22.9) at least **2V_e**, and mechanical splices of beam steel at
least `h/2` from the joint face (Cl 18.9.2.1). Strong-connection frames satisfy
Cl 18.6–18.8, apply Cl 18.6.2.1(a) between intended yielding locations, have
`φS_n ≥ S_e`, continuous primary steel developed outside the connection and hinge
region, and for column-to-column connections `φS_n ≥ 1.4S_e`, `φM_n ≥ 0.4M_pr`,
`φV_n ≥ V_e` (Cl 18.9.2.2). Frames meeting neither need ACI 374.1 testing with
representative details and a defined resisting mechanism (Cl 18.9.2.3).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-earthquake-general-and-ordinary-intermediate-frames]] — Cl 18.1–18.5.
- [[aci318-special-structural-walls]] — Cl 18.10–18.11.
- [[aci318-beam-column-and-slab-column-joints]] — Chapter 15 ordinary-joint
  provisions this section tightens.
- [[concrete-earthquake-imrf-detailing]] — the AS 3600 intermediate-frame
  equivalent, for structural comparison only (AS 3600 has no special moment frame
  tier).

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 18 Cl 18.6–18.9 (pp. 299–317),
  incl. Tables 18.7.5.4, 18.8.4.3 and Fig. R18.6.5.
