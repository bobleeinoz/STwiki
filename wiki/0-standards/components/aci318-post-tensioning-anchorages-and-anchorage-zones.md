---
title: ACI 318M-19 post-tensioning anchorages, couplers and anchorage zones
category: 0-standards
tags: [aci, prestressed-concrete, post-tensioning, anchorage-zone, general-zone, local-zone]
standards: [ACI 318M-19 Cl 25.8, ACI 318M-19 Cl 25.9]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 post-tensioning anchorages, couplers and anchorage zones

> Scope: ACI 318M-19 Cl 25.8–25.9. **ACI 318M-19 page, kept separate from the AS 3600:2018
> pages** (see [[aci-318m-19-building-code-concrete]]). Prestressing steel properties are
> in [[aci318-reinforcement-properties-durability-and-embedments]]; strut-and-tie design
> in [[aci318-strut-and-tie-method]].

## Summary

`[code]` Anchorage devices and couplers must develop the tendon capacity (Cl 25.8). The
anchorage region is split into a **local zone** (concrete prism immediately around the
device) and a **general zone** (where the concentrated force spreads to a uniform section
distribution), each with its own design rules (Cl 25.9.1.1).

## Detail

### Anchorages and couplers (Cl 25.8)

`[code]` Anchorages and couplers develop ≥ **95 % of `f_pu`** when tested unbonded, without
exceeding anticipated set (Cl 25.8.1). For bonded tendons they are placed so that **100 % of
`f_pu`** is developed at critical sections after bonding (Cl 25.8.2). In unbonded construction
under repeated loading, fatigue in anchorages and couplers is considered (Cl 25.8.3). Couplers
are located as approved by the licensed design professional and housed with room for movement
(Cl 25.8.4).

### Anchorage zones — general and required strength (Cl 25.9.1–25.9.2)

`[code]` Local zone is designed per Cl 25.9.3 and general zone per Cl 25.9.4; concrete strength
at stressing and the stressing sequence are specified per Cl 26.10 (Cl 25.9.1.2–25.9.1.5).
Factored prestressing force at the device `P_pu` exceeds the least of `1.2(0.94f_py)A_ps`,
`1.2(0.80f_pu)A_ps`, and 1.2 × the supplier's maximum jacking force, with 1.2 the load factor of
Cl 5.3.12 (Cl 25.9.2.1).

![[aci318-figure-R25.9.1.1a-local-general-zones.png]]
*Fig. R25.9.1.1a — local and general zones at a member end; the general zone extends about `h`
ahead of the device (ACI 318M-19 commentary).*

![[aci318-figure-R25.9.1.1b-zones-away-from-end.png]]
*Fig. R25.9.1.1b — zones for an anchorage located away from the member end: general zone covers
regions behind and ahead of the device (ACI 318M-19 commentary).*

### Local zone (Cl 25.9.3)

`[code]` One of: (a) monostrand or single bar ≤ 16 mm diameter devices meeting ACI 423.7 bearing
and local-zone rules; (b) basic multistrand devices meeting AASHTO LRFD Bridge Design
Specifications Art. 5.8.4.4.2, using Cl 5.3.12 load factors and φ from Cl 21.2.1; (c) special
anchorage devices passing the AASHTO LRFD tests of Art. 5.8.4.4.3 / Construction Specifications
Art. 10.3.2.3 (Cl 25.9.3.1). Special devices need supplementary skin reinforcement similar in
configuration and at least equal in volumetric ratio to that used in qualification tests
(Cl 25.9.3.2).

### General zone (Cl 25.9.4)

`[code]` Extent equals the largest cross-section dimension; for slab-edge anchorages the depth is
the tendon spacing (Cl 25.9.4.1); for devices away from the end, it includes the disturbed
regions behind and ahead (Cl 25.9.4.2).

![[aci318-figure-R25.9.4-tensile-stress-zones.png]]
*Fig. R25.9.4 — bursting, spalling and longitudinal edge-tension stresses in the general zone
(ACI 318M-19 commentary).*

![[aci318-figure-R25.9.4.1-general-zone-slab.png]]
*Fig. R25.9.4.1 — general-zone dimensions in a post-tensioned slab: depth `s` equals the tendon
spacing along the edge (ACI 318M-19 commentary).*

