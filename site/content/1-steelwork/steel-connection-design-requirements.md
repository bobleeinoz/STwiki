---
title: Connection design requirements — general, minimum actions, holes, block shear
category: 1-steelwork
tags: [connections, minimum-design-actions, block-shear, hole-deductions, staggered-holes, prying, hollow-section-connections]
standards: [AS 4100:2020 Cl 9.1]
status: draft
reviewed: 2026-09-13
---

# Connection design requirements — general provisions

> Scope: AS 4100:2020 Cl 9.1 — connection classification by form of
> construction, general design philosophy, minimum design actions on
> connections, intersections, choice of fasteners, combined connections,
> prying forces, connection component capacity (including block shear),
> hole deductions (staggered/non-staggered), hollow section connections.
> Bolt, pin and weld capacities are on [[steel-bolt-design]] and
> [[steel-weld-design]]; detailing limits are on
> [[steel-bolt-and-pin-detailing]].

## Summary

`[code]` Connections must be proportioned consistently with the analysis
assumption (rigid/semi-rigid/simple, Cl 4.2) and capable of transmitting
the calculated design action effects (Cl 9.1.1). Each connection has a
**minimum design action** independent of the calculated actions
(Cl 9.1.4) — e.g. simple-construction beam connections need ≥ the lesser
of `0.15 ×` the member design shear capacity or 40 kN.

## Detail

### Classification by form of construction (Cl 9.1.2)

`[code]`
- **Rigid** (9.1.2.1): conform to Cl 4.2.2; joint deformations must not
  significantly affect the frame's action-effect distribution or overall
  deformation.
- **Semi-rigid** (9.1.2.2): conform to Cl 4.2.3; must provide a predictable
  degree of interaction based on **experimentally determined**
  action-deformation behaviour.
- **Simple** (9.1.2.3): conform to Cl 4.2.4; must be able to deform to
  provide the required rotation without developing a restraining moment
  that adversely affects the structure; rotation capacity demonstrated
  experimentally; treated as subject to reaction shear at an eccentricity
  appropriate to the detailing.
- **Plastically analysed structures** (9.1.2.4): connections conform to
  Cl 4.5.3 in addition to Section 9.

### Design of connections (Cl 9.1.3)

`[code]` Each connection element's design capacity ≥ its calculated design
action effect. For earthquake load combinations: design for the calculated
action effects, exhibit the required ductility, and conform to Section 13.
Distributed design action effects in a connection must: (a) be in
equilibrium with the actions on the connection; (b) keep deformations within
element deformation capacities; (c) let every element and adjacent member
area resist the effects acting on it; (d) remain stable under the actions
and deformations. Design on a recognised, experimentally supported method.
Bolt-installation residual actions need not be considered.

### Minimum design actions on connections (Cl 9.1.4)

`[code]` Except lacing connections and connections to sag rods, purlins and
girts, design for the **greater of** the actual design action in the member
and the following minimums:

| Connection type | Minimum design action |
|---|---|
| Rigid construction | Bending moment = 0.5 × member design moment capacity |
| Beam in simple construction | Shear = lesser of 0.15 × member design shear capacity and 40 kN |
| Ends of tensile or compression members | Force = 0.3 × member design capacity (except threaded-rod bracing with turnbuckles: minimum tensile force = full member design capacity) |
| Splice in a member subject to axial tension | Force = 0.3 × member design tension capacity |
| Splice in a member subject to axial compression, ends prepared for full contact | ≥ 0.15 × member design compression capacity (bearing on contact surfaces permitted for the balance); PLUS, for splices between points of lateral support, `N*` plus `M* = δN*l_s/1000` (`δ` = δ_b or δ_s per Cl 4.4, `l_s` = distance between points of lateral support) |
| Splice in axial compression, not prepared for full contact | Force = 0.3 × member design compression capacity, splice material/fasteners arranged to hold parts in line |
| Splice in a flexural member | Bending moment = 0.3 × member design moment capacity (not applicable to shear-only splices) |
| Splice designed to transmit shear only | Design shear force + any moment from the eccentricity of that force about the connector-group centroid |
| Splice in a member with combined actions | Items (iv), (v) and (vi) above satisfied simultaneously |

Earthquake load combinations may require these minimums to be increased to
meet Section 13's ductility demands.

`[practice]` (ASI Handbook 1 Ch 8.1) The minimum is generally expressed as
a factor times the design capacity of the **minimum member size required
by the strength limit state** — not the design capacity of whatever
(possibly larger) member size is actually used. So if a member is
up-sized for a reason unrelated to strength (slenderness, serviceability,
section rationalisation), the minimum design action for its connection is
still pegged to the smallest strength-adequate member, not the larger
member actually specified. Where a member/splice must resist large
compression but only minor tension (or vice versa), both the
compression-based and tension-based minimums must be satisfied
independently.

### Intersections (Cl 9.1.5)

`[code]` Members/components at a joint should transfer actions with
centroidal axes meeting at a point wherever practicable; where there is
eccentricity, design for the resulting bending moments. Balancing fillet
welds about the centroidal axis for single/double angle end connections is
**not required for statically loaded members** but **is required for
fatigue-loaded members and connection components**. Eccentricity between
angle centroidal axes and bolted-connection gauge lines may be neglected
for statically loaded members but must be accounted for under fatigue
loading.

