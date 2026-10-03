---
title: ACI 318M-19 column slenderness and moment magnification — nonsway/sway, k, (EI)eff
category: 0-standards
tags: [aci, slenderness, moment-magnifier, second-order, columns]
standards: [ACI 318M-19 Cl 6.2.5, ACI 318M-19 Cl 6.6.4]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 column slenderness and moment magnification

> Scope: ACI 318M-19 Cl 6.2.5 (when slenderness effects may be neglected,
> radius of gyration) and Cl 6.6.4 (the moment magnifier method for both
> nonsway and sway frames/stories, stability index `Q`, critical buckling
> load `P_c`, effective length factor `k`, effective stiffness `(EI)_eff`).
> This is an **ACI 318M-19 page, kept separate from the AS 3600:2018 concept
> pages** elsewhere in `2-concrete` — see [[aci-318m-19-building-code-concrete]]
> for why.

## Summary

`[code]` Slenderness ("second-order") effects may be neglected entirely if a
column passes a simple slenderness-ratio screening test (Cl 6.2.5.1).
Otherwise, column/beam/supporting-member design must account for
second-order effects via the **moment magnifier method** (Cl 6.6.4), a
second-order elastic analysis (Cl 6.7), or an inelastic analysis (Cl 6.8) —
this page covers the moment magnifier method, the most commonly used of the
three. `[derived]` This is functionally the same role as AS 3600's column
slenderness/moment magnification provisions (see
[[as3600-column-slenderness-and-moment-magnification]]), but the specific
screening ratios, magnifier equations and coefficients are not
interchangeable between the two codes.

## Detail

### When slenderness may be neglected (Cl 6.2.5.1–6.2.5.2)

`[code]` Slenderness effects may be neglected if:

- **Unbraced against sidesway**: `kℓ_u/r ≤ 22` (Eq. 6.2.5.1a).
- **Braced against sidesway**: `kℓ_u/r ≤ 34 − 12(M1/M2)` **and**
  `kℓ_u/r ≤ 40` (Eq. 6.2.5.1b/c), where `M1/M2` is negative in single
  curvature, positive in double curvature (2011 Code sign-convention
  change, Cl R6.2.5.3).

`[code]` A story may be treated as braced against sidesway if its bracing
elements (walls, shear trusses, etc.) have at least **12× the gross lateral
stiffness** of the columns in that story, in the direction considered —
without needing further calculation (unnumbered provision following
Cl 6.2.5.1). Radius of gyration `r`: `√(I_g/A_g)` generally, or the
simplified `0.30h` (rectangular columns) / `0.25` × diameter (circular
columns) (Cl 6.2.5.2).

`[derived]` **Effective length factor `k`** is most commonly estimated via
the Jackson and Moreland alignment charts:

![[aci318-fig-r6.2.5.1-alignment-charts-effective-length-k.png]]
*Fig. R6.2.5.1 — effective length factor `k` nomographs: (a) nonsway frames
(`k` range 0.5–1.0); (b) sway frames (`k` range 1.0–∞), both plotted against
`Ψ_A`/`Ψ_B` (the ratio of ΣEI/ℓ_c for columns to ΣEI/ℓ for beams at each end
of the column) (ACI 318M-19).* As a first approximation, `k = 1.0` may be
used directly in Eq. 6.2.5.1b/c without consulting the chart (Cl R6.2.5.1).

`[code]` The upper limit on second-order moment: `M_u` including
second-order effects must never exceed **1.4×** the first-order `M_u`
(Cl 6.2.5.3) — `[derived]` this exists because P-Δ effects introduce
analytical singularities (physical instability) as they grow; research
found stability-failure probability rises sharply once the stability index
`Q` (Cl 6.6.4.4.1) exceeds 0.2 (a 1.25 secondary-to-primary moment ratio),
and ASCE/SEI 7's own stability coefficient θ caps at 0.25 (a 1.33 ratio) —
the 1.4 limit was set as a conservative envelope over both (Cl R6.2.5.3).

### Nonsway vs sway classification (Cl 6.6.4.1–6.6.4.3)

`[code]` Every column/story must be designated nonsway or sway unless
Cl 6.2.5.1 already allows slenderness to be neglected entirely (Cl 6.6.4.1).
A story may be analysed as nonsway if **either**: (a) the second-order
increase in column end moments is ≤ 5% of the first-order end moments, or
(b) the stability index `Q ≤ 0.05` (Cl 6.6.4.3).

`[code]` **Stability index**:

**Q = (ΣP_u Δ_o) / (V_us ℓ_c)**  (Eq. 6.6.4.4.1)

where `ΣP_u` and `V_us` are the story's total factored vertical load and
horizontal shear, and `Δ_o` is the first-order relative lateral deflection
across the story due to `V_us`.

`[code]` Member dimensions assumed in any slenderness analysis must stay
within **10%** of the specified construction-document dimensions (and
reinforcement ratio within 10%, if Table 6.6.3.1.1(b) stiffnesses are used),
or the analysis must be repeated (Cl 6.6.4.2).

### Critical buckling load and effective stiffness (Cl 6.6.4.4)

`[code]` **Critical buckling load**:

**P_c = π²(EI)_eff / (kℓ_u)²**  (Eq. 6.6.4.4.2)

`k` uses `E_c` per Cl 19.2.2 and `I` per Cl 6.6.3.1.1; `k = 1.0` is
permitted for nonsway members, `k ≥ 1.0` required for sway members
(Cl 6.6.4.4.3).

`[code]` **(EI)_eff** — three options of increasing refinement (Cl 6.6.4.4.4):

