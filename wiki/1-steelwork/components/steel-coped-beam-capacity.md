---
title: Supported member capacity — uncoped, single and double web coped beams, block shear, web reinforcement
category: 1-steelwork
tags: [coped-beam, web-cope, block-shear, section-moment-capacity, shear-capacity, ASI-handbook-1]
standards: [AS 4100:2020 Cl 5.2, AS 4100:2020 Cl 5.11, AS 4100:2020 Cl 5.12, AS 4100:2020 Cl 5.13, AS 4100:2020 Cl 14.3.3]
status: draft
reviewed: 2026-09-13
---

# Supported member capacity — coped beams

> Scope: ASI Design Guide "Handbook 1 — Background and Theory: Design of
> Structural Steel Connections" (T.J. Hogan, first edition 2007) Ch 6 —
> local section moment/shear capacity of a **supported member** near a
> connection, for uncoped, single-web-coped (SWC) and double-web-coped
> (DWC) sections, plus block shear and web reinforcement of coped ends.
> This is the "supported member" element of connection design (element (C)
> in [[steel-connection-classification-and-design-philosophy]]) — the
> companion case to [[steel-connection-component-capacity]] (element (B)).

## Summary

`[practice]` Only **section** capacity (not member capacity — buckling
over a length) is relevant locally at a connection, since a cope is short.
Design capacities are derived from AS 4100 Cl 5.2 (moment), 5.11–5.13
(shear, shear-moment interaction) for uncoped sections, and from
first-principles tee/rectangle section properties (with AISC/Kulak-derived
block shear) for coped sections, since AS 4100 itself gives no coping
provisions. Key design capacities:

- Uncoped: `φM_sx = φf_yZ_ex` (Cl 5.2.1), `φV_vo = 0.54f_yA_w` (typical
  rolled/welded I-section, web slender-ratio within limit).
- Single web cope (SWC, a tee section): `φM_ss = 0.9f_yZ_e` (`Z_e` from
  tee-section `S_s`/`Z_s`), `φV_ws = 0.9V_v` (non-uniform shear stress
  factor from `Q_c`, `I_x`).
- Double web cope (DWC, a rectangle `d_w × t_w`): `φM_sd = 0.225f_yt_wd_w²`,
  `φV_wd = 0.45f_yt_wd_w`.
- Block shear in a coped web: `φV_bs = φ[0.5A_nt f_ui + 0.6f_yiA_gv]`,
  `φ = 0.75` — **note the 0.5 factor**, different from the connection-
  component formula on [[steel-connection-component-capacity]] (see
  Contradictions there).
- AS 4100 Cl 14.3.3 requires the re-entrant corner at a cope to be
  radiused ≥ 10 mm.

## Detail

### General (Ch 6.1)

`[code]` Only **section** capacity matters locally at a connection (member
capacity/buckling is assessed separately as part of overall member design).
Relevant limit states: moment and shear (yield and buckling), derived using
AS 4100 Cl 5.2, 5.11, 5.12, 5.13. `[practice]` Keep cope length and depth as
small as practical so the connection design capacity, not the coped
member's local capacity, governs; AS 4100 Cl 14.3.3 requires the
re-entrant corner at a cope to be radiused to at least 10 mm.

### Uncoped sections (Ch 6.2)

`[code]` `M_s = f_yZ_e` (Cl 5.2.1); `Z_e = Z_c` if compact, else linear
interpolation between `Z` and `Z_c` by slenderness (Cl 5.2.3/5.2.4);
`Z_c = min[S, 1.5Z]`. Rolled-section slenderness limits: `λ_ep = 9`
(flange)/`82` (web); `λ_ey = 16`(flange)/`115`(web). Welded: `λ_ep = 8`
(flange)/`82`(web); `λ_ey = 15`(flange)/`115`(web).

