---
title: AS/NZS 1170.2 aerodynamic shape factor for enclosed rectangular buildings
category: 0-standards
tags: [as1170-2, wind, cpe, cpi, local-pressure, roofs, walls, enclosed-buildings]
standards: [AS/NZS 1170.2:2021 Cl 5.1-5.5, AS/NZS 1170.2:2021 App A.1-A.4]
status: draft
reviewed: 2026-10-03
---

# AS/NZS 1170.2 enclosed rectangular buildings — C_shp

> Scope: Section 5 (shape factors for enclosed rectangular buildings) plus
> App A.1-A.4 (multi-span, curved and mansard roofs). Tables are transcribed
> from scanned images; check against the printed standard before use. Silos
> and tanks: [[as1170-2-bins-silos-and-tanks-wind-pressures]].

## Summary

`[code]` C_shp for a surface gives the pressure on that surface; the sign of
C_shp indicates direction (positive towards the surface, negative = suction,
Cl 5.1, Fig 5.1). Design actions are the sum of internal and external pressure
effects (Cl 5.1). Rectangular buildings include buildings generally made of
rectangular shapes in plan.

## Detail

### Evaluation (Cl 5.2)

`[code]` Enclosed buildings:

- C_shp = C_p,i K_c,i K_v — internal pressure, Eq 5.2(1)
- C_shp = C_p,e K_a K_c,e K_ℓ K_p — external pressure, Eq 5.2(2)
- C_shp = C_f K_a K_c,e — frictional drag, Eq 5.2(3)

Circular bins/silos/tanks use App A.5; freestanding walls, hoardings, canopies
and roofs use App B (Eq 5.2(4)-(5)); exposed members and lattice towers App C;
flags and circular shapes App D.

### Internal pressure C_p,i (Cl 5.3)

`[code]` Speed at average roof height h, except windward-wall leakage or openings
on buildings over 25 m, where speed at the opening is used (Cl 5.3.1.1).
Table 5.1(A) (no opening > 0.5 % of the surface area, impermeable roof):

| Condition | C_pi |
|---|---|
| One wall permeable, others impermeable — windward permeable | C_p,e of windward wall |
| — windward impermeable | −0.3 |
| Two or three walls permeable — windward permeable | −0.1, 0.2 |
| — windward impermeable | −0.3 |
| All walls permeable | −0.3 or 0.0 (more severe for combined actions) |
| Effectively sealed, non-opening windows | −0.2 or 0.0 (more severe) |

A surface is *impermeable* below 0.1 % open area and *permeable* between 0.1 %
and 0.5 %; above 0.5 % it has large openings and Table 5.1(B) applies.
Table 5.1(B) (ratio of openings on one surface to the open area of other
surfaces): ≤ 0.5 → −0.3, 0.0; 1 → −0.1, 0.2 for largest opening on windward
wall, else −0.3, 0.0; 2 → 0.7 K_a K_ℓ C_p,e on windward wall, K_a K_ℓ C_p,e
elsewhere; 3 → 0.85 K_a K_ℓ C_p,e windward; ≥ 6 → K_a K_ℓ C_p,e.

Openings: doors and windows normally closed count as openings unless shown to
resist the pressures (Cl 5.3.2.2). In Regions C and D below 25 m, the element
area or the debris-impact opening area counts if greater (Cl 5.3.2.3); the
opening-area ratio is not taken below 2 unless an exception (a)-(c) of
Cl 5.3.1.3 applies, and ultimate limit states use Table 5.1(B) only.
Internal walls and ceilings forming an effective seal: minimum net pressure
coefficient 0.4; not forming a permanent seal: 0.3 (Cl 5.3.3).

Open area/volume factor (Cl 5.3.4): K_v = 1.01 + 0.15 log₁₀(100 A^1.5/Vol) for
0.09 ≤ 100A^1.5/Vol ≤ 3 — Eq 5.3(1); 0.85 below 0.09; 1.085 above 3; applies
when the largest opening is on a wall and exceeds the other open area by a
factor of six or more; otherwise K_v = 1.0.

### External pressure C_p,e (Cl 5.4.1)

`[code]` Parameters in Figure 5.2; speed at z = h for leeward walls, side walls
and roofs. Where two C_p,e values are listed, design the roof for both and
consider alternative combinations with internal pressure. Underside of elevated
buildings: 0.8 and −0.6 (Cl 5.4.1).