**(EI)_eff = 0.4 E_c I_g / (1 + β_dns)**  (Eq. 6.6.4.4.4a, simplest)
**(EI)_eff = [0.2 E_c I_g + E_s I_se] / (1 + β_dns)**  (Eq. 6.6.4.4.4b, for
small eccentricity ratios and high axial load)
**(EI)_eff = E_c I / (1 + β_dns)**  (Eq. 6.6.4.4.4c, most refined, `I` from
Table 6.6.3.1.1(b))

where `β_dns` is the ratio of maximum factored **sustained** axial load to
maximum factored axial load in the same combination. `[derived]` Dividing
by `(1 + β_dns)` approximates the stiffness-reducing effect of creep under
sustained load — a simplification of `β_dns = 0.6` reduces Eq. 6.6.4.4.4a to
the often-quoted `(EI)_eff = 0.25 E_c I_g` (Cl R6.6.4.4.4). Creep also
transfers load from concrete to longitudinal reinforcement over time, which
can prematurely yield compression steel in lightly-reinforced columns —
hence both terms of Eq. 6.6.4.4.4b are reduced for creep, not just the
concrete term (Cl R6.6.4.4.4).

### Moment magnifier — nonsway frames (Cl 6.6.4.5)

`[code]` **M_c = δM_2**  (Eq. 6.6.4.5.1, `M_2` = first-order factored moment)

**δ = C_m / (1 − P_u/(0.75P_c)) ≥ 1.0**  (Eq. 6.6.4.5.2)

`[derived]` The **0.75** in the denominator is itself a stiffness reduction
factor `φ_K`, calibrated for the probability of understrength in a single
isolated slender column — distinct from (and not equal to) the ordinary
cross-sectional strength `φ` from Chapter 21 (see
[[aci318-strength-reduction-factors]]). `φ_K = 0.75` applies to an isolated
column; the Table 6.6.3.1.1(a) `I` values for multistory frames already
embed a less conservative `φ_K = 0.875`, since frame deflections depend on
*average* concrete strength across many members rather than one critical
understrength column (Cl R6.6.4.5.2).

`[code]` **C_m**: `0.6 − 0.4(M1/M2)` for columns without transverse load
between supports (Eq. 6.6.4.5.3a, `M1/M2` sign convention as above);
`C_m = 1.0` where transverse load is applied between supports
(Eq. 6.6.4.5.3b) — `[derived]` because the equivalent-uniform-moment
derivation behind `C_m` assumes the maximum moment sits near midheight, an
assumption transverse loading between supports can break (Cl R6.6.4.5.3).

`[code]` **Minimum moment**: `M_2 ≥ M_{2,min} = P_u(15 + 0.03h)` about each
axis separately (Eq. 6.6.4.5.4, `h` in mm) — if `M_{2,min}` governs, `C_m`
is either taken as 1.0 or still calculated from the *actual* `M1/M2` ratio
(Cl 6.6.4.5.4). `[derived]` This minimum-eccentricity floor is not intended
to be applied about both axes simultaneously (Cl R6.6.4.5.4).

### Moment magnifier — sway frames (Cl 6.6.4.6)

`[code]` End moments: `M_1 = M_{1ns} + δ_s M_{1s}`, `M_2 = M_{2ns} + δ_s
M_{2s}` (Eq. 6.6.4.6.1a/b — "ns" = nonsway component, "s" = sway component).
`δ_s` by **one** of three methods (Cl 6.6.4.6.2), with only (b) or (c)
permitted once `δ_s > 1.5`:

- **(a) Q method**: `δ_s = 1/(1 − Q) ≥ 1` (Eq. 6.6.4.6.2a) — an infinite-series
  solution for iterative P-Δ second-order moments, valid up to `δ_s ≈ 1.5`
  (Cl R6.6.4.6.2).
- **(b) Sum-of-P method**: `δ_s = 1/(1 − ΣP_u/(0.75ΣP_c)) ≥ 1`
  (Eq. 6.6.4.6.2b) — `ΣP_u`/`ΣP_c` summed over the **whole story**, not per
  column, since all sway-resisting columns in a story share the same lateral
  deflection absent torsional twist (Cl R6.6.4.6.2).
- **(c) Second-order elastic analysis** — see
  [[aci318-second-order-and-advanced-analysis]].

`[code]` Flexural members (beams) must be designed for the **total magnified
end moments** of the columns at the joint (Cl 6.6.4.6.3) — `[derived]` sway
frame strength is governed by column stability and beam end-restraint; if
plastic hinges form in the restraining beams as the frame approaches a
failure mechanism, column axial strength drops drastically, so the beams
must have enough strength to resist the full magnified column moments
(Cl R6.6.4.6.3). Second-order effects **along** a sway column's length
(not just at its ends) must also be considered, using the Cl 6.6.4.5
nonsway procedure with `C_m` from the sway `M1`/`M2` (Cl 6.6.4.6.4).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-structural-analysis-methods]] — Cl 6.1–6.5, the method menu this
  page's slenderness provisions sit within.
- [[aci318-second-order-and-advanced-analysis]] — Cl 6.6.3 (section
  properties), 6.7 (second-order elastic analysis, option (c) above).
- [[aci318-strength-reduction-factors]] — Chapter 21, the ordinary strength φ
  distinct from the `φ_K = 0.75`/`0.875` stiffness reduction factors here.
- [[as3600-column-slenderness-and-moment-magnification]] — the AS 3600
  equivalent, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 6 Cl 6.2.5 (pp. 68–71) and
  Cl 6.6.4 (pp. 77–83), incl. Fig. R6.2.5.1.
