---
title: AS/NZS 1170.2 wind design procedure — site speed, design speed, pressures and forces
category: 0-standards
tags: [as1170-2, wind, loads, design-wind-speed, fatigue, debris]
standards: [AS/NZS 1170.2:2021 Cl 1.1-1.2, AS/NZS 1170.2:2021 Cl 2.1-2.5]
status: draft
reviewed: 2026-10-03
---

# AS/NZS 1170.2 wind design procedure

> Scope: Sections 1 and 2 of AS/NZS 1170.2:2021 — the four-step procedure from
> site wind speed to wind actions. Multipliers are on
> [[as1170-2-regional-wind-speeds-and-site-multipliers]]; shape factors on
> [[as1170-2-enclosed-building-pressure-coefficients]] and the other concept pages
> linked from [[as-1170.2-2021-wind-actions]].

## Summary

`[code]` The procedure is: (a) site wind speeds, (b) design wind speed from the
site speeds, (c) design wind pressures and distributed forces, (d) wind actions
(Cl 2.1). Wind actions W_u and W_s feed AS/NZS 1170.0 (Cl 2.5.1).

## Detail

### Scope limits (Cl 1.1)

`[code]` Covers buildings and towers ≤ 200 m, roof spans < 100 m, offshore
structures within 30 km of the coast. Excluded: offshore > 30 km, bridges,
wind-farm and power-transmission structures. Tornado wind is not covered.
Specialist techniques including wind-tunnel testing are required for
structures outside (a) and (b) (Notes 3, Cl 1.1). If a tall building has a
first-mode frequency below 1 Hz, Section 6 requires dynamic analysis (Note 2).

### Site wind speed (Cl 2.2)

`[code]` For the 8 cardinal directions β at reference height z:

V_sit,β = V_R · M_c · M_d · (M_z,cat · M_s · M_t)  — Eq 2.2

Generally the wind speed is taken at the average roof height h; in some cases
the reference height varies with the structure (Cl 2.2).

### Reference height (Cl 2.2, Fig 2.1)

`[code]` Ground level is natural ground (excluding excavations) at the centroid
of the roof footprint. With upper and lower roofs, h is the average height of
the upper roof (Figure 2.1 text).

### Design wind speed (Cl 2.3)

`[code]` V_des,θ = the maximum cardinal-direction V_sit,β within ±45° of the
orthogonal direction θ, linearly interpolated between cardinal points
(Figs 2.2, 2.3). For walls, hoardings and lattice towers (45° incidence) the
sector is ±22.5° about the 45° direction. For ultimate limit states V_des,θ
shall not be less than **30 m/s**.

### Design pressure and frictional drag (Cl 2.4)

`[code]`

- p = (0.5 ρ_air) [V_des,θ]² C_shp C_dyn — Eq 2.4(1); ρ_air = 1.2 kg/m³.
  Positive pressure acts towards the surface, negative is suction.
- f = (0.5 ρ_air) [V_des,θ]² C_shp — Eq 2.4(2), frictional drag per unit area.

C_dyn is 1.0 except for dynamically wind-sensitive structures
([[as1170-2-dynamic-response-and-crosswind]]).

### Wind actions (Cl 2.5)

`[code]`

- Directions: at least four orthogonal directions aligned to the structure
  (Cl 2.5.2).
- F = Σ(p_z A_z) — Eq 2.5(1), vector sum of pressure forces. For enclosed
  buildings, internal pressure acts simultaneously with external pressure
  including local factors K_ℓ. Tall structures divided into sectors for
  wind speed varying with height (windward walls, Table 5.2(A), lattice
  towers, Cl C.4.1) use sector sizes per Cl 4.2.2 (Cl 2.5.3.1).
- F = Σ(f_z A_z) — Eq 2.5(2) for frictional drag (Cl 2.5.3.2).
- F = (0.5 ρ_air) [V_des,θ]² C_shp C_dyn A_z — Eq 2.5(3) for force-coefficient
  structures (Appendices C and D) (Cl 2.5.3.3).
- Complete structures: sum the effects of external pressures on all surfaces;
  for rectangular enclosed buildings with h > 70 m apply torsion with eccentricity
  0.2b to the along-wind loading (Cl 2.5.4). For d/b > 1.5 torsion is mainly
  crosswind and specialist advice is advised (Note).

### Stress exceedances for fatigue (Cl 2.5.5)

`[code]` Number of times N_g a stress ratio σ/σ_max is exceeded in a 20-100
year life: σ/σ_max = 0.7 (log N_g)² − 17.4 log N_g + 100 — Eq 2.5(4),
Fig 2.4. It includes quasi-static gust cycles and resonant cycles; it does not
cover vortex-shedding crosswind fatigue (Note 4) nor low-cycle fatigue of
cladding in Regions C and D (Cl 2.5.6, AS 4040.3 and NCC).

### Windborne debris impact (Cl 2.5.8)

`[code]` Test debris: a 4 kg timber member (≥ 600 kg/m³, 100 × 50 mm) end-on at
0.4 V_R normal to walls, 0.4 V_R × sin(roof slope) on roofs steeper than 15°,
0.1 V_R on roofs ≤ 15°; and an 8 mm steel ball (~2 g) at 0.4 V_R on walls and
roofs steeper than 35°, 0.3 V_R on roofs ≤ 35°. No test method or acceptance
criteria are given (Note 5).

## Worked reference

None yet.

## Contradictions

None recorded.

## Figures and tables

`[code]` Page crops from the source scan (AS/NZS 1170.2:2021), stored in `0-standards/assets`. They are the authoritative reproduction of the tabulated values; prose transcriptions above are `[derived]` and must be checked against these images.

**Figure 2.1 — reference height of structures**

![[as1170-2-fig-2.1-reference-height-of-structures.png]]

**Figure 2.2 — wind directions and building orthogonal axes**

![[as1170-2-fig-2.2-wind-directions-and-building-orthogonal-axes.png]]

**Figure 2.3 — vsit beta to vdes theta conversion**

![[as1170-2-fig-2.3-vsit-beta-to-vdes-theta-conversion.png]]

**Figure 2.4 — wind load cycles vs stress ratio**

![[as1170-2-fig-2.4-wind-load-cycles-vs-stress-ratio.png]]

## Related

- [[as-1170.2-2021-wind-actions]] — source register
- [[as1170-2-regional-wind-speeds-and-site-multipliers]]
- [[as1170-2-enclosed-building-pressure-coefficients]]
- [[as1170-2-dynamic-response-and-crosswind]]
- [[as1170-2-bins-silos-and-tanks-wind-pressures]]
- [[as3774-environmental-and-accidental-loads]] — AS 3774 wind clause that defers to this standard

## Sources

- `raw/0-standards/AS 1170-2-2021-reprint.pdf` — printed pp. 1-23, AS/NZS 1170.2:2021.