### Choice of fasteners (Cl 9.1.6)

`[code]` Where SLS slip must be avoided: high-strength bolts in a
friction-type joint (category 8.8/TF or 10.9/TF), fitted bolts, or welds.
Where a joint is subject to impact or vibration: 8.8/TF or 10.9/TF bolts,
locking devices, or welds.

### Combined connections (Cl 9.1.7)

`[code]` Non-slip fasteners (friction-type high-strength bolts, welds) used
with slip-type fasteners (snug-tight bolts, tensioned bearing-type bolts):
assume the non-slip fasteners resist **all** design actions. A mixture of
non-slip fastener types may share load. Welding combined with other
non-slip fasteners: actions applied before welding are resisted by the
pre-existing fasteners only (not redistributed to the weld); actions
applied after welding are resisted by the weld.

### Prying forces (Cl 9.1.8)

`[code]` Bolts carrying design tension must be proportioned to also resist
any additional tension from prying action.

### Connection components (Cl 9.1.9)

`[code]` Cleats, gusset plates, brackets etc. (not connectors) are assessed:
(a) shear — Cl 5.11; (b) tension — Cl 7.2; (c) compression — Section 6;
(d) bending — Section 5.

`[code]` **Block shear** (9.1.9(e)) — a connection component (including a
member framing onto it) subject to design shear or tension:
`R*_bs ≤ φR_bs`, `φ = 0.75`,

`R_bs = 0.6 f_uc A_nv + k_bs f_uc A_nt ≤ 0.6 f_yc A_gv + k_bs f_uc A_nt`

- `f_uc`, `f_yc` = tensile strength / yield stress of the connection element.
- `A_nv` = net area subject to shear at rupture; `A_nt` = net area subject to
  tension at rupture; `A_gv` = gross area subject to shear at rupture.
- `k_bs` = 1.0 for uniform tension stress, 0.5 for non-uniform tension
  stress (e.g. a bolt group with an eccentric tension component).

`[derived]` Block shear governs coped beam ends and gusset-plate corners
where a torn-out block combines shear rupture along one path with tension
rupture along a perpendicular path — check it whenever a connection removes
material near a free edge or a cope, not just at the fastener line itself.

### Deductions for fastener holes (Cl 9.1.10)

`[code]`
- **Hole area** (9.1.10.1): use the gross area of the hole in the plane of
  its axis (countersunk holes included).
- **Not staggered** (9.1.10.2): deduct the maximum sum of hole areas in any
  cross-section perpendicular to the design action.
- **Staggered** (9.1.10.3): deduct the greater of (a) the non-staggered
  deduction, and (b) the sum of all hole areas in any zig-zag line across
  the member, **less** `s_p² t / (4 s_g)` for each gauge space in the chain,
  where `s_p` = staggered pitch (centre-to-centre along the load direction),
  `t` = holed-material thickness, `s_g` = gauge (centre-to-centre
  perpendicular to the load direction; for angles with holes in both legs,
  the sum of the back marks less the leg thickness).

![[as4100-fig-9.1.10.3A-staggered-holes.png]]
*Figure 9.1.10.3(A) — staggered holes: zig-zag line, s_p and s_g (AS 4100:2020).*

![[as4100-fig-9.1.10.3B-angles-both-legs.png]]
*Figure 9.1.10.3(B) — angles with holes in both legs: gauge = sum of back marks − leg thickness (AS 4100:2020).*

### Hollow section connections (Cl 9.1.11)

`[code]` Where design actions from one member are applied to a hollow
section at a connection, the design must include local effects on the
hollow section (e.g. face/punching shear, local wall bending — not further
quantified in AS 4100 itself; specialist hollow-section connection guidance
applies).

## Worked reference

None yet.

## Contradictions

`[practice]` **Block shear formula divergence** — see
[[steel-connection-component-capacity]] Contradictions section. The
Cl 9.1.9(e) formula above is the applicable AS 4100:2020 text; the ASI
Handbook 1 (2007) instead recommends a Kulak/AISC-derived expression
(`φV_bs = φ[A_nt f_ui + 0.6 f_yi A_gv]`) for connection components that is
not algebraically equivalent to it. Cl 9.1.9(e) governs for code
compliance.

## Related

- [[steel-bolt-design]] — Cl 9.2, 9.3 bolt and bolt-group capacities.
- [[steel-bolt-and-pin-detailing]] — Cl 9.4, 9.5 pins and detailing limits.
- [[steel-weld-design]] — Cl 9.6, 9.7 welds and weld groups.
- [[steel-tension-member-capacity]] — Cl 7.2 net area, used with the hole
  deduction rules here.
- [[steel-web-shear-and-bearing]] — Cl 5.11 shear capacity referenced for
  connection-component shear.
- [[steel-connection-component-capacity]] — full rectangular-component
  shear/bending/compression/tension/block-shear derivation (ASI Handbook 1
  Ch 5).
- [[steel-connection-classification-and-design-philosophy]] — background
  on connection design models.
- [[asi-design-capacity-tables-vol1-open-sections]] — Part 9 "standardised
  structural connections" rationalised components (1999 design aid).

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Cl 9.1 (pp. 113–117).
  Figures 9.1.10.3(A)/(B) reproduced in `wiki/1-steelwork/assets/`.
