---
title: AS/NZS 1170.2 freestanding walls, hoardings, free roofs, canopies, flags and circular shapes
category: 0-standards
tags: [as1170-2, wind, hoarding, free-roof, canopy, flag, appendix-b, appendix-d]
standards: [AS/NZS 1170.2:2021 App B.1-B.3.1, AS/NZS 1170.2:2021 App D]
status: draft
reviewed: 2026-10-03
---

# AS/NZS 1170.2 freestanding structures (Appendices B and D)

> Scope: App B.1-B.3.1 (general, hoardings and walls, free roofs) and App D
> (flags, discs, spheres). B.3.2 onward (cantilevered roofs, canopies, conical
> canopies, solar panels B.8-B.12) is not yet ingested except that Tables B.13-B.14
> were seen.

## Summary

`[code]` Appendix B gives C_shp for free roofs (including hyperbolic paraboloid
and conical canopies), canopies/awnings/carports adjacent to enclosed buildings,
cantilevered roofs, hoardings and freestanding walls, and ground- or
roof-mounted solar panels (B.1.1). The reference area for normal pressure is one
side of the structure; for friction it is all affected sides. Speed at the top
of the hoarding or wall (Note 2, B.2.1).

## Detail

### Factors (B.1)

`[code]` K_a per Cl 5.4.2 for freestanding roofs and canopies, otherwise 1.0.
K_ℓ (Table B.1) only for cladding and elements giving immediate support in free
roofs: 1.5 (area 0-1.0a² within 1.0a of an upwind roof edge or downwind of a ridge
≥ 10° pitch), 2.0 (area ≤ 0.25a² within 0.5a), 3.0 (upward net pressure on
≤ 0.25a² within 0.5a of an upwind corner, pitch < 10°); a = 20 % of the shortest
plan dimension. Net porosity factor K_p = 1 − (1 − δ)² — Eq B.1 (δ = solidity
ratio) for freestanding hoardings and walls; 1.0 elsewhere.

### Hoardings and freestanding walls (B.2)

`[code]` C_shp = C_p,n K_p — Eq B.2, applied to the gross area b × c. The resultant
acts at half height with horizontal eccentricity e (Table B.2). Wind normal
(θ = 0°): b/c 0.5-5 and c/h 0.2-1: C_p,n = 1.3 + 0.5[0.3 + log₁₀(b/c)](0.8 − c/h);
b/c > 5: 1.7 − 0.5c/h; c/h < 0.2: 1.4 + 0.3 log₁₀(b/c); e = 0. At 45°
(Tables B.2(B)-(C)): same expressions with e = 0.2b, and for b/c > 5 maximum 3.0
within 0-2c of the windward free end (c/h ≤ 0.7) or 2.4 within 0-2h (c/h > 0.7),
falling to 0.75 or 0.6 beyond 4c or 4h. Wind parallel (θ = 90°, Table B.2(D)):
±1.2, ±0.6, ±0.3 (c/h ≤ 0.7) and ±1.0, ±0.25, ±0.25 (c/h > 0.7) by distance zone.
Friction: C_f 0.04 / 0.02 / 0.01 as for enclosed buildings, both surfaces summed
(Table B.3).

### Free roofs (B.3.1)

`[code]` C_shp = C_p,n K_a K_ℓ — Eq B.3(1), with C_p,n (positive = net downward) for
windward half C_p,w and leeward half C_p,ℓ from Tables B.4-B.7 for monoslope,
pitched, troughed and hypar free roofs, 0.25 ≤ h/d ≤ 1 (B.4(B): 0.05 ≤ h/d < 0.25).
"Empty under" means stored goods block < 50 % of the cross-section; "blocked
under" means > 75 %. All combinations of C_p,w and C_p,ℓ shall be taken into
account; interpolate only between values of the same sign. Example (Table B.4(A),
θ = 0°, α = 15°, empty under): C_p,w −1.0, C_p,ℓ −0.6, 0.0.

### Flags and circular shapes (App D)

`[code]` Fixed flag: treat as elevated hoarding. Free flag:
C_shp = 0.05 + 0.7 (m_f/(ρ_air c)) (A_ref/c²)^−1.25 but ≤ 0.76 — Eq D.2.
Table D.1 (A_ref = projected area normal to wind): circular disc 1.3; hemispherical
bowl cup to wind 1.4; bowl facing away 0.4; flat-to-wind hemisphere 1.2;
sphere 0.5 for bV_des,θ < 7 m²/s, 0.2 for ≥ 7 m²/s. Speed at mid-height (D.1).

`[derived]` For open-framed mining structures (conveyor galleries, pipe racks)
App C ([[as1170-2-exposed-members-frames-and-lattice-towers]]) is the more usual
route; App B applies to solid hoardings, screens and walls such as dust or wind
fences.

