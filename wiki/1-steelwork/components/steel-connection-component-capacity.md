---
title: Connection component capacity — rectangular components (cleats, gussets, plates) and block shear
category: 1-steelwork
tags: [connection-components, gusset-plate, cleat, block-shear, rectangular-section, ASI-handbook-1]
standards: [AS 4100:2020 Cl 9.1.9, AS 4100:2020 Cl 5.11, AS 4100:2020 Cl 5.2, AS 4100:2020 Section 6, AS 4100:2020 Cl 7.2]
status: draft
reviewed: 2026-09-13
---

# Connection component capacity — rectangular components

> Scope: ASI Design Guide "Handbook 1 — Background and Theory: Design of
> Structural Steel Connections" (T.J. Hogan, first edition 2007) Ch 5 —
> standard angle/flat/plate component dimensions, and the derivation of
> shear, bending, axial compression, axial tension and block-shear design
> capacities for a **rectangular** connection component (cleat, gusset
> plate, bracket) treated as a beam/column/tie of section `d_i × t_i`.
> General component-capacity routing is at AS 4100 Cl 9.1.9, briefly noted
> on [[as4100-connection-design-requirements]]; this page derives the
> working formulas.

## Summary

`[code]` AS 4100 Cl 9.1.9 routes connection-component capacity to Sections
5 (bending, shear), 6 (compression) and 7 (tension), all at the
**connection-component `φ = 0.90`** (Table 3.4) — a higher factor than the
member-design `φ` values used elsewhere, reflecting the lower consequence
and more predictable behaviour of a short, stocky component.

`[practice]` For the common case of a rectangular component `d_i × t_i`
(cleat, gusset, bracket plate) treated as **compact** in bending about
either axis and short enough to preclude buckling in compression, the
handbook derives:

- `φV_v = 0.45 f_yi d_i t_i` (shear, Cl 5.11.3/5.11.4)
- `φM_s = 0.225 f_yi t_i d_i²` (major-axis bending) / `0.225 f_yi d_i t_i²`
  (minor-axis bending)
- `φN_s = 0.9 A_n f_yi` (axial compression, `k_f = 1.0`)
- `φN_t ≤ min[0.90 f_yi d_i t_i, 0.765 f_ui(d_i t_i − n_p d_h t_i)]`
  (axial tension)

`[derived]` For **block shear** in a rectangular component, this handbook
recommends the Kulak-based expression `φV_bs = φ[A_nt f_ui + 0.6 f_yi
A_gv]`, `φ = 0.75` — which is **not the same formula** as AS 4100's own
Cl 9.1.9(e) block-shear expression already on
[[as4100-connection-design-requirements]]. See Contradictions below.

## Detail

### Standard component dimensions (Ch 5.1–5.3)

`[practice]` Rationalised angle-leg thicknesses, gauge lines and flat/plate
sizes for detailing are tabulated in the source (Tables 26–31: equal
angles, unequal angles, gauge lines for angles, angle/flat/plate
strengths) — not reproduced here as routine steel-catalogue reference data
rather than design theory; see the source PDF for the full tables.

`[derived]` Typical rectangular-component applications: end plates (flexible
or rigid), column base plates, fin/web-side plates, gusset plates,
stiffeners, splice plates. Standard plate thicknesses (Grade 250 to
AS/NZS 3678): 5, 6, 8, 10, 12, 16, 20, 25, 28, 32, 36, 40, 45, 50 mm.

### Rectangular component geometry (Ch 5.4)

![[asi-h1-fig-45-rectangular-component-geometry.png]]
*Figure 45 — rectangular connection component geometry: depth `d_i`,
thickness `t_i`, optional line of `n_p` holes of diameter `d_h` at pitch
`s_p` (ASI Handbook 1, 2007).*

### Design shear capacity (Ch 5.4)

`[code]` Since shear stress across a rectangular section is non-uniform,
Cl 5.11.3 applies: `V_v = 2V_u / [0.9 + (f*_vm/f*_va)] ≤ V_u`, where `V_u`
(Cl 5.11.2/5.11.4, no hole allowance needed) = `V_w = 0.6 f_yi d_i t_i`.

`[derived]` For a rectangular section under shear `V*`: `f*_vm/f*_va = 1.5`
(elastic parabolic shear stress distribution, `I = t_i d_i³/12`,
`Q = t_i d_i²/8`, `b = t_i`). Substituting:

`V_v = 2V_u/(0.9+1.5) = 0.833V_u = 0.50 f_yi d_i t_i`

