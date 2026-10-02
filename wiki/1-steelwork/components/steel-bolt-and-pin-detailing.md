---
title: Pin connections and bolt/pin detailing limits
category: 1-steelwork
tags: [pins, pin-connection, pitch, edge-distance, holes, detailing]
standards: [AS 4100:2020 Cl 9.4, AS 4100:2020 Cl 9.5]
status: draft
reviewed: 2026-09-13
---

# Pin connections and bolt/pin detailing limits

> Scope: AS 4100:2020 Cl 9.4 (pin in shear, bearing, bending; ply in
> bearing due to a pin) and Cl 9.5 (minimum pitch, minimum/maximum edge
> distance — Table 9.5.2, maximum pitch, maximum edge distance, holes).
> Bolt capacities are on [[steel-bolt-design]]; pin-connected tension
> member detailing (hole geometry) is on [[steel-tension-member-capacity]]
> Cl 7.5.

## Summary

`[code]` Pin strength limit states: shear `V_f = 0.62 f_yp n_s A_p`
(Cl 9.4.1); bearing `V_b = 1.4 f_yp d_f t_p k_p` (Cl 9.4.2, `k_p` = 1.0 no
rotation / 0.5 with rotation); bending `M_p = f_yp S` (Cl 9.4.3); ply
bearing per Cl 9.2.2.4 (Cl 9.4.4). `φ = 0.80` for pin shear/bearing/
bending, `0.90` for ply bearing (Table 3.4).

`[code]` Bolt/pin detailing (Cl 9.5): minimum pitch `2.5 d_f`; minimum edge
distance from Table 9.5.2 by edge preparation; maximum pitch and maximum
edge distance are corrosion/buckling-driven limits; holes per AS/NZS 5131.

## Detail

### Pin in shear (Cl 9.4.1)

`[code]` `V*_f ≤ φV_f`, `φ = 0.80`, `V_f = 0.62 f_yp n_s A_p`: `f_yp` = pin
yield stress, `n_s` = number of shear planes, `A_p` = pin cross-sectional
area.

### Pin in bearing (Cl 9.4.2)

`[code]` `V*_b ≤ φV_b`, `φ = 0.80`, `V_b = 1.4 f_yp d_f t_p k_p`: `d_f` =
pin diameter, `t_p` = connecting-plate thickness(es), `k_p` = 1.0 (pin
without rotation) or 0.5 (pin with rotation — e.g. a pinned bearing
intended to rotate in service).

### Pin in bending (Cl 9.4.3)

`[code]` `M* ≤ φM_p`, `φ = 0.80`, `M_p = f_yp S` (`S` = plastic section
modulus of the pin).

### Ply in bearing due to a pin (Cl 9.4.4)

`[code]` `V*_b ≤ φV_b` per Cl 9.2.2.4, `φ = 0.90`.

`[derived]` Cl 9.5.5 pin-plate detailing (thickness vs hole-edge distance,
net-area-beyond-hole, sum-of-areas-perpendicular) is at Cl 7.5 — see
[[steel-tension-member-capacity]] — since it's stated there as an
additional requirement for pin-connected *tension* members specifically,
not repeated in Section 9.

### Minimum pitch (Cl 9.5.1)

`[code]` Centre-to-centre distance between fastener holes ≥ `2.5 d_f`
(`d_f` = nominal fastener diameter). May be increased by the Cl 9.2.2.4
ply-bearing check (component of force toward an adjacent hole).

### Minimum edge distance (Cl 9.5.2, Table 9.5.2)

`[code]`
- **Standard holes** (Cl 14.3.2 size): edge distance measured from hole
  centre to the plate/section edge, per Table 9.5.2.
- **Non-standard (oversize/slotted) holes**: measured from the **nearer
  edge of the hole** to the physical edge, **plus half the fastener
  diameter**, per Table 9.5.2.

| Edge condition | Minimum edge distance |
|---|---|
| Sheared or hand flame-cut edge | `1.75 d_f` |
| Rolled plate, flat bar or section: machine cut, sawn or planed edge | `1.50 d_f` |
| Rolled edge of a rolled flat bar or section | `1.25 d_f` |

May also be increased by Cl 9.2.2.4 (ply bearing toward an edge).

### Maximum pitch (Cl 9.5.3)

`[code]` Lesser of `15 t_p` (`t_p` = thinner connected ply) or 200 mm,
**except**: (a) fasteners not carrying design actions, in a region not
liable to corrosion — lesser of `32 t_p` or 300 mm; (b) an outside line of
fasteners in the direction of the design action — lesser of `(4t_p + 100)`
mm or 200 mm.

`[derived]` Case (b) is the classic built-up-member stitch-bolt spacing
rule (e.g. double-angle or gusset-connected flange plates) — it is tighter
than the general 15t_p/200 mm rule to control local plate buckling between
the outer bolt line and the free edge.

### Maximum edge distance (Cl 9.5.4)

`[code]` ≤ `12 t` (`t` = thinnest outer connected ply in contact), and
≤ 150 mm.

### Holes (Cl 9.5.5)

`[code]` Holes for bolts and pins per AS/NZS 5131.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[steel-bolt-design]] — bolt strength limit states, bolting categories.
- [[steel-tension-member-capacity]] — Cl 7.5 pin-connected tension member
  hole/plate rules.
- [[steel-connection-design-requirements]] — general connection
  provisions, minimum design actions.
- [[steel-fabrication-and-erection-requirements]] — Cl 14.3.2 hole sizes
  by category, referenced here for "standard hole".

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Cl 9.4–9.5
  (pp. 123–125).
