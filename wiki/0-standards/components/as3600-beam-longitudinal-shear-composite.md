---
title: Longitudinal shear at interfaces (composite and monolithic beams)
category: 0-standards
tags: [beams, composite, interface-shear, shear-friction]
standards: [AS 3600:2018 Cl 8.4]
status: draft
reviewed: 2026-09-12
---

# Longitudinal shear at interfaces

> Scope: AS 3600 Cl 8.4 — shear-friction design for interface shear planes,
> covering both composite beams (precast + cast-in-situ topping/flange) and
> monolithically-constructed beams (e.g. web-flange junctions of T-beams).

## Summary

`[code]` The interface is checked as a demand-vs-capacity ratio: design shear
stress `τ*` on the plane must not exceed a unit shear strength `τu` built from
a friction term, a cohesion term, and (where present) a permanent-load
clamping term.

## Detail

### Design shear stress (Cl 8.4.2)

`[code]` `τ* = V*/(z·bf)`, where `z` is the internal moment lever arm and
`bf` the shear-plane width. A load-sharing ratio `ψ` (own-words: the fraction
of the total compression, or of the total tension, force carried on the far
side of the shear plane from the extreme fibre) scales the effective demand
— worked out from the compression force distribution if the plane sits in
a compression region, or from the tensile-reinforcement force distribution
if it sits in a tension region.

### Shear stress capacity (Cl 8.4.3)

`[code]` `τu = kco·f'ct + μ·(Asf·fsy/(s·bf) + gp/bf)`, capped at the lesser
of `0.2·f'c` or 10 MPa (own-words: a cohesion term plus a friction term
acting on clamping stress from crossing reinforcement and any permanent
normal load, subject to an absolute strength ceiling). `μ` (friction
coefficient) and `kco` (cohesion coefficient) come from Table 8.4.3, with
four surface-preparation categories, in increasing
order of both coefficients: as-cast-against-formwork/equivalent finish;
trowelled/tamped/slip-formed with fines brought to the surface; deliberately
roughened (textured, exposed coarse aggregate, or spray-exposed); and
monolithic construction or mechanical shear keys (the highest values —
effectively no distinct "interface" at all).

![[as3600-table-8.4.3-shear-plane-surface-coefficients.png]]
*Table 8.4.3 — shear plane surface coefficients μ and kco, by surface
preparation category (AS 3600:2018).*

The clause explicitly warns
these coefficients don't apply where the plane sees high differential
shrinkage, temperature, direct tension, or fatigue effects — those need
separate assessment rather than a shear-friction check.

### Shear plane reinforcement and spacing (Cl 8.4.4)

`[code]` Reinforcement added specifically for interface shear must be
anchored to develop full strength at the plane; existing shear/torsional
reinforcement already crossing the plane counts toward this demand.
Maximum spacing: `smax = 3.5·tf`, where `tf` is the thickness of the topping
or flange being anchored — a fairly tight spacing limit compared to ordinary
beam shear reinforcement (Cl 8.3.2.2), reflecting how locally an interface
failure can initiate.

### Minimum component thickness (Cl 8.4.5)

`[code]` Average thickness of a component subject to interface shear ≥50 mm,
with a minimum local thickness ≥30 mm — a practical floor below which the
shear-friction model isn't considered reliable.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-beam-vibration-tbeams-slenderness]] — Cl 8.8 T-/L-beam flange
  effective width, whose flange-web junction is designed for interface shear
  under this clause.
- [[as3600-slab-strength-in-bending]] — Cl 9.8 applies this same clause to
  composite slabs.
- [[as3600-beam-shear-and-torsion-design]] — the member-level shear/torsion
  check this interface check supplements.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 8.4 (Table 8.4.3
  reproduced).