`[practice]` Where flange holes exceed the Cl 5.2.6 deduction-free limit
(`100{1-[f_y/(0.85f_u)]}%` of flange area — e.g. 14.4–25.1% for Grade 300
rolled sections depending on `f_y`, 15.2–23.4% for Grade 300 welded plate
depending on `f_y`), the handbook derives exact `Z'`/`S'` formulas for
holes in both flanges (Figure 51) and one flange (Figures 52, 53) — more
exact than AS 4100's own simplified method (a) (`Z' = (A_n/A)Z`). No
deduction is required for web holes (Cl 5.2.6 only addresses flanges).

![[asi-h1-fig-51-section-holes-both-flanges.png]]
*Figure 51 — I-section with holes in both flanges: net section properties
`A'`, `I'_x`, `Z'_x`, `S'_x` (ASI Handbook 1, 2007).*

![[asi-h1-fig-52-section-holes-one-flange.png]]
*Figure 52 — I-section with holes in the bottom flange only: neutral-axis
shift `Δy`, `y_bh`, `y_th`, holed `A'`, `I'_x` and `Z'_x` (ASI Handbook 1,
2007).*

![[asi-h1-fig-53-section-holes-one-flange.png]]
*Figure 53 — I-section with holes in one flange: plastic neutral axis
shift `y_bp`, net plastic modulus `S'_x` (ASI Handbook 1, 2007).*

`[code]` Shear (Cl 5.11.1–5.11.4): for `d_p/t_w ≤ 82/√(f_y/250)`,
`φV_vo = 0.54f_yA_w` (`A_w = d_pt_w` welded / `dt_w` rolled); AS 4100
requires no adjustment for web bolt holes (assumed filled). Shear-moment
interaction (Cl 5.12.3): `V_vm = V_v` for `M* ≤ 0.75φM_s`, else
`V_v[2.2-(1.6M*/φM_s)]` up to `M* = φM_s`.

`[practice]` Ready-reference design capacities for Grade 300 UB, PFC and
welded beam sections (unholed / holed one flange / holed two flanges):

![[asi-h1-table-32-ub-pfc-section-moment-web-capacities.png]]
*Table 32A/B — universal beam and parallel flange channel design section
moment (`φM_sx`) and web shear (`φV_v`) capacities, Grade 300, with 22 mm
hole allowance (ASI Handbook 1, 2007).*

`[derived]` (Table 32C, welded beams 700WB–1200WB, not reproduced here —
same structure, 24 mm holes — see the source.) Worked example 6 in the
source (250UB31.4, `f_y = 320 MPa`) walks the full non-compact-section
`Z_ex` interpolation and one/two-flange hole-deduction calculation
end-to-end — a useful template for a section not covered by Table 32.

### Single web coped (SWC) sections (Ch 6.4)

`[practice]` A SWC section (Figure 54) is a **tee section** in
cross-section at the cope — genuinely different section behaviour from the
parent I-section, requiring its own `Z_e`.

![[asi-h1-fig-54-single-web-coped-sections.png]]
*Figure 54 — single web coped (SWC) sections: cope length `L_c`, min. 10 mm
corner radius, web depth `d_w`, tee depth `d_wt` (ASI Handbook 1, 2007).*

`[practice]` Slenderness limits specific to the tee (differ from the
parent I-section limits above, reflecting one edge free / one edge
supported): `λ_ep = 9` (flange outstand or web, uniform or max-compression-
at-unsupported-edge behaviour); `λ_ey = 16` (flange outstand) / `25` (web).
Local web buckling is assumed **not** to govern for a SWC section — cope
lengths are typically 100–150 mm and the connection itself stiffens the
web locally (Ref. 9 makes the same assumption); where this needs checking
explicitly, a Cheng-et-al-based elastic critical stress `f_cr` method is
given (not reproduced in full here — see the source, Ch 6.4).

`[practice]` `Z_e = [S_s, 1.5Z_s]_min` (tee section, full section assumed
effective locally). Elastic modulus `Z_s` derived from first-principles tee
properties (`I_x`, `y_c`, Figure 56); plastic modulus `S_s` derived
separately for the two possible plastic-neutral-axis positions — in the
web (Figure 57) or in the bottom flange (Figure 58) — depending on the
tee's proportions. `φM_ss = 0.9f_yZ_e`, `f_y = min(f_yf, f_yw)`.