**Analysis (Cl 25.9.4.3).** `[code]` Permitted methods: strut-and-tie (Chapter 23), linear stress
analysis including FEA, or the AASHTO LRFD Art. 5.8.4.5 simplified equations; other methods need
strength predictions in substantial agreement with comprehensive tests (Cl 25.9.4.3.1). The
simplified equations are **not** used when any of the following apply (Cl 25.9.4.3.2): nonrectangular
cross section; force-flow discontinuities in or near the zone; edge distance < 1.5× the device lateral
dimension; multiple devices other than one closely spaced group; tendon centroid outside the kern;
tendon inclination below −5° or above +20° to the member axis. Three-dimensional effects are
analysed in 3D or by summing two orthogonal planes (Cl 25.9.4.3.3).

![[aci318-figure-R25.9.4.3.1-general-zone-terms.png]]
*Fig. R25.9.4.3.1 — terms for the bursting force `T_burst` and its position `d_burst` (ACI 318M-19
commentary).*

![[aci318-figure-R25.9.4.4.2-cross-section-change.png]]
*Fig. R25.9.4.4.2 — an abrupt section change roughly doubles `T_burst` from about `0.25P_pu`
(rectangular) to about `0.50P_pu` (flanged section with end diaphragm) (ACI 318M-19 commentary).*

**Reinforcement (Cl 25.9.4.4).** `[code]` Concrete tensile strength is neglected (Cl 25.9.4.4.1).
Reinforcement resists bursting, spalling and longitudinal edge tension, considering abrupt section
changes and the stressing sequence (Cl 25.9.4.4.2). For devices away from the member end, bonded
steel transfers ≥ `0.35P_pu` into the concrete behind the anchor, placed symmetrically and fully
developed both sides (Cl 25.9.4.4.3). Curved tendons need bonded steel for radial and splitting
forces, except monostrand tendons in slabs or where analysis shows it is unnecessary
(Cl 25.9.4.4.4). Reinforcement of nominal tensile strength equal to **2 %** of the factored
prestressing force is provided in orthogonal directions parallel to the loaded face to limit
spalling, with the same exceptions (Cl 25.9.4.4.5).

*Monostrand devices (≤ 12.7 mm strand, normalweight slabs), Cl 25.9.4.4.6.* `[code]` Unless detailed
analysis shows otherwise: (a) two horizontal bars ≥ No. 13 within the local zone, parallel to the slab
edge, centres ≤ 100 mm ahead of the bearing face, extending ≥ 150 mm each side of the device;
(b) devices at ≤ 300 mm spacing form a group, and each group of six or more has ≥ `n + 1` hairpin
bars or closed stirrups ≥ No. 10 (`n` = number of devices), one between adjacent devices and one at
each end, with the vertical leg `3h/8` to `h/2` ahead of the bearing face, detailed per
Cl 25.7.1.1–25.7.1.2.

![[aci318-figure-R25.9.4.4.6-monostrand-slab-anchorage.png]]
*Fig. R25.9.4.4.6 — anchorage zone reinforcement for groups of monostrand tendons in slabs
(ACI 318M-19 commentary).*

**Limiting stresses (Cl 25.9.4.5).**

![[aci318-table-25.9.4.5.1-max-design-tensile-stress-general-zone.png]]
*Table 25.9.4.5.1 — maximum design tensile stress in reinforcement at nominal strength:
nonprestressed `f_y`; bonded prestressed `f_py`; unbonded prestressed `f_se + 70` (ACI 318M-19).*

`[code]` Compressive stress in concrete at nominal strength ≤ `0.7λf'ci`, λ per Cl 19.2.4
(Cl 25.9.4.5.2). See [[aci318-concrete-design-properties-and-durability]].

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[aci-318m-19-building-code-concrete]] — source register.
- [[aci318-reinforcement-spacing-hooks-and-development]], [[aci318-splices-bundled-bars-and-transverse-reinforcement]]
  — rest of Chapter 25.
- [[aci318-strut-and-tie-method]] — permitted general-zone analysis method.
- [[aci318-reinforcement-properties-durability-and-embedments]] — `f_pu`, `f_py`, `f_se`.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 25 Cl 25.8–25.9 (printed pp. 504–513).
