---
title: Member effective length factors and frame buckling load factors
category: 0-standards
tags: [effective-length, buckling, frame-buckling, stiffness-ratio, elastic-buckling-load]
standards: [AS 4100:2020 Cl 4.6, AS 4100:2020 Cl 4.7, AS 4100:2020 App G]
status: draft
reviewed: 2026-09-13
---

# Member effective length factors and frame buckling load factors

> Scope: AS 4100:2020 Cl 4.6 (member elastic buckling load `N_om`, effective
> length factor `k_e` for idealised restraints, frames and triangulated
> structures, stiffness ratio `γ`, Table 4.6.3.4 `β_e`), Cl 4.7 (frame
> elastic buckling load factor `λ_c`, `λ_m`, `λ_ms`) and Appendix G (braced
> member buckling in frames with axial-force-modified restraint stiffness).

## Summary

`[code]` `N_om = π² E I / (k_e l)²` (Cl 4.6.2), with `l` the member length
centre-to-centre of intersections with supporting members and `k_e` from
Cl 4.6.3. `N_omb` (braced) feeds `δ_b` (Cl 4.4.2.2); `N_oms` (sway) feeds
`λ_ms` and hence `δ_s` (Cl 4.4.2.3, 4.7.2.2).

`[code]` `k_e` is obtained from: Cl 4.6.3.2 (idealised end restraints,
Figure 4.6.3.2); Cl 4.6.3.3 or App G (braced members in frames); Cl 4.6.3.3
(sway members in rectangular frames with regular loading and negligible beam
axial force); Cl 4.6.3.5 (triangulated structures) (Cl 4.6.3.1).

## Detail

### Idealised end restraints (Cl 4.6.3.2, Figure 4.6.3.2)

![[as4100-fig-4.6.3.2-effective-length-factors-idealised.png]]
*Figure 4.6.3.2 — effective length factors for idealised end restraints (AS 4100:2020).*

`[code]` Own tabulation of the figure:

| Case | Top end | Bottom end | k_e |
|---|---|---|---|
| Braced | rotation fixed, translation fixed | rotation fixed, translation fixed | 0.7 |
| Braced | rotation free, translation fixed | rotation fixed, translation fixed | 0.85 |
| Braced | rotation free, translation fixed | rotation free, translation fixed | 1.0 |
| Sway | rotation fixed, translation free | rotation fixed, translation fixed | 1.2 |
| Sway | rotation free, translation free | rotation fixed, translation fixed | 2.2 |
| Sway | rotation fixed, translation free | rotation free, translation fixed | 2.2 |

`[derived]` Note the AS 4100 values are deliberately above the theoretical
Euler values (0.5, 0.7, 1.0, 1.0, 2.0, 2.0) to allow for realistic
non-rigid "fixed" ends. The sway "fixed-fixed" case at 1.2 (theoretical 1.0)
is the one most often under-estimated in hand checks of portal columns.

### Members in rigid-jointed frames (Cl 4.6.3.3, 4.6.3.4)

`[code]` `k_e` from Figure 4.6.3.3(a) for a braced member and 4.6.3.3(b) for
a sway member, entered with the stiffness ratios `γ_1`, `γ_2` at each end:

`γ = Σ(I/l)_c / Σ β_e (I/l)_b`

- `Σ(I/l)_c` — sum of in-plane stiffnesses of all compression members
  rigidly connected at that end, including the member itself.
- `Σβ_e(I/l)_b` — sum of in-plane stiffnesses of all beams rigidly
  connected at that end; pin-connected beams contribute nothing.
- Base not rigidly connected to a footing: `γ ≥ 10` unless rational analysis
  justifies less. Base rigidly connected to a footing: `γ ≥ 0.6` unless
  justified (4.6.3.4).

`[code]` Table 4.6.3.4 — beam far-end modifying factor `β_e`:

| Fixity at far end of beam | Beam restraining a braced member | Beam restraining a sway member |
|---|---|---|
| Pinned | 1.5 | 0.5 |
| Rigidly connected to a column | 1.0 | 1.0 |
| Fixed | 2.0 | 0.67 |

![[as4100-fig-4.6.3.3a-ke-chart-braced.png]]
*Figure 4.6.3.3(a) — k_e for braced members (AS 4100:2020).*

![[as4100-fig-4.6.3.3b-ke-chart-sway.png]]
*Figure 4.6.3.3(b) — k_e for sway members (AS 4100:2020).*

