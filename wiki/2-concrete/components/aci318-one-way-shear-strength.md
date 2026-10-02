---
title: ACI 318M-19 one-way shear strength — Vc size effect, Vs, biaxial shear
category: 2-concrete
tags: [aci, shear, one-way-shear, size-effect, sectional-strength]
standards: [ACI 318M-19 Cl 22.5]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 one-way shear strength

> Scope: ACI 318M-19 Cl 22.5 — nominal one-way shear strength `V_n = V_c +
> V_s`, the cross-section size limit, the 2019-revised `V_c` equations for
> nonprestressed members (including the new size-effect factor `λ_s`),
> prestressed-member `V_c` methods, reduced-prestress regions near
> pretensioned member ends, and shear reinforcement (`V_s`). This is an
> **ACI 318M-19 page, kept separate from the AS 3600:2018 concept pages**
> elsewhere in `2-concrete` — see [[aci-318m-19-building-code-concrete]] for
> why.

## Summary

`[code]` Nominal one-way shear strength is `V_n = V_c + V_s` (Eq. 22.5.1.1) —
concrete contribution plus steel (transverse reinforcement or bent-up bar)
contribution. `[code]` **The nonprestressed `V_c` equations were substantially
revised in the 2019 Code** to explicitly include a member-depth "size effect"
and the longitudinal reinforcement ratio, replacing the simpler pre-2019
`V_c = 0.17λ√f'c b_w d` formula used unconditionally. A page citing a flat
`0.17λ√f'c b_w d` for every nonprestressed member (no size-effect factor, no
reinforcement-ratio term) is citing a pre-2019 edition.

## Detail

### Cross-section size limit (Cl 22.5.1.2)

`[code]` Cross-sectional dimensions must satisfy:

**V_u ≤ φ(V_c + 0.66√f'c b_w d)**  (Eq. 22.5.1.2)

`[derived]` This caps total shear strength (concrete + steel combined) at a
level intended to avoid diagonal-compression (web-crushing) failure in the
concrete and limit crack extent (Cl R22.5.1.2) — structurally the same role
as AS 3600's own diagonal-crushing shear limit (see
[[concrete-beam-shear-and-torsion-design]]), though the two codes' limiting
coefficients and `V_c` definitions are not interchangeable.

### Other general provisions (Cl 22.5.1, 22.5.2, 22.5.3)

`[code]` `V_c` for nonprestressed members: Cl 22.5.5 (below). For prestressed
members: Cl 22.5.6 or 22.5.7. `λ` (lightweight-concrete modification factor)
always per Cl 19.2.4. Openings in a member must be accounted for in `V_n`
(Cl 22.5.1.7) — the strut-and-tie method of Chapter 23 is available for
members with openings or other discontinuities. Axial tension from creep/
shrinkage must be considered in `V_c` (Cl 22.5.1.8); inclined flexural
compression in variable-depth members may optionally be considered
(Cl 22.5.1.9).

`[code]` **Biaxial shear** (Cl 22.5.1.10–22.5.1.11): interaction between
orthogonal shear forces may be neglected if either direction's demand/
capacity ratio alone is ≤ 0.5 (`v_u,x/(φv_n,x) ≤ 0.5` or
`v_u,y/(φv_n,y) ≤ 0.5`, Eq. 22.5.1.10a/b). Otherwise a linear interaction
check applies: `v_u,x/(φv_n,x) + v_u,y/(φv_n,y) ≤ 1.5` (Eq. 22.5.1.11).
`[code]` Circular sections may use the resultant shear directly since their
one-way shear strength is the same about every axis (Cl R22.5.1.10); for
calculation purposes a circular section takes `d = 0.8 × diameter` and
`b_w = diameter` (solid) or `b_w = 2 × wall thickness` (hollow) (Cl 22.5.2.2).

`[code]` **Material strength limits** (Cl 22.5.3): `√f'c` used for `V_c`,
`V_ci`, `V_cw` is capped as if `f'c ≤ 8.3 MPa` (i.e. `√f'c` capped at
√8.3 ≈ 2.88), **unless** the beam/joist has minimum web reinforcement per
Cl 9.6.3.4/9.6.4.2, lifting the cap — there is a lack of test data above this
for shear (Cl R22.5.3.1). `f_y`/`f_yt` used for `V_s` are capped per
Cl 20.2.2.4 (420 MPa) to control diagonal crack widths (Cl R22.5.3.3).

### Vc for nonprestressed members (Cl 22.5.5) — the 2019 size-effect revision

`[code]` `V_c` depends on whether shear reinforcement meets the minimum
`A_v,min` (Table 9.6.3.4/10.6.2.2):

![[aci318-table-22.5.5.1-vc-nonprestressed-members.png]]
*Table 22.5.5.1 — `V_c` for nonprestressed members: `A_v ≥ A_v,min` may use
either the simple expression (a) or the reinforcement-ratio expression (b);
`A_v < A_v,min` must use the size-effect expression (c), `λ_s` ≤ 1
(ACI 318M-19).*

`[code]` The **size-effect modification factor**:

**λ_s = √(2 / (1 + 0.004d)) ≤ 1**  (Eq. 22.5.5.1.3, `d` in mm)