- Windward wall (Table 5.2(A)): h > 25 m → 0.8 (wind speed varying with
  height); h ≤ 25 m on ground → 0.8 (varying speed) or 0.7 (speed at z = h);
  elevated → 0.8 (speed at h).
- Leeward wall (Table 5.2(B)), θ = 0 hip/gable: α < 10°: d/b ≤ 1 → −0.5,
  2 → −0.3, ≥ 4 → −0.2; α = 10°, 15°, 20° → −0.3, −0.3, −0.4; α ≥ 25°:
  d/b ≤ 0.1 → −0.75, ≥ 0.3 → −0.5; θ = 90° gable: ≤ 1 → −0.5, 2 → −0.3,
  ≥ 4 → −0.2.
- Side walls (Table 5.2(C)): 0-1h → −0.65; 1h-2h → −0.5; 2h-3h → −0.3; > 3h → −0.2.
- Roofs: Tables 5.3(A) (α < 10° and monoslope: e.g. 0-0.5h from windward edge
  −0.9, −0.4 for h/d ≤ 0.5), 5.3(B) (upwind slope α ≥ 10°) and 5.3(C)
  (downwind slope and hip crosswind slope). Interpolate only between values of
  the same sign.

### Area reduction factor K_a (Cl 5.4.2, Table 5.4)

`[code]` Roofs and side walls: 1.0 for tributary area A ≤ 10 m², 0.9 at 25 m²,
0.8 for A ≥ 100 m². Windward walls (h < 25 m): 1.0, 0.95, 0.9. Leeward walls
(h < 25 m): 1.0, 1.0, 0.95. K_a = 1.0 otherwise.

### Action combination factor K_c (Cl 5.4.3, Table 5.5)

`[code]` For effects from several surfaces acting together: K_c,e and K_c,i may
be 0.9 for two contributing surfaces and 0.8 for three or more; an internal
surface is not effective if |C_pi| < 0.4. The product K_a K_c,e shall not be
less than 0.8. Table 5.5 lists example cases (e.g. four effective surfaces:
0.8 / 0.8; one effective surface alone: 1.0 / 1.0).

### Local pressure factor K_ℓ (Cl 5.4.4, Tables 5.6-5.7, Fig 5.3)

`[code]` K_ℓ = 1.0 except for cladding, its fixings and members directly
supporting it, where the larger of 1.0 and the Table 5.6 value applies. Negative
cases are alternatives, not simultaneous. Dimension a is the minimum of 0.2b,
0.2d or h for walls; for roofs the minimum of 0.2b or 0.2d (if h/b or h/d ≥ 0.2),
or 2h otherwise. Selected values: windward wall WA1 (A ≤ 0.25a²) 1.5; corner
roof zones RC1/RC2 3.0; edge zones RA1/RA3 1.5, RA2/RA4 2.0; side walls SA1-SA5
1.5-3.0. The product K_ℓ C_p,e is limited to −3.0. Parapet reduction K_r
(Table 5.7): 0.5 to 1.0 by parapet height.

### Permeable cladding K_p (Cl 5.4.5, Table 5.8)

`[code]` K_p = 1.0 except for permeable cladding with open-area ratio between 0.1 %
and 1 %, where negative-pressure values 0.9, 0.8, 0.7, 0.8 may apply along 0-0.2d_a,
0.2-0.4d_a, 0.4-0.8d_a, 0.8-1.0d_a from the windward edge.

### Frictional drag (Cl 5.5, Table 5.9)

`[code]` Calculate friction on roofs and side walls only where d/h or d/b > 4.
C_f = 0.04 (ribs across the wind), 0.02 (corrugations across the wind), 0.01
(smooth or parallel ribs) for x ≥ the lesser of 4h and 4b from the windward edge;
0 closer. Area for h ≤ b: (b + 2h)(d − 4h); for h > b: (b + 2h)(d − 4b).

### Appendix A.1-A.4

`[code]` Multi-span pitched (Table A.1) and saw-tooth (Table A.2) roofs, curved
roofs (Table A.3, with breadth/span factor (b/d)^0.25 limited to +0.8, −1.7) and
mansard roofs (A.4) have their own C_p,e. Use wind speed at average roof height.

## Worked reference

None yet.

