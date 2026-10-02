---
title: ACI 318M-19 bearing and shear friction — frustum A2, coefficient of friction
category: 2-concrete
tags: [aci, bearing, shear-friction, sectional-strength]
standards: [ACI 318M-19 Cl 22.8, ACI 318M-19 Cl 22.9]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 bearing and shear friction

> Scope: ACI 318M-19 Cl 22.8 (bearing strength — the frustum method for a
> confined bearing area) and Cl 22.9 (shear friction — the clamping-force
> model for shear transfer across an existing or potential crack or
> dissimilar-material interface). This is an **ACI 318M-19 page, kept
> separate from the AS 3600:2018 concept pages** elsewhere in `2-concrete` —
> see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Bearing (Cl 22.8) and shear friction (Cl 22.9) are the last two
sectional-strength mechanisms in Chapter 22, both φ-tagged in Table 21.2.1
(bearing φ = 0.65; shear friction uses the shear φ = 0.75, see
[[aci318-strength-reduction-factors]]). Bearing strength does **not** apply to
post-tensioned anchorage zones — those are designed per Cl 25.9 instead
(Cl 22.8.1.2).

## Detail

### Bearing (Cl 22.8)

`[code]` Design requirement: `φB_n ≥ B_u` (Eq. 22.8.3.1) for each applicable
factored load combination, with `B_u` from the Chapter 5 load combinations
and Chapter 6 analysis (Cl 22.8.2.1).

![[aci318-table-22.8.3.2-nominal-bearing-strength.png]]
*Table 22.8.3.2 — nominal bearing strength `B_n`: where the supporting
surface is wider on all sides than the loaded area `A₁`, the lesser of a
confinement-enhanced term (using `A₂`, capped at 2×) and a flat `0.85f'c A₁`
otherwise (ACI 318M-19).*

`[code]` `A₁` is the loaded area (not greater than the bearing plate/cross-
section); `A₂` is the area of the lower base of the **largest frustum** of a
pyramid/cone/tapered wedge, contained wholly within the support, whose upper
base equals `A₁`, with sides sloped **1 vertical to 2 horizontal**
(Cl 22.8.3.2):

![[aci318-fig-r22.8.3.2-frustum-bearing-area.png]]
*Fig. R22.8.3.2 — application of the frustum to find `A₂` for stepped or
sloped supports: plan view shows the 45° (1:2 slope → arctan(0.5) ≈ 26.6°
from vertical, drawn here as the in-plan spread) frustum projection from the
loaded area; elevation shows `A₂` measured at the plane where the frustum
first intersects a support boundary (ACI 318M-19).*

`[code]` The `0.85f'c` permissible bearing stress is empirical (Hawkins
1968); the confinement-enhanced term `√(A₂/A₁)(0.85f'c A₁)` reflects that
surrounding concrete restrains lateral expansion of the bearing zone when
the support is wider than the loaded area on all sides, raising effective
bearing strength (Cl R22.8.3.2). `[derived]` The Commentary stresses that
the frustum is a **stress-confinement idealisation, not a load-dispersion
path** — an actual load path through the support fans out at a steeper
angle than the 1:2 frustum used here (Cl R22.8.3.2). No minimum support
depth is given — that is instead controlled by the Cl 22.6 punching shear
check (Cl R22.8.3.2). The bearing provisions only cover the compression
component normal to the bearing surface; any tangential component needs a
separate load path (e.g. anchor bolts, shear lugs) (Cl R22.8.3.2).

### Shear friction (Cl 22.9)

`[code]` Applies wherever shear transfer across an assumed plane needs
checking: an existing or potential crack, a dissimilar-material interface,
or an interface between concretes cast at different times (Cl 22.9.1.1).
Design requirement: `φV_n ≥ V_u` (Eq. 22.9.3.1). Surface preparation assumed
for the design must be stated in the construction documents (Cl 22.9.1.4) —
it directly sets which `μ` row of Table 22.9.4.2 applies.