![[asi-h1-fig-55-swc-ub-notation.png]]
*Figure 55 — SWC universal beam notation: `L_c`, `d_w`, `t_f`, section A-A
where properties are calculated (ASI Handbook 1, 2007).*

`[code]` Shear (non-uniform stress distribution in a tee, Cl 5.11.1/
5.11.3): `φV_ws = 0.9 × 2V_u/[0.9 + Q_cd_w/I_x] ≤ 0.54f_yd_wt_w`, where
`Q_c` is the first moment of area of the tee about its elastic neutral
axis and `V_u = 0.6f_yd_wt_w`. Shear-moment interaction per Cl 5.12.3 as
for uncoped sections, with `V_v = V_ws`, `M_s = M_ss`.

`[practice]` Ready-reference SWC design capacities (Grade 300, 65 mm cope
depth):

![[asi-h1-table-33-swc-section-capacities.png]]
*Table 33A — single web coped universal beam design section moment
(`φM_ss`) and shear (`φV_ws`) capacities, Grade 300, 65 mm cope
(ASI Handbook 1, 2007).* (Table 33B, PFC sections, and the PFC-specific
`I_x`/`y_c`/`Q_c`/`S_s` formula variations, are in the source but not
reproduced here.)

#### Worked example 7 — SWC universal beam (Ch 6.5)

`[derived]` A 410UB53.7 Grade 300 beam, cope 120 mm long × 65 mm deep
(Figure 59), gives `φM_ss = 97.2 kNm` and `φV_ws = 387 kN` (< the
uniform-shear upper bound of 429 kN) — matching Table 33A directly. The
worked calculation is a direct template for any section not in Table 33.

![[asi-h1-fig-59-swc-worked-example.png]]
*Figure 59 — SWC universal beam worked example geometry (ASI Handbook 1,
2007).*

### Double web coped (DWC) sections (Ch 6.6)

`[practice]` A DWC section (Figure 60) leaves a plain rectangular web
`d_w × t_w` — both edges unsupported, but local buckling in the triangular
compression zone above the neutral axis is assumed not to govern locally
(same rationale as SWC; Ref. 9 concurs). Treating it as the rectangular
component of [[steel-connection-component-capacity]] Ch 5.4:

`Z_e = t_wd_w²/4`, `φM_sd = 0.225f_yt_wd_w²`

![[asi-h1-fig-60-double-web-coped-sections.png]]
*Figure 60 — double web coped (DWC) sections: cope depths `d_ct` (top),
`d_cb` (bottom), web depth `d_w` (ASI Handbook 1, 2007).*

`[practice]` Where local buckling **is** to be checked (Ref. 9 Part 9,
Cheng et al.): `φM_sd = 0.9f_crZ_x`, with `f_cr` a function of `t_w`,
`L_c`, `d_w`, a plate-buckling adjustment factor `f_d` (depends on
`d_ct/d`), and a coefficient `K` tabulated against `2L_c/d_w` (from 16 at
`2L_c/d_w=0.25` down to 0.425 at `2L_c/d_w≥4`) — not reproduced in full
here, see the source.

`[code]` Shear: `φV_wd = 0.45f_yt_wd_w` (uniform stress in the rectangular
web, same derivation as [[steel-connection-component-capacity]]'s
rectangular-component shear capacity). Shear-moment interaction per
Cl 5.12.3 with `V_v = V_wd`, `M_s = M_sd`. `[code]` Since a DWC section has
no flanges, Cl 5.2.6's hole-deduction rule (flanges only) never applies to
web holes in a DWC section.

![[asi-h1-fig-61-elastic-na-dwc-section.png]]
*Figure 61 — elastic neutral axis in a DWC section vs the parent uncoped
section's neutral axis (ASI Handbook 1, 2007).*

`[practice]` Ready-reference DWC design capacities (Grade 300, 65 mm top
cope):

