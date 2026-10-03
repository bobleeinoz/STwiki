---
title: ACI 318M-19 torsional strength — threshold/cracking torsion, space truss analogy, Tn
category: 0-standards
tags: [aci, torsion, space-truss, sectional-strength]
standards: [ACI 318M-19 Cl 22.7]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 torsional strength

> Scope: ACI 318M-19 Cl 22.7 — when torsion can be neglected (threshold
> torsion), equilibrium vs compatibility torsion and the redistribution
> allowance, the thin-walled-tube space-truss analogy behind nominal
> torsional strength `T_n`, and the combined shear+torsion cross-sectional
> size limit. This is an **ACI 318M-19 page, kept separate from the AS
> 3600:2018 concept pages** elsewhere in `2-concrete` — see
> [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Torsion design is based on a **thin-walled tube / space truss
analogy**: the solid or hollow cross section is idealised as a thin-walled
tube, with the core concrete of a solid section neglected once torsional
cracking occurs (Cl R22.7). Torsional strength after cracking is assumed
provided entirely by closed stirrups and longitudinal bars near the surface
— the concrete's own torsional contribution is ignored, but `V_c` for
combined shear+torsion is taken as unaffected by the presence of torsion
(Cl R22.7.6). `[derived]` This mirrors the role AS 3600's own thin-walled
tube/space-truss torsion model plays (see
[[as3600-beam-shear-and-torsion-design]]), though the two codes' threshold
and design equations are not interchangeable.

## Detail

### When torsion can be neglected — threshold torsion (Cl 22.7.1, 22.7.4)

`[code]` Torsion only needs to be designed for if `T_u ≥ φT_th` (Cl 22.7.1.1)
— below the **threshold torsion** `T_th`, the Commentary's reasoning is that
torsion causes no structurally significant reduction in flexural or shear
strength (Cl R22.7.1.1). `T_th` is set at **one-quarter of the cracking
torsion `T_cr`** (Cl R22.7.4) — chosen because that level corresponds to
under 5% reduction in inclined shear-cracking capacity for solid sections
(negligible), versus a ~25% reduction if the full `T_cr` were used as the
threshold for a thin-walled hollow section (hence hollow sections get their
own, more conservative `(A_g/A_cp)²`-modified expression rather than reusing
the solid-section one).

![[aci318-table-22.7.4.1-22.7.5.1-threshold-cracking-torsion.png]]
*Tables 22.7.4.1(a)/(b) — threshold torsion `T_th` for solid and hollow
cross sections (nonprestressed, prestressed, and axial-force cases) — and
Table 22.7.5.1 — cracking torsion `T_cr` (same three cases), each using the
same `0.33λ√f'c` principal-tensile-stress cracking criterion as `T_th`'s
`0.083 = 0.33/4` coefficient (ACI 318M-19).*

`[code]` `A_cp`/`p_cp` relate to the full gross section (outer perimeter);
`A_g`/`p_cp` are used for hollow sections (`A_g` = gross area excluding the
void) — the ratio `A_g/A_cp` captures how much thinner a hollow section's
effective torsional "tube" is relative to an equivalent solid section
(Cl R22.7.4). `[derived]` A hollow section with a small void
(`A_g/A_cp ≥ 0.95`, e.g. an ungrouted post-tensioning duct) can simply be
treated as solid for `T_th` purposes (Cl R22.7.4).

### Equilibrium vs compatibility torsion (Cl 22.7.3)

`[code]` Two distinct design situations (Cl R22.7.3):

- **Equilibrium torsion** — the torsional moment is required for the
  structure's equilibrium and *cannot* be reduced by internal force
  redistribution (e.g. a beam cantilevering a slab off one side, where the
  support torsion is statically determined). Here the member is designed to
  resist the full `T_u` (Cl 22.7.3.1).
- **Compatibility torsion** — torsion arising only from the member twisting
  to maintain deformation compatibility with adjoining members (e.g. a
  spandrel beam restraining a slab's edge rotation), which **can** redistribute
  once the member cracks torsionally. Here, where `T_u ≥ φT_cr` in a
  statically indeterminate structure, `T_u` may be **reduced to `φT_cr`**
  (Cl 22.7.3.2) — and the adjoining members' design moments/shears must then
  be kept in equilibrium with that reduced torsion (Cl 22.7.3.3).

`[derived]` The cracking-torque ceiling on redistributed compatibility
torsion exists specifically to limit torsional crack width after
redistribution (Cl R22.7.3) — it is a serviceability-driven cap, not a
strength argument.

### Nominal torsional strength (Cl 22.7.6)

`[code]` `T_n` is the **lesser of** a stirrup-governed and a
longitudinal-reinforcement-governed expression, both derived from the same
space-truss analogy with compression diagonals at angle `θ`:

**T_n = 2 A_o A_t f_yt cot θ / s**  (Eq. 22.7.6.1a, stirrup/transverse)
**T_n = 2 A_o A_ℓ f_y tan θ / p_h**  (Eq. 22.7.6.1b, longitudinal)

where `A_o` is the gross area enclosed by the shear flow path (may be taken
as `0.85 A_oh`, Cl 22.7.6.1.1), `A_t` is the area of **one leg** of a closed
stirrup, `A_ℓ` is the total longitudinal torsional reinforcement area, and
`p_h` is the perimeter of the outermost closed stirrup's centreline.
`θ` must be the **same value in both equations**, and is bounded
`30° ≤ θ ≤ 60°` if obtained by analysis, or may simply be taken as:

- **45°** for nonprestressed members, or prestressed members with
  `A_ps f_se < 0.4(A_ps f_pu + A_s f_y)` (lightly prestressed) (Cl 22.7.6.1.2a).
- **37.5°** for prestressed members with `A_ps f_se ≥ 0.4(...)` (heavily
  prestressed) (Cl 22.7.6.1.2b).

`[derived]` Picking a smaller `θ` trades less stirrup area for more
longitudinal reinforcement, and vice versa (Cl R22.7.6.1.2) — the two
equations pull in opposite directions as `θ` varies, which is why a single
consistent `θ` is mandatory rather than optimising each independently.

![[aci318-fig-r22.7.6.1a-space-truss-analogy.png]]
*Fig. R22.7.6.1a — space truss analogy: torsion `T` idealised as shear flow
around a thin-walled tube, resolved into wall forces `V₁`–`V₄` carried by
diagonal concrete compression struts at angle `θ` and the closed stirrups
(ACI 318M-19).* `[derived]` Each wall's shear flow `V_i` resolves into a
diagonal compression `D_i = V_i/sin θ` plus a longitudinal tension
`N_i = V_i cot θ`, split half to the top and half to the bottom chord
(Cl R22.7.6.1) — summing `N_i` around all walls is what sizes the total
longitudinal reinforcement `A_ℓ f_y` in Eq. 22.7.6.1b.

![[aci318-fig-r22.7.6.1.1-aoh-definition.png]]
*Fig. R22.7.6.1.1 — `A_oh` (area enclosed by the centreline of the outermost
closed transverse torsional reinforcement) for rectangular, I/T/L-shaped
and circular sections, including with an opening (ACI 318M-19).*

### Cross-sectional size limit under combined shear and torsion (Cl 22.7.7)

`[code]` Cross-section dimensions must satisfy, for solid sections:

**√[(V_u/(b_w d))² + (T_u p_h / (1.7 A_oh²))²] ≤ φ(V_c/(b_w d) + 0.66√f'c)**
(Eq. 22.7.7.1a)

and for hollow sections, the same two shear-stress terms added **directly**
rather than by square-root-sum-of-squares:

**V_u/(b_w d) + T_u p_h / (1.7 A_oh²) ≤ φ(V_c/(b_w d) + 0.66√f'c)**
(Eq. 22.7.7.1b)

`[derived]` The difference in combination rule reflects where the stresses
physically act: in a hollow section the shear-from-`V_u` and
shear-from-torsion both occur in the same box walls and are directly
additive at the critical point; in a solid section, torsional shear acts in
an outer tube while `V_u`'s shear spreads across the full width, so the
combination uses the square-root form instead (Cl R22.7.7.1). This limit is
structurally the same role as the one-way shear size limit of Cl 22.5.1.2
(diagonal-crushing / crack-width control), just extended to include torsion
— see [[aci318-one-way-shear-strength]]. For prestressed members, `d` need not
be taken less than `0.8h` here either (Cl 22.7.7.1.1). For a hollow section
with varying wall thickness, Eq. 22.7.7.1b is evaluated where the combined
stress term is maximum, and if the wall is thinner than `A_oh/p_h` at that
point, the torsion term substitutes the actual wall thickness `t` for
`A_oh/p_h` (Cl 22.7.7.1.2, 22.7.7.2).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-one-way-shear-strength]] — Cl 22.5, the shear provisions this
  chapter's combined shear+torsion size limit builds on.
- [[as3600-beam-shear-and-torsion-design]] — the AS 3600 equivalent
  (also thin-walled tube/space-truss based), for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 22 Cl 22.7 (pp. 420–428), incl.
  Tables 22.7.4.1(a)/(b), 22.7.5.1 and Figs. R22.7.6.1a, R22.7.6.1.1.
