---
title: Tension member capacity, k_t distribution factor and built-up tension members
category: 0-standards
tags: [tension, net-area, kt, shear-lag, eccentric-connection, built-up-members, pin-connection]
standards: [AS 4100:2020 Section 7]
status: draft
reviewed: 2026-09-13
---

# Tension member capacity

> Scope: AS 4100:2020 Section 7 — `N_t` on gross yield and net fracture,
> the force-distribution correction factor `k_t` (Table 7.3.2), two- or
> more-component tension members (back-to-back, laced, battened), and
> additional requirements for pin-connected tension members.

## Summary

`[code]` `N* ≤ φN_t` (Cl 7.1), `φ = 0.9`, with `N_t` the lesser of
`A_g f_y` and `0.85 k_t A_n f_u` (Cl 7.2). `A_n` = gross area less all
penetrations and holes (fastener holes per Cl 9.1.10); threaded rods use
the AS 1275 tensile stress area. `k_t = 1.0` for uniform force
distribution (Cl 7.3.1), otherwise from Table 7.3.2 for eccentrically
connected angles, channels and tees, or 0.85 for I-sections/channels
connected by both flanges only (Cl 7.3.2).

## Detail

### Uniform force distribution (Cl 7.3.1)

`[code]` `k_t = 1.0` where the end connection (a) connects **each part** of
the member symmetrically about the centroidal axis, and (b) each part of the
connection transmits at least the maximum design force in the connected
part.

### Non-uniform force distribution (Cl 7.3.2)

`[code]` Otherwise design to Section 8 (combined actions, eccentricity
moment) with `k_t = 1.0`, **except** that Cl 7.2 may still be used for:
(a) eccentrically connected angles, channels and tees with `k_t` from
Table 7.3.2; (b) symmetrical rolled/built-up I-sections or channels
connected by both flanges only, `k_t = 0.85`, provided the connection length
(first to last fastener row, or longitudinal weld length each side of each
flange) is at least the member depth and each flange connection carries at
least half the maximum design force.

![[as4100-table-7.3.2-kt-correction-factor.png]]
*Table 7.3.2 — correction factor k_t (AS 4100:2020).*

`[code]` Own transcription of Table 7.3.2:

| Case | Configuration | k_t |
|---|---|---|
| (a) | Single angle connected by one leg to a gusset | 0.75 for unequal angles connected by the short leg; 0.85 otherwise |
| (b) | Two angles back-to-back on one side of a gusset, connected by one leg each | as for (a) |
| (c) | Channel connected by web only (flanges outstanding) | 0.85 |
| (d) | Tee connected by flange only | 0.90 |
| (e) | Two angles either side of a gusset (star / cruciform pattern) | 1.0 |
| (f) | Two channels back-to-back either side of a gusset | 1.0 |
| (g) | Two tees flange-to-flange either side of a gusset | 1.0 |

`[derived]` For a single 100×100×8 EA (`[practice]` shorthand `EA` = AS/NZS
3679.1 Grade 300 equal angle) bolted through one leg with one M20 bolt (22 mm
hole): `A_g = 1500 mm²`, `A_n = 1500 − 22×8 = 1324 mm²`, `f_y = 320`
(t < 11), `f_u = 440`: `A_g f_y = 480 kN`; `0.85 × 0.85 × 1324 × 440 =
421 kN` → `N_t = 421 kN`, `φN_t = 379 kN`. Fracture on the net section
governs for single-leg-connected angles in most cases.

### Tension members with two or more main components (Cl 7.4)

`[code]`
- Connections between components resist the internal actions from the
  external design forces and moments; lacing bar forces and batten
  forces/moments are shared equally among connection planes parallel to the
  force (7.4.2).
- **Back-to-back** (7.4.3): separated components connected at intervals so
  the component slenderness between connections ≤ 300, or by connections
  per Cl 6.5.1.4/6.5.1.5; components in contact connected per Cl 6.5.2.4/
  6.5.2.5.
- **Laced** (7.4.4): per Cl 6.4.2 except lacing slenderness ≤ 210 and main
  component slenderness between lacing points ≤ 300; tie plates per
  Cl 6.4.2.7 but thickness ≥ 0.017 × distance between innermost connection
  lines.
- **Battened** (7.4.5): per Cl 6.4.3 except batten spacing so main component
  slenderness ≤ 300; bolted battens need ≥ 2 bolts and Cl 6.4.3.7 does not
  apply; batten thickness ≥ 0.017 × distance between innermost connection
  lines; intermediate battens ≥ half the effective width of end battens.

### Pin-connected tension members (Cl 7.5)

`[code]` Pin capacity per Cl 9.4 ([[as4100-bolt-and-pin-detailing]] /
[[as4100-bolt-design]]), plus: (a) an unstiffened element containing a pin
hole must be ≥ 0.25 × the distance from the hole edge to the element edge
measured perpendicular to the member axis (not applicable to internal plies
clamped by external nuts); (b) net area beyond the hole, parallel to or
within 45° of the member axis, ≥ the net area required for the member;
(c) sum of areas at the hole perpendicular to the axis ≥ 1.33 × the required
net area; (d) pin plates arranged to avoid eccentricity and proportioned to
distribute load from pin to member.

## Worked reference

See the `[derived]` single-angle example above.

## Contradictions

None recorded.

## Related

- [[as4100-built-up-compression-members]] — Cl 6.4/6.5 rules referenced by
  Cl 7.4.
- [[as4100-combined-actions-section-capacity]] — Section 8 path for
  eccentric connections not covered by Table 7.3.2.
- [[as4100-connection-design-requirements]] — Cl 9.1.10 hole deductions
  (staggered holes) used for `A_n`.
- [[as4100-bolt-design]] — Cl 9.4 pin connections.
- [[as4100-materials-and-design-strengths]] — `f_y`, `f_u`.
- [[asi-design-capacity-tables-vol1-open-sections]] — Part 7 `φN_t` design
  section capacity tables per section/grade.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Section 7 (pp. 99–102).
  Table 7.3.2 reproduced in `wiki/0-standards/assets/`.
