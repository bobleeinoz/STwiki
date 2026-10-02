---
title: Combined actions — section capacity (axial + bending)
category: 1-steelwork
tags: [combined-actions, section-capacity, uniaxial-bending, biaxial-bending, interaction]
standards: [AS 4100:2020 Cl 8.1, AS 4100:2020 Cl 8.2, AS 4100:2020 Cl 8.3]
status: draft
reviewed: 2026-09-13
---

# Combined actions — section capacity

> Scope: AS 4100:2020 Cl 8.1–8.3 — general routing for members under combined
> axial force and bending, design action definitions, uniaxial section
> capacity about the major (`M_rx`) and minor (`M_ry`) principal axes, and
> biaxial bending section capacity. Member (buckling) capacity is on
> [[steel-combined-actions-member-capacity]].

## Summary

`[code]` A member under combined axial and bending actions must satisfy
Cl 8.3 (section capacity) and Cl 8.4 (member capacity) at all sections and
along the whole member respectively (Cl 8.1). For plastic design, only
Cl 8.4.3 need be satisfied. Eccentrically loaded double-bolted or welded
single angles in trusses satisfy Cl 8.3 and either Cl 8.4.5 or Cl 8.4.6.

`[code]` Basic uniaxial interaction: `M_rx = M_sx(1 − N*/φN_s)`,
`M_ry = M_sy(1 − N*/φN_s)` — a linear reduction of section moment capacity
by the axial load ratio, applicable to any section shape. Compact doubly
symmetric I-sections and compact RHS/SHS to AS/NZS 1163 get less
conservative closed forms.

## Detail

### Design actions (Cl 8.2)

`[code]` For **section** capacity: `N*` (tension or compression) and
`M*_x`, `M*_y` are the values **at the section** considered. For **member**
capacity: `N*` and `M*_x`, `M*_y` are the **maximum** values anywhere in the
member. `M*_x`, `M*_y` include second-order effects from frame action and
transverse loading (the amplified moments from Cl 4.4.2/App E), obtained by:
(a) first-order elastic analysis with Cl 4.4.2 amplification; (b) second-
order elastic analysis (App E); (c) first-order plastic analysis (frames
with `λ_c ≥ 5`, satisfying Cl 4.5.4); (d) second-order plastic analysis
(`λ_c < 5`); or (e) advanced structural analysis (App D) — in which case
only Cl 8.3 (section) and Section 9 (connections) need be satisfied.

### Section capacity — general (Cl 8.3.1)

`[code]` Routing: (a) bending about the major x-axis only → Cl 8.3.2 at all
sections; (b) about the minor y-axis only → Cl 8.3.3; (c) about a
non-principal axis, or about both principal axes → Cl 8.3.4 (biaxial).
`M_sx`, `M_sy` = nominal section moment capacities (Cl 5.2); `N_s` =
nominal section axial capacity (Cl 6.2 compression, or Cl 7.2 tension,
where `N_s = N_t`).

### Uniaxial bending about the major x-axis (Cl 8.3.2)

`[code]` `M*_x ≤ φM_rx`, general form: `M_rx = M_sx(1 − N*/φN_s)`.

`[code]` Less conservative alternatives for **compact** doubly symmetric
I-sections and compact RHS/SHS to AS/NZS 1163 (Cl 5.2.3):
- `k_f = 1.0` (compression) or tension:
  `M_rx = 1.18 M_sx (1 − N*/φN_s) ≤ M_sx`
- `k_f < 1.0` (compression):
  `M_rx = M_sx (1 − N*/φN_s)[1 + 0.18(82 − λ_w)/(82 − λ_wy)] ≤ M_sx`,
  `λ_w`, `λ_wy` = the web's `λ_e`, `λ_ey` (Cl 6.2.3, Table 6.2.4).

### Uniaxial bending about the minor y-axis (Cl 8.3.3)

`[code]` `M*_y ≤ φM_ry`, general form: `M_ry = M_sy(1 − N*/φN_s)`.

`[code]` Alternatives: doubly symmetric I-sections compact —
`M_ry = 1.19 M_sy [1 − (N*/φN_s)²] ≤ M_sy`; compact RHS/SHS to AS/NZS 1163
— `M_ry = 1.18 M_sy [1 − (N*/φN_s)] ≤ M_sy`.

### Biaxial bending (Cl 8.3.4)

`[code]` General: `N*/φN_s + M*_x/φM_sx + M*_y/φM_sy ≤ 1`.

`[code]` Less conservative, compact doubly symmetric I-sections and compact
RHS/SHS: `(M*_x/φM_rx)^γ + (M*_y/φM_ry)^γ ≤ 1`, with `M_rx`, `M_ry` from
Cl 8.3.2/8.3.3 and `γ = 1.4 + N*/φN_s ≤ 2.0`.

`[derived]` `γ` ranges from 1.4 (zero axial load, pure biaxial bending
interaction close to a straight-ish diamond) to 2.0 (heavily axially loaded,
approaching a circular/elliptical interaction) — physically this reflects
that axial-load-dominated sections have a less severe biaxial-bending
penalty than bending-dominated ones.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[steel-combined-actions-member-capacity]] — Cl 8.4, buckling capacity
  under combined actions (uses `M_rx`, `M_ry` from this page).
- [[steel-beam-section-moment-capacity]] — `M_sx`, `M_sy`, compact section
  definition (Cl 5.2.3).
- [[steel-compression-member-capacity]] — `N_s` (Cl 6.2), `k_f`.
- [[steel-tension-member-capacity]] — `N_t` (Cl 7.2).
- [[asi-design-capacity-tables-vol1-open-sections]] — Part 8 worked braced
  beam-column example, biaxial interaction confirmed against DCT formulas.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Cl 8.1–8.3
  (pp. 103–107).