![[asi-h1-table-34-dwc-section-capacities.png]]
*Table 34A/B — double web coped universal beam and PFC design section
moment (`φM_sd`) and shear (`φV_wd`) capacities, Grade 300
(ASI Handbook 1, 2007).*

#### Worked example 8 — DWC universal beam (Ch 6.7)

`[derived]` The same 410UB53.7 Grade 300 beam as example 7, now double-web
coped (`d_w = 285 mm`, `t_w = 7.6 mm`): `φM_sd = 44.4 kNm`,
`φV_wd = 312 kN` — matching Table 34A directly.

![[asi-h1-fig-62-dwc-worked-example.png]]
*Figure 62 — DWC universal beam worked example geometry (ASI Handbook 1,
2007).*

### Lateral torsional buckling of coped ends (Ch 6.8)

`[practice]` Connection components and coped sections are generally short
enough that lateral torsional buckling of neither the connection elements
nor the coped section itself governs — but an exceptionally long cope can
reduce the elastic critical buckling moment of the whole (laterally
unrestrained) member. AS 4100 gives no specific guidance on the effect of
web coping on member buckling capacity; the handbook recommends either a
buckling analysis (Ref. 28, permitted by Cl 5.6.4) or conservatively
assuming only **partial restraint** at the coped end when evaluating the
twist restraint factor `k_t` and lateral restraint factor `k_r`
(Cl 5.6.3). `[derived]` `k_r = 1.0` should always be used for a member
connected only by angle cleats or web plates (coped or not), since these
connections provide no restraint to the top flange.

### Block shear failure of coped sections (Ch 6.9)

`[practice]` A coped member web can fail by a block of material pulling
out (Figure 63) — the coped-section analogue of the connection-component
block shear on [[steel-connection-component-capacity]]. The failure mode
differs from a gusset plate: a coped beam has shear resistance on only
**one** surface (vs two for a gusset plate), so the failing block must
**rotate** as it pulls out. Tensile fracture occurs on the horizontal net
section through the bolt holes, but the tensile stress is non-uniform
(higher toward the web end); relatively little test data exists for this
specific case (Ref. 11).

![[asi-h1-fig-63-block-shear-coped-sections.png]]
*Figure 63 — block shear failure in coped beam webs: SWC (left) and DWC
(right), showing the block rotating as it pulls out (ASI Handbook 1,
2007).*

`[practice]` **Recommended design capacity for coped beam webs** (Kulak,
Ref. 11):

`φV_bs = φ[0.5A_nt f_ui + 0.6f_yiA_gv]`, `φ = 0.75`

— note the **0.5 factor on the tension term**, which is *not present* in
this handbook's own connection-component formula
(`φV_bs = φ[A_ntf_ui + 0.6f_yiA_gv]`, [[steel-connection-component-capacity]])
— reflecting the single-shear-surface/rotating-block mechanism specific to
a coped web. `[practice]` AISC Cl J4.3 gives upper bounds depending on bolt
layout: `φV_bs = φ[A_ntf_ui + 0.6f_yiA_gv]` (single column of bolts) or
`φ[0.5A_ntf_ui + 0.6f_yiA_gv]` (double column of bolts) — i.e. the
handbook's recommended coped-web formula corresponds to the AISC
**double-column-of-bolts** upper bound, not the single-column one.

![[asi-h1-fig-64-block-shear-areas-swc-dwc.png]]
*Figure 64 — block shear areas in SWC and DWC members: `A_nt = l_tt_w -
0.5d_ht_w` (single column of bolts), `A_gv = l_vt_w`, with `l_t` = end
distance to bolt-line centreline, `l_v` = cope top to bottom-hole
centreline (ASI Handbook 1, 2007).*

`[derived]` The three-way divergence — AS 4100 Cl 9.1.9(e) (current code
clause), this handbook's Ch 5.4 connection-component formula, and this
handbook's own Ch 6.9 coped-web formula (with its extra 0.5 factor) — means
block shear must be checked against the formula that actually matches the
element and bolt-column arrangement being assessed, not applied
interchangeably. See the Contradictions section on
[[steel-connection-component-capacity]] for the full comparison against
Cl 9.1.9(e).

