---
title: Weld group analysis methods — in-plane, out-of-plane, combined loading, properties of common groups
category: 1-steelwork
tags: [welds, weld-group, fillet-weld, instantaneous-centre, in-plane, out-of-plane, ASI-handbook-1]
standards: [AS 4100:2020 Cl 9.7, AS 4100:2020 Cl 9.8]
status: draft
reviewed: 2026-09-13
---

# Weld group analysis methods

> Scope: ASI Design Guide "Handbook 1 — Background and Theory: Design of
> Structural Steel Connections" (T.J. Hogan, first edition 2007) Ch 4 —
> weld types and symbols, weld categories, fillet weld design theory, the
> full elastic instantaneous-centre method for fillet weld groups loaded
> in-plane (AS 4100 Cl 9.8.1), out-of-plane (Cl 9.8.2) and combined
> (Cl 9.8.3), properties of common weld-group shapes, closed-form design
> capacities for two common cases, and two fully worked examples. This is
> the derivation and design-aid material behind the brief clause summary on
> [[steel-weld-design]] (Cl 9.7 "Assessment of a weld group").

## Summary

`[practice]` A fillet weld group is analysed identically to a bolt group
(same instantaneous-centre assumptions, AS 4100 Cl 9.8.1.1 mirrors
Cl 9.4.1), except the weld is treated as a **continuous line element of
unit throat thickness** rather than discrete fasteners — giving closed-form
expressions in terms of the weld group's length `L_w` and its "polar
second moment of area" `I_wp = I_wx + I_wy` (a line-element analogy to a
cross-section's polar second moment of area). Design requirement at every
point: `v*_res ≤ φv_w = φ(0.6f_uw t_t)` (AS 4100 Cl 9.7.3.10).

## Detail

### Weld types and symbols (Ch 4.1)

`[code]` AS 4100 recognises six weld types: complete penetration butt,
incomplete penetration butt, fillet, plug, slot, compound.

![[asi-h1-fig-28-weld-types.png]]
*Figure 28 — the six AS 4100 weld types in cross-section (ASI Handbook 1,
2007).*

`[practice]` Standard drafting symbols (AS 1101.3) for specifying these on
drawings:

![[asi-h1-fig-29-weld-symbols.png]]
*Figure 29 — standard weld symbols per AS 1101.3, showing every annotation
position on the reference line/arrow/tail (ASI Handbook 1, 2007).*

### Weld categories and butt weld design (Ch 4.2–4.4)

`[practice]` AS 4100 permits two weld categories — **SP** (structural
purpose, tighter permitted-imperfection limits) and **GP** (general
purpose) — selectable at the designer's discretion, though SP is expected
to be the practical default. `[derived]` The GP/SP capacity-factor ratio
sets a break-even utilisation below which GP is a legitimate economy: for
complete-penetration butt welds, `φ_GP/φ_SP = 0.6/0.9 = 66.7%`; for fillet/
incomplete-penetration/plug/slot/weld-group, `0.6/0.8 = 75%`. **If the GP
weld is loaded above this fraction of the equivalent SP capacity, GP is
disqualified and SP must be specified** — i.e. GP is only a valid choice
where the weld is lightly loaded relative to what it could carry as SP.

`[code]` Complete-penetration butt weld design capacity = nominal capacity
of the weaker joined part × `φ` (0.90 SP / 0.60 GP). Incomplete-penetration
butt weld is designed **as a fillet weld** using the Cl 9.7.2.3(b) design
throat thickness.

![[asi-h1-fig-30-incomplete-penetration-throat-thickness.png]]
*Figure 30 — design throat thickness of an incomplete penetration butt
weld: (a) other than a fully automatic process (throat = depth of
preparation less 0–3 mm); (b) fully automatic process, where a macro test
can justify taking the full depth of preparation (ASI Handbook 1, 2007).*

### Fillet weld strength design (Ch 4.5)

`[code]` `v*_w ≤ φv_w`, `φ = 0.80` SP / `0.60` GP, `v_w = 0.6 f_uw t_t k_r`
(Cl 9.7.3.10). Design throat thickness `t_t` is the shortest distance from
the weld root to the hypotenuse of the (possibly unequal-leg, or deep-
penetration) triangular weld cross-section:

![[asi-h1-fig-31-fillet-weld-throat-thickness.png]]
*Figure 31 — design throat thickness for (a) equal-leg, (b) unequal-leg,
and (c) automatic-process deep-penetration fillet welds:
`t_t = t_t1 + 0.85t_t2` (ASI Handbook 1, 2007).*