`[derived]` (general knowledge, not from AS 4100) Closed-form fits commonly used in spreadsheets in place of the
charts (not in AS 4100; from the Eurocode/AISC alignment-chart literature):
braced `k_e ≈ (1 + 0.145(γ_1+γ_2) − 0.265γ_1γ_2) / (2 − 0.364(γ_1+γ_2) − 0.247γ_1γ_2)`;
sway `k_e ≈ sqrt[(1 − 0.2(γ_1+γ_2) − 0.12γ_1γ_2) / (1 − 0.8(γ_1+γ_2) + 0.6γ_1γ_2)]`.
Check against the chart before relying on a fitted value near the chart
boundaries.

### Triangulated structures (Cl 4.6.3.5)

`[code]` `l_e ≥ l` (centre-to-centre of intersections) unless a rational
elastic buckling analysis consistent with App G shows otherwise.

`[derived]` For truss chords and web members this means `k_e = 1.0` in-plane
by default; out-of-plane the effective length is the distance between
effective lateral restraints (purlins, bracing nodes), which is a Section 6
member-length question rather than a frame-buckling one.

### Appendix G — braced member buckling in frames (normative)

`[code]` Same `N_om = π²EI/(k_e l)²` with `k_e` from Figure 4.6.3.3(a), but
the stiffness ratio at each restrained end includes the effect of axial
force in the restraining members:

`γ = (I/l)_m / Σ β_e α_sr (I/l)_r`

- `(I/l)_m` — stiffness of the compression member under consideration.
- `Σβ_e α_sr (I/l)_r` — sum over all braced restraining members rigidly
  connected at that end (excluding the member itself).
- `β_e` — Table 4.6.3.4 far-end factor.
- `α_sr` — stability function multiplier for design axial force `N*_r` in
  the restraining member, from theory or the Figure G.1 approximation with
  `ρ = N*_r / N_olr`, `N_olr = π² E I_r / l_r²`. Restraining member in
  tension: `α_sr = 1.0` conservatively. Restraining member with negligible
  moment-transmitting connection: contribution = 0.

![[as4100-fig-G.1-stability-function-multipliers.png]]
*Figure G.1 — stability function multipliers α_sr (AS 4100:2020).*

`[code]` Reading Figure G.1 (own words): for `N*_r = 0`, `α_sr = 1.0`. Far end
of restraining member fixed: `α_sr ≈ 1 − ρ/4` (double curvature) or
`1 − ρ/2`; far end pinned or free-to-rotate with single curvature:
`1 − 2ρ/3` type lines, and lines `2 − 2ρ`, `2 − ρ`, `1 − ρ` for other
curvature / fixity combinations. Compression `ρ` positive; tension negative
(α_sr > 1).

### Frame buckling analysis (Cl 4.7)

`[code]` `λ_c` = ratio of the elastic buckling load set of the frame to the
design load set — it depends on the load set. Used in `δ_s` (Cl 4.4.2.3(b))
and to bound the analysis method (Cl 4.5.4, App E) (4.7.1). For a
rigid-jointed frame obtain `λ_c` by an approximate method (4.7.2.1 or
4.7.2.2) or a rational elastic buckling analysis of the whole frame.

- **Rectangular frames, all members braced** (4.7.2.1): `N_omb` per
  Cl 4.6.2/4.6.3.3/4.6.3.4 for each column; `λ_m = N_omb / N*`; frame
  `λ_c` = lowest `λ_m`.
- **Rectangular frames with sway members** (4.7.2.2): `N_oms` per the same
  clauses; for each storey `λ_ms = Σ(N_oms/l) / Σ(N*/l)` summed over all
  columns in the storey with tension `N*` negative; frame `λ_c` = lowest
  `λ_ms`.

`[derived]` STAAD and SAP2000 buckling analyses return `λ_c` directly
for a given load case; check that the returned mode is an in-plane sway
mode of the frame (not a local member or out-of-plane mode) before using
it in `δ_s`. Declare the software convention on the tool page.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as4100-structural-analysis-methods]] — δ_b, δ_s amplification that
  consumes `N_omb`, `λ_ms`, `λ_c`.
- [[as4100-compression-member-capacity]] — Cl 6.3.2 effective length `l_e =
  k_e l` for member capacity uses the same `k_e`.
- [[as4100-combined-actions-member-capacity]] — Cl 8.4 in-plane capacity.
- [[as3600-column-slenderness-and-moment-magnification]] — AS 3600
  counterpart (effective length charts, stiffness ratios).

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Cl 4.6–4.7
  (pp. 47–52), Appendix G (pp. 192–193). Figures 4.6.3.2, 4.6.3.3(a)/(b)
  and G.1 reproduced in `wiki/0-standards/assets/`.
