---
title: Slab vibration, moment-resisting width for concentrated loads, and composite longitudinal shear
category: 2-concrete
tags: [slabs, vibration, concentrated-loads, composite]
standards: [AS 3600:2018 Cl 9.6-9.8]
status: draft
reviewed: 2026-09-12
---

# Slab vibration, concentrated-load moment width, and composite shear

> Scope: three short Section 9 clauses grouped on one page — vibration
> (Cl 9.6), the effective moment-resisting width of one-way slabs under
> concentrated loads (Cl 9.7), and longitudinal shear in composite slabs
> (Cl 9.8, a direct pointer to Cl 8.4).

## Detail

### Vibration of slabs (Cl 9.6)

`[code]` Same framing as beam vibration (Cl 8.7, see
[[concrete-beam-vibration-tbeams-slenderness]]): must be considered and
mitigated where machinery or vehicular/pedestrian traffic vibration would
adversely affect serviceability — no calculation method prescribed.

### Moment-resisting width for one-way slabs under concentrated loads (Cl 9.7)

`[code]` For a solid one-way simply-supported or continuous slab, the width
deemed to resist a concentrated load's moment: away from an unsupported edge,
`bef = load width + 2.4a·[1.0 − (a/Ln)]`, where `a` is the perpendicular
distance from the nearer support to the section considered — the effective
width shrinks as the load approaches midspan (`a/Ln` grows). Near an
unsupported edge, `bef` is capped at the lesser of the away-from-edge value
and half that value plus the distance from the load centre to the
unsupported edge — reflecting reduced lateral load spread where there's no
slab material on one side to help distribute the moment.

### Longitudinal shear in composite slabs (Cl 9.8)

`[code]` Composite slab systems (e.g. precast planks with a cast-in-situ
topping) are checked for longitudinal shear at component interfaces using
Cl 8.4 — see [[concrete-beam-longitudinal-shear-composite]]. No
slab-specific modification to that method is introduced here.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-beam-vibration-tbeams-slenderness]] — the equivalent beam
  vibration clause.
- [[concrete-beam-longitudinal-shear-composite]] — the Cl 8.4 method Cl 9.8
  points to.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clauses 9.6–9.8.