![[asi-h1-table-23-24-fillet-weld-capacities.png]]
*Tables 23–24 — SP (`φ=0.8`) and GP (`φ=0.6`) design capacity per unit
length of equal-leg fillet weld, by leg size and consumable
(E41XX/W40X `f_uw=410`, E48XX/W50X `f_uw=480`) (ASI Handbook 1, 2007).
Preferred sizes: 3–5 mm (minimum-size fillet), 6–8 mm (single-pass,
preferred for structural connections), 10–12 mm (not guaranteed
single-pass — confirm with the fabricator before specifying).*

`[practice]` Design force per unit length is the **vectorial sum** of three
orthogonal components resolved onto the weld throat (normal, longitudinal,
transverse — Figure 32); AS 4100 adopts `k_v = k_w = 1.0` in this
combination based on Ref. 21's test-calibration studies, i.e. **no
directional strength bonus** is taken even though transversely loaded
fillet welds test 13–44% stronger than longitudinally loaded ones (at
roughly 1/4 the ductility) — the conservatism is instead absorbed into
`φ`.

![[asi-h1-fig-32-design-actions-fillet-weld.png]]
*Figure 32 — design actions on a fillet weld resolved normal (`v*_n`),
transverse (`v*_vt`) and longitudinal (`v*_vl`) to the throat
(ASI Handbook 1, 2007).*

### Weld group loaded in-plane (Ch 4.6–4.7)

`[code]` AS 4100 Cl 9.8.1.1 mirrors the bolt-group assumptions
([[steel-bolt-group-analysis-methods]]): rigid connection plates rotating
about an instantaneous centre; pure couple → centre at the weld-group
centroid; centroidal shear only → centre at infinity, force per unit length
uniform; combined → superpose, or use a recognised method; force per unit
length at any point acts at right angles to, and proportional to, its
radius from the instantaneous centre.

![[asi-h1-fig-35-general-fillet-weld-group.png]]
*Figure 35 — general fillet weld group loaded in-plane: load point
`(x_p, y_p)`, instantaneous centre `(x_e, y_e)`, weld element `d_s` at
`(x_s, y_s)` (ASI Handbook 1, 2007).*

`[derived]` Equilibrium of the weld group (summing `v*_s d_s` components,
Eqns 4.7.1–4.7.3), substituting `v*_s = k_w r_s` (assumption (c)), and
introducing the weld group's second moments of area treated as a unit-
thickness line element (`I_wx = Σy_s²d_s`, `I_wy = Σx_s²d_s`,
`I_wp = I_wx + I_wy`) gives closed-form solutions for the instantaneous
centre and proportionality constant:

`x_e = -F*_y/(k_w L_w)`, `y_e = -F*_x/(k_w L_w)`,
`k_w = [M*_z + F*_x y_p + F*_y x_p] / I_wp` (Eqns 4.7.10–4.7.12)

`v*_w = k_w r_s`, `r_s = sqrt[(x_s-x_e)² + (y_s-y_e)²]` (Eqn 4.7.13),
checked against `φv_w`.

`[practice]` **Superposition alternative** (Cl 9.8.1.1(b)): transfer the
design actions to the weld-group centroid (`M*_zo = M*_z + F*_x y_p -
F*_y x_p`, Eqn 4.7.14); centroidal shear is then uniform
(`v*_x = F*_x/L_w`, `v*_y = F*_y/L_w`) and the pure couple gives
`v*_mx = -M*_zo y_s/I_wp`, `v*_my = +M*_zo x_s/I_wp` (Figure 36, Eqns
4.7.15–4.7.16); superposed:

`v*_x = F*_x/L_w − M*_zo y_s/I_wp`, `v*_y = F*_y/L_w + M*_zo x_s/I_wp`
(Eqns 4.7.17–4.7.18), `v*_res = sqrt[(v*_x)² + (v*_y)²]` (Eqn 4.7.19)

`[derived]` Eqns 4.7.13 (first-principles) and 4.7.19 (superposition) are
alternative, equivalent design requirements — either satisfies AS 4100;
the superposition form is generally more convenient for hand calculation
since it avoids solving for the instantaneous centre location directly.

### Weld group loaded out-of-plane (Ch 4.8)

`[code]` AS 4100 Cl 9.8.2.1: (a) weld group considered in isolation from
the connected element; (b) force per unit length from a design moment
varies **linearly** with distance from the relevant centroidal axis; from
shear or axial force, **uniform** along the weld length.