`[derived]` **Model**: reinforcement crossing the assumed crack is stressed
to `f_y` by the crack faces separating as they slip past each other under
shear; this tension clamps the crack faces together with force `A_vf f_y`,
and the applied shear is resisted by friction between the faces, shearing-off
of surface protrusions, and dowel action of the crossing bars (Cl R22.9.1.1).
Because the model lumps all of this into a single "friction" term, the `μ`
values used are **deliberately higher than true material friction
coefficients** — calibrated so the equation's output matches test results,
not a physical friction measurement (Cl R22.9.4.2).

`[code]` **Perpendicular reinforcement**:

**V_n = μ A_vf f_y**  (Eq. 22.9.4.2)

![[aci318-table-22.9.4.2-coefficients-of-friction.png]]
*Table 22.9.4.2 — coefficient of friction `μ` by contact-surface condition:
1.4λ monolithic, 1.0λ intentionally roughened to ≈6 mm amplitude, 0.6λ
hardened-but-unroughened, 0.7λ against as-rolled structural steel with
studs/welded bars (ACI 318M-19).* `[derived]` The unroughened-interface
value (0.6λ) is markedly lower because shear transfer there is primarily by
dowel action rather than friction/interlock (Cl R22.9.4.2) — a page
specifying only one blanket `μ` value for "cast against hardened concrete"
without checking whether it was intentionally roughened is citing the wrong
row.

`[code]` **Inclined reinforcement** (where the shear force component along
the bar induces **tension** in it):

**V_n = A_vf f_y (μ sin α + cos α)**  (Eq. 22.9.4.3, α = angle between the
reinforcement and the shear plane)

![[aci318-fig-r22.9.4.3ab-inclined-shear-friction-reinforcement.png]]
*Figs. R22.9.4.3a/b — inclined shear-friction reinforcement: (a) where the
shear force puts the bar in **tension**, Eq. 22.9.4.3 applies; (b) where it
would put the bar in **compression**, shear friction does not apply at all
(`V_n = 0`) (ACI 318M-19).*

`[code]` `f_y` for shear friction is capped per Cl 20.2.2.4 (420 MPa)
(Cl 22.9.1.3) — same cap used for one-way/two-way shear reinforcement.

`[code]` **Upper limit** (Cl 22.9.4.4), since Eq. 22.9.4.2/22.9.4.3 alone can
become unconservative for some cases (Cl R22.9.4.4):

![[aci318-table-22.9.4.4-max-vn-shear-friction.png]]
*Table 22.9.4.4 — maximum `V_n` across the assumed shear plane:
intentionally-roughened/monolithic normalweight concrete gets the least of
three strength-dependent/flat-stress terms; all other cases are capped
lower, at the lesser of two terms (ACI 318M-19).* Where concretes of
different strengths meet at the interface, the **lesser** `f'c` governs
(Cl 22.9.4.4).

`[code]` **Permanent net compression** across the shear plane may be added
directly to the `A_vf f_y` clamping force when calculating required `A_vf`
(Cl 22.9.4.5) — `[derived]` this reduction is only valid if that compression
is permanent (Cl R22.9.4.5), since shear friction relies on the clamping
force being present for the full service life of the connection, not just at
the moment of peak shear.

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-strength-reduction-factors]] — Chapter 21, the φ = 0.65 (bearing) and
  φ = 0.75 (shear friction, same as shear) used here.
- [[aci318-one-way-shear-strength]] — Cl 22.5, the companion sectional-shear
  provisions in the same chapter.
- [[concrete-anchorage-zones-and-bearing-surfaces]] — the AS 3600 equivalent
  for bearing, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 22 Cl 22.8–22.9 (pp. 428–433),
  incl. Tables 22.8.3.2, 22.9.4.2, 22.9.4.4 and Figs. R22.8.3.2, R22.9.4.3a/b.