`φV_v = 0.9 × 0.50 f_yi d_i t_i = 0.45 f_yi d_i t_i ≥ V*`

### Design moment capacity — major and minor axis (Ch 5.4)

`[code]` A rectangular component bent about either axis is compact in most
connections (Cl 5.2.1, `M_s = f_yi Z_e`; Cl 5.2.3, `Z_e` = lesser of `S`
and `1.5Z`). Major axis: `S = t_i d_i²/4`, `1.5Z = 1.5 t_i d_i²/6 = t_i
d_i²/4` — identical, so `Z_e = t_i d_i²/4` always governs.

`M_s = f_yi t_i d_i²/4`, `φM_s = 0.225 f_yi t_i d_i² ≥ M*`

![[asi-h1-fig-46-47-component-major-minor-axis-bending.png]]
*Figure 46 (major axis) and Figure 47 (minor axis) — rectangular component
bending orientations (ASI Handbook 1, 2007).*

`[derived]` Local buckling in flexure is not normally a governing concern
for connection components — Table 5.2 of AS 4100 has no plasticity
slenderness limit for an unsupported-both-edges element in combined
tension/compression bending (the loading a rectangular component sees), and
attachment to the connected member usually prevents it in practice.
Cl 5.2.6's hole allowance applies only to flanges, which a rectangular
component (Figure 46) does not possess, so it does not apply here.

`[code]` Minor axis (Figure 47): `Z_e = d_i t_i²/4` similarly governs;
`φM_s = 0.225 f_yi d_i t_i² ≥ M*`.

### Design capacity in axial compression (Ch 5.4)

`[practice]` Connection components are usually short enough that only
gross-section yielding governs (no local/member buckling) — Cl 6.2.1,
`N_s = k_f A_n f_yi`, `k_f = 1.0` in the absence of local buckling,
`A_n = A_g = d_i t_i` (holes filled with bolts) or `d_i t_i − n_p d_h t_i`
if unfilled holes reduce the gross area by more than `100{1-[f_y/(0.85f_u)]}%`
(Cl 6.2.1).

`φN_s = 0.9 A_n f_yi ≥ N*`

### Design capacity in axial tension (Ch 5.4)

`[code]` Cl 7.2: `N_t` = lesser of `A_g f_yi` and `0.85 k_t A_n f_ui`;
`k_t = 1.0` for the usual uniform force distribution in a connection
component (Cl 7.3). `A_g = d_i t_i`, `A_n = d_i t_i − n_p d_h t_i`
(Figure 48).

`φN_t ≤ 0.90 f_yi d_i t_i` and `≤ 0.765 f_ui(d_i t_i − n_p d_h t_i) ≥ N*`

![[asi-h1-fig-48-component-axial-tension.png]]
*Figure 48 — rectangular component design capacity in axial tension:
hole geometry `d_h`, `s_p`, `n_p` (ASI Handbook 1, 2007).*

### Block shear rupture (Ch 5.4)