## Contradictions

None recorded.

## Figures and tables

`[code]` Page crops from the source scan (AS/NZS 1170.2:2021), stored in `0-standards/assets`. They are the authoritative reproduction of the tabulated values; prose transcriptions above are `[derived]` and must be checked against these images.

**Figure 5.1A — sign conventions for cshp enclosed buildings**

![[as1170-2-fig-5.1A-sign-conventions-for-cshp-enclosed-buildings.png]]

**Figure 5.1B — sign conventions for cshp walls and roofs**

![[as1170-2-fig-5.1B-sign-conventions-for-cshp-walls-and-roofs.png]]

**Table 5.1A — internal pressure coefficients no large openings**

![[as1170-2-table-5.1A-internal-pressure-coefficients-no-large-openings.png]]

**Table 5.1B — internal pressure coefficients large openings**

![[as1170-2-table-5.1B-internal-pressure-coefficients-large-openings.png]]

**Figure 5.2 — parameters for rectangular enclosed buildings**

![[as1170-2-fig-5.2-parameters-for-rectangular-enclosed-buildings.png]]

**Table 5.2A — walls windward cpe**

![[as1170-2-table-5.2A-walls-windward-cpe.png]]

**Table 5.2B — walls leeward cpe**

![[as1170-2-table-5.2B-walls-leeward-cpe.png]]

**Table 5.2C — walls side cpe**

![[as1170-2-table-5.2C-walls-side-cpe.png]]

**Table 5.3A — roofs upwind downwind low pitch cpe**

![[as1170-2-table-5.3A-roofs-upwind-downwind-low-pitch-cpe.png]]

**Table 5.3B — roofs upwind slope cpe**

![[as1170-2-table-5.3B-roofs-upwind-slope-cpe.png]]

**Table 5.3C — roofs downwind slope and hip cpe**

![[as1170-2-table-5.3C-roofs-downwind-slope-and-hip-cpe.png]]

**Table 5.4 — area reduction factor ka**

![[as1170-2-table-5.4-area-reduction-factor-ka.png]]

**Table 5.5 — action combination factors a c**

![[as1170-2-table-5.5-action-combination-factors-a-c.png]]

**Table 5.5 — action combination factors d h continued**

![[as1170-2-table-5.5-action-combination-factors-d-h-continued.png]]

**Table 5.6 — local pressure factor kl**

![[as1170-2-table-5.6-local-pressure-factor-kl.png]]

**Table 5.7 — parapet reduction factor h le 25m**

![[as1170-2-table-5.7-parapet-reduction-factor-h-le-25m.png]]

**Table 5.7 — parapet reduction factor h gt 25m continued**

![[as1170-2-table-5.7-parapet-reduction-factor-h-gt-25m-continued.png]]

**Figure 5.3 — local pressure factor zones**

![[as1170-2-fig-5.3-local-pressure-factor-zones.png]]

**Table 5.8 — permeable cladding reduction factor kp**

![[as1170-2-table-5.8-permeable-cladding-reduction-factor-kp.png]]

**Figure 5.4 — notation for permeable surfaces**

![[as1170-2-fig-5.4-notation-for-permeable-surfaces.png]]

**Table 5.9 — frictional drag coefficient cf**

![[as1170-2-table-5.9-frictional-drag-coefficient-cf.png]]

**Table A.1 — multi span pitched roofs with fig A.1**

![[as1170-2-table-A.1-multi-span-pitched-roofs-with-fig-A.1.png]]

**Table A.2 — multi span saw tooth roofs with fig A.2**

![[as1170-2-table-A.2-multi-span-saw-tooth-roofs-with-fig-A.2.png]]

**Table A.3 — curved roofs with fig A.3**

![[as1170-2-table-A.3-curved-roofs-with-fig-A.3.png]]

**Figure A.4 — mansard roofs**

![[as1170-2-fig-A.4-mansard-roofs.png]]

## Related

- [[as-1170.2-2021-wind-actions]] — source register
- [[as1170-2-wind-design-procedure-and-pressures]]
- [[as1170-2-regional-wind-speeds-and-site-multipliers]]
- [[as1170-2-bins-silos-and-tanks-wind-pressures]]

## Sources

- `raw/0-standards/AS 1170-2-2021-reprint.pdf` — printed pp. 40-57 and 70-73.