### Web reinforcement of coped supported members (Ch 6.10)

`[practice]` Where an SWC/DWC section's capacity is inadequate, either
select a different (deeper/heavier) member to eliminate the need for
reinforcement, or reinforce the web — noting the added labour cost of
stiffeners/doubler plates may make member selection the more economical
fix despite higher material cost. Three reinforcing details (Ref. 9,
Part 9), for rolled sections with `d_w/t_w ≤ 60`:

- **Doubler plate** (Figure 65(a)): substitute `(t_w + t_d,req)` for `t_w`
  in the coped-section capacity formulas above to find the required
  doubler thickness; extend the plate ≥ the cope depth `d_c` beyond the
  cope to prevent local crippling.
- **Longitudinal stiffener** (Figure 65(b)): proportion to meet AS 4100
  width-thickness limits; check the stiffened cross-section's moment
  capacity (local web buckling need not then be separately checked);
  extend ≥ `d_c` beyond the cope.
- **Combined longitudinal + transverse stiffeners** (Figure 65(c)): for
  thin-web plate girders (`d_w/t_w > 60`); longitudinal stiffener extends
  ≥ `L_c/3` beyond the cope.

![[asi-h1-fig-65-web-reinforcement-coped-members.png]]
*Figure 65 — web reinforcement of coped supported members: (a) doubler
plate, (b) longitudinal stiffener, (c) combined longitudinal and
transverse stiffeners (ASI Handbook 1, 2007).*

## Worked reference

See worked examples 6 (Ch 6.3, uncoped UB), 7 (Ch 6.5, SWC UB) and 8
(Ch 6.7, DWC UB) above — fully transcribed with source figures.

## Contradictions

`[practice]` **Block shear formula divergence (coped webs vs connection
components)** — this handbook's own Ch 6.9 coped-beam-web block-shear
formula (`φV_bs = φ[0.5A_ntf_ui + 0.6f_yiA_gv]`) includes a `0.5` factor on
the tension term that its Ch 5.4 connection-component formula
(`φV_bs = φ[A_ntf_ui + 0.6f_yiA_gv]`, see
[[steel-connection-component-capacity]]) does not. Both differ from AS
4100:2020's own current Cl 9.1.9(e). See the Contradictions section on
[[steel-connection-component-capacity]] for the full three-way comparison
— confirm the correct formula per element type and bolt-column arrangement
before use, and cite AS 4100 Cl 9.1.9(e) for code compliance.

## Related

- [[steel-connection-component-capacity]] — the parallel Ch 5 treatment
  for connection components (gusset plates, cleats), including the
  block-shear formula divergence with AS 4100 Cl 9.1.9(e).
- [[as4100-beam-section-moment-capacity]] — Cl 5.2 general section moment
  capacity provisions (uncoped case).
- [[as4100-web-shear-and-bearing]] — Cl 5.11–5.13 general shear capacity
  and shear-moment interaction provisions.
- [[as4100-web-stiffeners]] — general AS 4100 stiffener design (Cl 5.14–
  5.16), the code-clause counterpart to the coped-end stiffening practice
  above.
- [[steel-connection-classification-and-design-philosophy]] — the four
  connection elements (fasteners, components, supported member, supporting
  member) this page and [[steel-connection-component-capacity]] address.

## Sources

- `raw/1-steelwork/ASI - Handbook 1 - Background and Theory - Design of
  Structural Steel Connections.pdf`, Ch 6.1–6.10 (pp. 86–109). Figures
  51, 52, 53, 54, 55, 59, 60, 61, 62, 63, 64, 65 and Tables 32A/B, 33A, 34A/B
  reproduced in `wiki/1-steelwork/assets/`. Table 32C, Table
  33B and the PFC-specific SWC formula variations described in text but
  not reproduced.