`[practice]` AS 4100 (as of this handbook's 2007 edition) did not itself
address block shear rupture; the handbook adopts the AISC Specification
(Ref. 22, Cl J4.3) / Kulak (Ref. 11) treatment, distinguishing block shear
in **connection components** (gusset plates, cleats, angles — this
Section) from block shear in **coped beam webs** (a supported member —
see [[steel-coped-beam-capacity]]).

![[asi-h1-fig-49-block-shear-failure-examples.png]]
*Figure 49 — block shear failure examples: (a) a gusset plate in tension
tearing out diagonally through a bolt group; (b) a cleat in shear pulling
out and down along a bolt line (after Ref. 11) (ASI Handbook 1, 2007).*

`[derived]` Test evidence (Ref. 11) shows block shear is a **combined**
shear + tension rupture mechanism: the tension-loaded region fractures
through the bolt holes (net section); the shear-loaded region yields on a
plane roughly parallel to the load but generally **not** through the bolt
holes, and tension-plane fracture is reached before shear-plane fracture.

`[practice]` **AISC Cl J4.3 general form**:
`φV_bs = φ[0.6 f_u A_nv + f_u A_nt U_bs] ≤ φ[0.6 f_y A_gv + f_u A_nt U_bs]`,
`φ = 0.75`, `U_bs = 1.0` (uniform tension stress) or `0.5` (non-uniform).

`[practice]` **Recommended design expression for connection components**
(Kulak, Ref. 11, and adopted by this handbook):

`φV_bs = φ[A_nt f_ui + 0.6 f_yi A_gv]`, `φ = 0.75`

— i.e. **tension always at rupture** (`f_ui`, net area) combined with
**shear always at yield** (`f_yi`, gross area), without the AISC
upper/lower-bound selection logic. `A_nt`, `A_gv` per Figure 50 (shear-force
and tension-force block-shear area definitions, accounting for the number
and pitch of holes each region crosses).

![[asi-h1-fig-50-block-shear-area-components.png]]
*Figure 50 — block shear area definitions for shear-force and
tension-force cases: `A_nt = (l_t − 0.5d_h)t_i` or `(l_t − 1.5d_h)t_i`
(single vs double line of holes in the shear region), `A_gv = l_v t_i`;
tension-region `A_nt = [l_t − (n_h−1)d_h]t_i` (ASI Handbook 1, 2007).*

`[practice]` A separate UK reference (Steel Construction Institute, Ref. 24)
takes a shear-**yielding**-based approach rather than shear rupture — a
further indication that block-shear treatment was not settled/harmonised
across steel design guidance as of this handbook's writing.

## Worked reference

None yet — no fully worked block-shear or component-capacity example in
this chapter of the source (worked examples resume in Ch 6, see
[[steel-coped-beam-capacity]]).

## Contradictions

`[practice]` **Block shear formula divergence.** AS 4100 Cl 9.1.9(e)
(already on [[as4100-connection-design-requirements]]) gives:

`R_bs = 0.6 f_uc A_nv + k_bs f_uc A_nt ≤ 0.6 f_yc A_gv + k_bs f_uc A_nt`,
`φ = 0.75`

— i.e. shear **always at rupture** (`f_u`), tension at rupture scaled by
`k_bs` (1.0 uniform / 0.5 non-uniform), the whole expression **capped** by
substituting shear yield (`f_y`) for shear rupture.

This handbook's Ch 5.4 recommends instead (from Kulak/AISC, predating or
independent of the current AS 4100 Cl 9.1.9(e) text): `φV_bs = φ[A_nt f_ui
+ 0.6 f_yi A_gv]` — i.e. shear **always at yield** (`f_y`, not `f_u`),
tension always at full rupture (`f_u`, no `k_bs` reduction), no cap/
selection logic.

The two formulas are **not algebraically equivalent** and can give
materially different capacities for the same geometry (the AS 4100 formula
is capped from above by a shear-yield term but its uncapped branch uses
shear rupture `f_u > f_y`; the handbook formula always uses shear yield).
Since the current AS 4100:2020 Cl 9.1.9(e) postdates this 2007 handbook and
is the applicable code clause, **Cl 9.1.9(e) governs** for AS 4100
compliance — this handbook's Ch 5.4 expression is retained here only as
useful background on the block-shear mechanism and the AISC/Kulak
derivation AS 4100's own clause is descended from. Flagged to the human:
confirm which formula a given calculation should cite before use.

`[practice]` A **third** variant appears on [[steel-coped-beam-capacity]]
(Ch 6.9, coped beam webs): `φV_bs = φ[0.5A_ntf_ui + 0.6f_yiA_gv]` — the
same form as this page's formula but with an extra `0.5` factor on the
tension term, reflecting the single-shear-surface/rotating-block failure
mechanism specific to a coped web (vs the two-surface mechanism in a
gusset plate). Match the formula to the element being checked.

## Related

- [[as4100-connection-design-requirements]] — AS 4100 Cl 9.1.9 routing and
  the current Cl 9.1.9(e) block-shear formula (see Contradictions above).
- [[steel-coped-beam-capacity]] — block shear in a coped beam web
  (supported member), the companion case to this page's connection
  components.
- [[as4100-beam-section-moment-capacity]] — Cl 5.2 section moment capacity
  general provisions.
- [[as4100-web-shear-and-bearing]] — Cl 5.11 shear capacity general
  provisions.
- [[as4100-tension-member-capacity]] — Cl 7.2 tension capacity general
  provisions.

## Sources

- `raw/1-steelwork/ASI - Handbook 1 - Background and Theory - Design of
  Structural Steel Connections.pdf`, Ch 5.1–5.4 (pp. 77–85). Figures 45–50
  reproduced in `wiki/1-steelwork/assets/`; Tables 26–31 (angle/flat/plate
  dimension and strength reference tables) not reproduced — routine
  steel-catalogue data, see the source PDF.