## Worked reference

None yet.

## Contradictions

None recorded.

## Figures and tables

`[code]` Page crops from the source scan (AS/NZS 1170.2:2021), stored in `0-standards/assets`. They are the authoritative reproduction of the tabulated values; prose transcriptions above are `[derived]` and must be checked against these images.

**Table B.1 — local net pressure factors open structures**

![[as1170-2-table-B.1-local-net-pressure-factors-open-structures.png]]

**Figure B.1 — freestanding hoardings and walls**

![[as1170-2-fig-B.1-freestanding-hoardings-and-walls.png]]

**Table B.2A — hoarding net pressure theta 0**

![[as1170-2-table-B.2A-hoarding-net-pressure-theta-0.png]]

**Table B.2B — hoarding net pressure theta 45 high ratio**

![[as1170-2-table-B.2B-hoarding-net-pressure-theta-45-high-ratio.png]]

**Table B.2C — hoarding net pressure theta 45 distance from free end**

![[as1170-2-table-B.2C-hoarding-net-pressure-theta-45-distance-from-free-end.png]]

**Table B.2 — D hoarding net pressure theta 90**

![[as1170-2-table-B.2D-hoarding-net-pressure-theta-90.png]]

**Table B.3 — frictional drag coefficient cf**

![[as1170-2-table-B.3-frictional-drag-coefficient-cf.png]]

**Table B.4A — monoslope free roofs h d 0.25 to 1**

![[as1170-2-table-B.4A-monoslope-free-roofs-h-d-0.25-to-1.png]]

**Table B.4B and Figure B.2 — monoslope free roofs low h d**

![[as1170-2-table-B.4B-and-fig-B.2-monoslope-free-roofs-low-h-d.png]]

**Table B.5 — pitched free roofs**

![[as1170-2-table-B.5-pitched-free-roofs.png]]

**Figure B.3 — pitched free roofs**

![[as1170-2-fig-B.3-pitched-free-roofs.png]]

**Table B.6 and Figure B.4 — troughed free roofs**

![[as1170-2-table-B.6-and-fig-B.4-troughed-free-roofs.png]]

**Table B.7 — hypar free roofs**

![[as1170-2-table-B.7-hypar-free-roofs.png]]

**Figure B.5 — hyperbolic paraboloid roofs**

![[as1170-2-fig-B.5-hyperbolic-paraboloid-roofs.png]]

**Table B.8 — conical canopies**

![[as1170-2-table-B.8-conical-canopies.png]]

**Figure B.6 — conical canopies**

![[as1170-2-fig-B.6-conical-canopies.png]]

**Table B.9 — attached canopies theta 0**

![[as1170-2-table-B.9-attached-canopies-theta-0.png]]

**Figure B.7 — attached canopies and awnings**

![[as1170-2-fig-B.7-attached-canopies-and-awnings.png]]

**Table B.10 — partially enclosed carports**

![[as1170-2-table-B.10-partially-enclosed-carports.png]]

**Table B.11 — isolated cantilever roofs**

![[as1170-2-table-B.11-isolated-cantilever-roofs.png]]

**Figure B.8 — cantilevered roof zones**

![[as1170-2-fig-B.8-cantilevered-roof-zones.png]]

**Figure B.9 — solar panel parallel to roof plane**

![[as1170-2-fig-B.9-solar-panel-parallel-to-roof-plane.png]]

**Figure B.10 — roof zones for panel array**

![[as1170-2-fig-B.10-roof-zones-for-panel-array.png]]

**Table B.12 — solar panels parallel to roof cshp**

![[as1170-2-table-B.12-solar-panels-parallel-to-roof-cshp.png]]

**Figure B.11 — solar panel arrays ground mounted**

![[as1170-2-fig-B.11-solar-panel-arrays-ground-mounted.png]]

**Table B.13 — solar panel array theta 0**

![[as1170-2-table-B.13-solar-panel-array-theta-0.png]]

**Table B.14 — solar panel array theta 180**

![[as1170-2-table-B.14-solar-panel-array-theta-180.png]]

**Figure D.1 — reference area for flags**

![[as1170-2-fig-D.1-reference-area-for-flags.png]]

**Table D.1 — circular shapes aerodynamic shape factor**

![[as1170-2-table-D.1-circular-shapes-aerodynamic-shape-factor.png]]

## Related

- [[as-1170.2-2021-wind-actions]] — source register
- [[as1170-2-enclosed-building-pressure-coefficients]]
- [[as1170-2-wind-design-procedure-and-pressures]]

## Sources

- `raw/0-standards/AS 1170-2-2021-reprint.pdf` — printed pp. 77-82 and 91, pp. 106-107.