![[asi-h1-fig-37-weld-group-out-of-plane.png]]
*Figure 37 — fillet weld group loaded out-of-plane: design moment `M*_x`
about the x-axis, forces `F*_y`, `F*_z` (ASI Handbook 1, 2007).*

`[code]` `v*_x = F*_x/L_w`, `v*_y = F*_y/L_w`,
`v*_z = F*_z/L_w + M*_x y/I_wx` (or `+ M*_y x/I_wy` for moment about y),
`v*_res = sqrt[(v*_x)²+(v*_y)²+(v*_z)²] ≤ φv_w`
(Eqns 4.8.1–4.8.4). `[practice]` Superposition is assumed permitted here
too (not explicit in Cl 9.8.2.1, but the AS 4100 Commentary extends the
Cl 9.8.1.1 permission).

### Combined in-plane and out-of-plane loading (Ch 4.9)

`[code]` Cl 9.8.3.1: combine the in-plane and out-of-plane methods, both
satisfying Cl 9.7.3.10 at every point, shear/force components combined
vectorially.

![[asi-h1-fig-33-weld-group-axes.png]]
*Figure 33 — design forces per unit length resolved parallel to the weld
group's x, y, z axes (ASI Handbook 1, 2007).*

For the general fillet weld group of Figure 38 (combining Eqns 4.7.17,
4.7.18, 4.8.1–4.8.4):

`v*_x = F*_x/L_w − M*_z y/I_wp` (Eqn 4.9.1)
`v*_y = F*_y/L_w + M*_z x/I_wp` (Eqn 4.9.2)
`v*_z = F*_z/L_w + M*_x y/I_wx − M*_y x/I_wy` (Eqn 4.9.3)

`[practice]` These may be modified to reflect a realistic distribution of
the force components among different portions of the weld group by
substituting `L_wx`, `L_wy`, `L_wz` (the length of weld assumed to receive
each force component) for `L_w` (Eqns 4.9.4–4.9.6) — e.g. assuming only the
web welds of a box/channel section resist vertical shear (used directly in
Worked example 5 below). `v*_res = sqrt[(v*_x)²+(v*_y)²+(v*_z)²] ≤ φv_w`.

### Properties of common fillet weld groups (Ch 4.9 design aid)

`[practice]` `x̄`, `ȳ`, `I_wx`, `I_wy`, `I_wp` (all for **unit throat
thickness**, i.e. per mm of `t_t`) for eight common weld-group outline
shapes — single line, single/double C-channel outline (with or without
flange returns), full/partial rectangle outline, I-outline, circle:

![[asi-h1-table-25a-weld-group-properties.png]]
*Table 25 (part 1) — properties of weld-group types 1–5: single vertical
line, single-return channel, double-return channel, full C-channel,
C-channel with inward flange returns (ASI Handbook 1, 2007).*

![[asi-h1-table-25b-weld-group-properties.png]]
*Table 25 (part 2) — properties of weld-group types 6–8: full rectangle
outline, I-outline (top/bottom + web), circle (ASI Handbook 1, 2007).*

`[derived]` This table is the weld-group analogue of tabulated cross-
section properties — indispensable for the superposition method (Eqns
4.7.17–4.9.6), since `I_wx`/`I_wy`/`I_wp` must be computed for the actual
weld outline before any force-per-unit-length equation can be evaluated.

`[practice]` For weld groups made of lines parallel to the x/y axes, the
governing check need only be made at a small set of **critical points**
(corners and extremities):

![[asi-h1-fig-39-weld-group-critical-points.png]]
*Figure 39 — the 8 possible critical points (corners 1–4 and 5–8 at the
opposite ends) for a rectangular-outline weld group (ASI Handbook 1,
2007).*

### Closed-form capacities — two common weld-group cases (Ch 4.10)

`[practice]` **Two parallel vertical welds loaded out-of-plane** (a common
bracket/stiffener detail, Figure 41: two equal-length vertical fillet welds
each side of a plate, length `L_w`, loaded by `F*_y`, `F*_z`, `M*_x` at the
centroid):

- Vertical shear only: `φv_dv = 2L_w(φv_w)`.
- Horizontal shear only: `φv_dh = 2L_w(φv_w)`.
- Moment only: `φM_dm = (1/3)L_w²(φv_w)`.
- Vertical force at eccentricity `e`:
  `F*_y ≤ 2L_w(φv_w) / sqrt[1+(6e/L_w)²]`.

![[asi-h1-fig-41-two-parallel-vertical-welds.png]]
*Figure 41 — two parallel vertical welds loaded out-of-plane
(ASI Handbook 1, 2007).*