`[derived]` only applies where `A_v < A_v,min` — i.e. lightly/un-reinforced
members, where test data (Kuchma et al. 2019) shows measured shear strength
does **not** scale in direct proportion with member depth (doubling depth
less than doubles shear-at-failure, Cl R22.5.5.1.1). Members with
`A_v ≥ A_v,min` are not subject to `λ_s` at all — they may use either
expression (a) (simpler, ignores reinforcement ratio) or (b) (uses `ρ_w^(1/3)`,
generally less conservative for lightly-longitudinally-reinforced sections).
`N_u` is positive for compression, negative for tension, and `V_c` is never
taken less than zero even if the `N_u` term would drive it negative
(Table 22.5.5.1 notes).

`[code]` Two further caps: `V_c` never exceeds `0.42λ√f'c b_w d`
(Cl 22.5.5.1.1), and the `N_u/6A_g` term in Table 22.5.5.1 is capped at
`0.05 f'c` (Cl 22.5.5.1.2).

### Vc for prestressed members (Cl 22.5.6–22.5.7)

`[code]` Where `A_ps f_se ≥ 0.4(A_ps f_pu + A_s f_y)` (i.e. a reasonably
heavily-prestressed section), `V_c` may use the simplified Table 22.5.6.2
expression (least of three terms, one of which is the same `0.42λ√f'c b_w d`
upper bound as the nonprestressed case), subject to a `0.17λ√f'c b_w d`
floor — or the more rigorous Cl 22.5.6.3 method instead.

`[derived]` The rigorous method (Cl 22.5.6.3) takes `V_c` as the **lesser of
two physically distinct inclined-cracking modes** (Cl R22.5.6.3): **flexure-
shear cracking** `V_ci` (initiated by a flexural crack, then driven inclined
by combined shear + flexural tension — Eq. 22.5.6.3.1a, with floors at
Eq. 22.5.6.3.1b/c depending on the same `A_ps f_se` prestress-level test as
above) and **web-shear cracking** `V_cw` (principal tensile stress exceeding
concrete's tensile strength at an interior point, away from any flexural
crack — Eq. 22.5.6.3.2, or the alternative principal-stress check of
Cl 22.5.6.3.3 at the centroidal axis or flange/web junction). Not
reproduced here as full equations given their narrow applicability
(prestressed-member shear design specifically) — see Cl 22.5.6.3.1–22.5.6.3.4
in the source.

`[code]` **Reduced prestress near pretensioned member ends** (Cl 22.5.7):
within the transfer length `ℓ_tr` (taken as `50d_b` for strand, `100d_b` for
wire, Cl 22.5.7.1), effective prestress is assumed to vary linearly from
zero at the strand end (or at the point bonding commences, for debonded
strand) up to its full value at `ℓ_tr` — this reduced force must then be used
consistently in both the Cl 22.5.6.2 applicability test and the `V_cw`
calculation (Cl 22.5.7.2–22.5.7.5).

### One-way shear reinforcement (Cl 22.5.8)

`[code]` Wherever `V_u > φV_c`, transverse reinforcement must be provided
such that `V_s ≥ V_u/φ − V_c` (Eq. 22.5.8.1). Permitted shear reinforcement
types: stirrups/ties/hoops perpendicular to the member axis, welded wire
reinforcement with perpendicular wires, or spiral reinforcement
(Cl 22.5.8.5.1); inclined stirrups at ≥ 45° to the axis are also permitted in
nonprestressed members (Cl 22.5.8.5.2), as are bent-up longitudinal bars at
≥ 30° (Cl 22.5.8.6.1). Where more than one shear-reinforcement type is used
together, `V_s` is the sum of each type's contribution (Cl 22.5.8.4).

`[code]` **Perpendicular transverse reinforcement**: `V_s = A_v f_yt d / s`
(Eq. 22.5.8.5.3). **Inclined stirrups** at angle `α`: `V_s = A_v f_yt d
(sin α + cos α) / s` (Eq. 22.5.8.5.4) — `s` measured parallel to the
longitudinal reinforcement. `A_v` is the effective area of all legs/wires
within spacing `s` for a rectangular tie/stirrup/hoop/crosstie
(Cl 22.5.8.5.5), or twice the bar/wire area for a circular tie or spiral
(Cl 22.5.8.5.6).

`[code]` **Bent-up longitudinal bars**: a single bar/group bent the same
distance from the support gives `V_s` as the lesser of `A_v f_y sin α`
(Eq. 22.5.8.6.2a) and `0.25√f'c b_w d` (Eq. 22.5.8.6.2b) — the second term
caps reliance on bent-up bars regardless of how much steel is provided. A
series of bars bent at different distances from the support instead uses the
same inclined-stirrup equation (22.5.8.5.4).

`[derived]` Inclined stirrups/bent-up bars only work if they actually cross
the potential shear crack — the Commentary explicitly warns that
reinforcement oriented close to parallel with the expected crack provides no
real shear strength regardless of area provided (Cl R22.5.8.5.4, R22.5.8.6).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-sectional-strength-flexure-and-axial]] — Cl 22.2–22.4, same chapter's
  flexure/axial provisions and the φ this V_n feeds into via Chapter 21.
- [[aci318-two-way-shear-strength]] — Cl 22.6, the companion punching-shear
  provisions for slabs/footings.
- [[aci318-one-way-slab-design]] — Chapter 7, which invokes this page's `V_n`
  for the slab shear design strength check (Cl 7.5.3.1).
- [[concrete-beam-shear-and-torsion-design]] — the AS 3600 MCFT-based
  equivalent, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 22 Cl 22.5 (pp. 401–411), incl.
  Table 22.5.5.1.