`[practice]` **Two parallel horizontal welds loaded out-of-plane**
(Figure 42: two horizontal fillet welds, length `L_w`, separated by `t`,
loaded by `F*_y`, `F*_z`, `M*_x`):

- Vertical shear only: `φv_dv = 2L_w(φv_w)`.
- Horizontal shear only: `φv_dh = 2L_w(φv_w)`.
- Moment only: `φM_dm = L_w t(φv_w)`.
- Vertical force at eccentricity `e`:
  `F*_y ≤ (φv_w)·2L_w / sqrt[1+4(e/t)²]`.

![[asi-h1-fig-42-two-parallel-horizontal-welds.png]]
*Figure 42 — two parallel horizontal welds loaded out-of-plane
(ASI Handbook 1, 2007).*

`[derived]` These closed forms are ready-made design capacities for two of
the most common bracket/stiffener weld layouts, saving a full `I_wx`/`I_wp`
calculation — directly analogous to the bolt-group `Z_b` design aids on
[[steel-bolt-group-analysis-methods]].

### Worked example 4 — fillet weld group loaded in-plane (Ch 4.11)

`[derived]` A Table-25-type-4 (C-channel outline) weld group,
`a = b = 275 mm`, `d = 300 mm`, resists `F*_y = -180 kN` applied 275+175 mm
from the weld group's back face (Figure 43). Weld centroid `x̄ = 89.0 mm`,
`M*_z = -64 980 kNmm`. `I_wp = 21.8×10⁶ mm³`(sic — units of mm³ for a
unit-thickness line-element second moment). Critical points 1, 6:
`v*_x = ±0.447`, `v*_y = -0.767`, `v*_res = 0.888 kN/mm`. A 6 mm E48XX SP
fillet weld (`φv_w = 0.978 kN/mm` from Table 23) is satisfactory.

![[asi-h1-fig-43-weld-group-in-plane-example.png]]
*Figure 43 — fillet weld group loaded in-plane, worked example 4 geometry
(ASI Handbook 1, 2007).*

### Worked example 5 — fillet weld group loaded out-of-plane (Ch 4.12)

`[derived]` A rectangular (box-section-type) weld group, 300×200 mm
outline, resists `F*_y = -450 kN` and `M*_x = 90 kNm` (Figure 44). Using
the **alternative** (Cl 9.8.2.2) method — assuming the vertical shear is
carried **only by the two 300 mm web welds** (`L_wy = 600 mm`, not the full
1000 mm perimeter) while the moment is resisted by the full outline's
`I_wx` (Table 25 type 6) — gives `v*_y = -0.75 kN/mm` at the web welds,
`v*_z = ±1.00 kN/mm` at the top/bottom corners, `v*_res = 1.25 kN/mm`. An
8 mm E48XX SP fillet weld (`φv_w = 1.30 kN/mm`) is satisfactory.

![[asi-h1-fig-44-weld-group-out-of-plane-example.png]]
*Figure 44 — fillet weld group loaded out-of-plane, worked example 5
geometry (ASI Handbook 1, 2007).*

`[derived]` This example is the clearest illustration of why the
**alternative** analysis method (Cl 9.8.2.2, treating the weld group as an
extension of the connected member with an assumed, equilibrium-satisfying
force distribution) can be more realistic and less conservative than the
**general** method (isolated weld group, Cl 9.8.2.1) — a designer who
understands how the connected member (here, a box section) actually
carries shear through its webs can avoid over-designing the weld by
assuming the full unmodified perimeter resists vertical shear.

## Worked reference

See worked examples 4 and 5 above (Ch 4.11, 4.12) — fully transcribed with
source figures.

## Contradictions

None recorded.

## Related

- [[steel-weld-design]] — AS 4100 Cl 9.6–9.8 code clauses this page's
  methods implement.
- [[steel-bolt-group-analysis-methods]] — the directly analogous
  instantaneous-centre method for bolt groups; the same mathematics with
  discrete fasteners instead of a continuous line element.
- [[steel-connection-classification-and-design-philosophy]] — Cl 9.1.3
  design-model background.

## Sources

- `raw/1-steelwork/ASI - Handbook 1 - Background and Theory - Design of
  Structural Steel Connections.pdf`, Ch 4.1–4.12 (pp. 52–76). Figures 28,
  29, 30, 31, 32, 33, 35, 37, 39, 41, 42, 43, 44 and Table 25 (both parts)
  and Tables 23–24 reproduced in `wiki/1-steelwork/assets/`. Figures 34,
  36, 38, 40 and Tables 21–22 described in text but not reproduced.
