---
title: AS/NZS 1170.2 regional wind speeds and site exposure multipliers
category: 0-standards
tags: [as1170-2, wind, regional-wind-speed, terrain, shielding, topography]
standards: [AS/NZS 1170.2:2021 Cl 3.1-3.4, AS/NZS 1170.2:2021 Cl 4.1-4.4]
status: draft
reviewed: 2026-10-03
---

# AS/NZS 1170.2 regional wind speeds and site multipliers

> Scope: Sections 3 and 4 — V_R, M_c, M_d, M_z,cat, M_s, M_t. Values are
> transcribed from scanned tables; re-check against the printed standard before
> use in a calculation.

## Summary

`[code]` Site wind speed V_sit,β = V_R M_c M_d (M_z,cat M_s M_t)
([[as1170-2-wind-design-procedure-and-pressures]]). Regional speeds are peak
gusts (≈ 0.2 s moving average), rounded to 1 m/s (Table 3.1 Note 1, Cl 3.2).
Importance level and annual probability of exceedance come from the NCC or
AS/NZS 1170.0 (Table 3.1(A) Note 3).

## Detail

### Regional wind speed V_R (Cl 3.2, Table 3.1(A) Australia)

`[code]` Region columns: A (0 to 5), B1 and B2 share a column, C (maximum),
D (maximum). Selected rows (m/s):

| R (years) | A | B1, B2 | C | D |
|---|---|---|---|---|
| V_1 | 30 | 26 | 23 | 23 |
| V_5 | 32 | 28 | 33 | 35 |
| V_20 | 37 | 38 | 45 | 51 |
| V_50 | 39 | 44 | 52 | 60 |
| V_100 | 41 | 48 | 56 | 66 |
| V_200 | 43 | 52 | 61 | 72 |
| V_500 | 45 | 57 | 66 | 80 |
| V_1000 | 46 | 60 | 70 | 85 |
| V_2000 | 48 | 63 | 73 | 90 |
| V_5000 | 50 | 67 | 78 | 95 |
| V_10000 | 51 | 69 | 81 | 99 |

For R ≥ 5 years: V_R = 67 − 41 R^−0.1 (A); 106 − 92 R^−0.1 (B1, B2);
122 − 104 R^−0.1 (C); 156 − 142 R^−0.1 (D). V_1 is not given by the formula.
In Regions C and D only the maximum is tabulated; lower values apply with
distance from the smoothed coast, by linear interpolation between C and B2 (for
C) and between D and C (for D) (Cl 3.2, Table 3.1(A) Note 4). New Zealand has
its own Table 3.1(B).

### Wind direction multiplier M_d (Cl 3.3, Table 3.2(A))

`[code]` Cardinal-direction values, Australia (columns A0, A1, A2, A3, A4, A5,
B1, B2/C/D):

| Dir | A0 | A1 | A2 | A3 | A4 | A5 | B1 | B2,C,D |
|---|---|---|---|---|---|---|---|---|
| N | 0.90 | 0.90 | 0.85 | 0.90 | 0.85 | 0.95 | 0.75 | 0.90 |
| NE | 0.85 | 0.85 | 0.75 | 0.75 | 0.75 | 0.80 | 0.75 | 0.90 |
| E | 0.85 | 0.85 | 0.85 | 0.75 | 0.75 | 0.75 | 0.85 | 0.90 |
| SE | 0.90 | 0.80 | 0.95 | 0.90 | 0.80 | 0.80 | 0.90 | 0.90 |
| S | 0.90 | 0.80 | 0.95 | 0.90 | 0.80 | 0.80 | 0.95 | 0.90 |
| SW | 0.95 | 0.95 | 0.95 | 0.95 | 0.90 | 0.95 | 0.95 | 0.90 |
| W | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 1.00 | 0.95 | 0.90 |
| NW | 0.95 | 0.95 | 0.95 | 0.95 | 1.00 | 0.95 | 0.90 | 0.90 |

M_d shall be 1.0 for circular or polygonal chimneys, tanks and poles, and for
cladding and its immediate supporting structure in Regions B2, C and D
(Cl 3.3(a),(b)).

### Climate change multiplier M_c (Cl 3.4, Table 3.3)

`[code]` 1.0 for Regions A (0 to 5) and B1; 1.05 for B2, C and D; 1.0 for NZ 1-4.

### Terrain/height multiplier M_z,cat (Cl 4.2, Table 4.1)

`[code]` Terrain categories TC1 (very exposed open, water), TC2 (open, scattered
obstructions 1.5-5 m), TC2.5 (outer urban/large acreage), TC3 (numerous closely
spaced obstructions 3-10 m, e.g. suburban/light industrial), TC4 (large high
closely-spaced constructions 10-30 m, city centres, developed industrial
complexes) (Cl 4.2.1). Roughness length z₀ = 2 × 10^(TC − 4) m (Note).
Table 4.1 (all regions except A0), TC1 / TC2 / TC2.5 / TC3 / TC4:

| z (m) | TC1 | TC2 | TC2.5 | TC3 | TC4 |
|---|---|---|---|---|---|
| ≤ 3 | 0.97 | 0.91 | 0.87 | 0.83 | 0.75 |
| 5 | 1.01 | 0.91 | 0.87 | 0.83 | 0.75 |
| 10 | 1.08 | 1.00 | 0.92 | 0.83 | 0.75 |
| 15 | 1.12 | 1.05 | 0.97 | 0.89 | 0.75 |
| 20 | 1.14 | 1.08 | 1.01 | 0.94 | 0.75 |
| 30 | 1.18 | 1.12 | 1.06 | 1.00 | 0.80 |
| 40 | 1.21 | 1.16 | 1.10 | 1.04 | 0.85 |
| 50 | 1.23 | 1.18 | 1.13 | 1.07 | 0.90 |
| 75 | 1.27 | 1.22 | 1.17 | 1.12 | 0.98 |
| 100 | 1.31 | 1.24 | 1.20 | 1.16 | 1.03 |
| 150 | 1.36 | 1.27 | 1.24 | 1.21 | 1.11 |
| 200 | 1.39 | 1.29 | 1.27 | 1.24 | 1.16 |

In Region A0, M_z,cat = TC2 value for all z ≤ 100 m, and 1.24 for 100 < z ≤ 200 m
(Note 1). Linear interpolation applies for intermediate height and terrain.
Where upwind terrain varies, M_z,cat is a weighted average over an averaging
distance x_a = larger of 500 m or 40z, ignoring a lag distance x_i = 20z
(Cl 4.2.3, Fig 4.1). Future terrain changes are to be anticipated (Cl 4.1).

### Shielding multiplier M_s (Cl 4.3, Table 4.2)

`[code]` Shielding applies only to h ≤ 25 m; M_s = 1.0 for h > 25 m. Trees and
vegetation do not shield. Only buildings within a 45° sector of radius 20h with
height ≥ h shield, and not where the average upwind ground gradient is above 0.2.
Shielding parameter s = l_s / √(h_s b_s), l_s = h(10/n_s + 5) — Eq 4.3(1)-(2).
Table 4.2: s ≤ 1.5 → 0.7; 3.0 → 0.8; 6.0 → 0.9; ≥ 12.0 → 1.0 (linear
interpolation).

### Topographic multiplier M_t (Cl 4.4)

`[code]`

- Regions A4 and NZ1-4 above 500 m elevation: M_t = M_h M_lee (1 + 0.00015E) —
  Eq 4.4(1).
- Region A0: M_t = 0.5 + 0.5 M_h — Eq 4.4(2).
- Elsewhere: larger of M_h and M_lee.
- M_h = 1.0 outside the local topographic zones (Figs 4.3-4.5) and for H < 10 m.
  For 0.05 ≤ H/(2L_u) ≤ 0.45: M_h = 1 + (H/(3.5(z + L₁)))(1 − |x|/L₂) —
  Eq 4.4(3); for H/(2L_u) > 0.45 within the peak zone: M_h = 1 + 0.71(1 − |x|/L₂)
  — Eq 4.4(4). L₁ = greater of 0.36 L_u and 0.4 H; L₂ = 4L₁ upwind (hills,
  ridges), 10L₁ downwind for escarpments. Table 4.3 gives M_h at the crest:
  1.0, 1.08, 1.16, 1.32, 1.48, 1.71 for H/(2L_u) = <0.05, 0.05, 0.10, 0.20, 0.30,
  ≥ 0.45.
- M_lee applies only to listed NZ lee zones (Tables 4.4-4.5, Fig 4.6); no lee
  zones are identified in Australia (Cl 4.4.3).

`[derived]` For a mine site on a ridge or escarpment in Region A, the M_h
route above is the relevant one, but whether a given terrain feature meets the
Fig 4.3-4.5 definitions needs engineering judgement not stated in the standard.

## Worked reference

None yet.

## Contradictions

None recorded.

## Figures and tables

`[code]` Page crops from the source scan (AS/NZS 1170.2:2021), stored in `0-standards/assets`. They are the authoritative reproduction of the tabulated values; prose transcriptions above are `[derived]` and must be checked against these images.

**Table 3.1A — regional wind speeds australia**

![[as1170-2-table-3.1A-regional-wind-speeds-australia.png]]

**Table 3.1B — regional wind speeds new zealand**

![[as1170-2-table-3.1B-regional-wind-speeds-new-zealand.png]]

**Table 3.2A — wind direction multiplier australia**

![[as1170-2-table-3.2A-wind-direction-multiplier-australia.png]]

**Table 3.2B — wind direction multiplier new zealand**

![[as1170-2-table-3.2B-wind-direction-multiplier-new-zealand.png]]

**Table 3.3 — climate change multiplier**

![[as1170-2-table-3.3-climate-change-multiplier.png]]

**Figure 3.1A — wind regions australia**

![[as1170-2-fig-3.1A-wind-regions-australia.png]]

**Figure 3.1B — wind regions new zealand**

![[as1170-2-fig-3.1B-wind-regions-new-zealand.png]]

**Table 4.1 — terrain height multipliers**

![[as1170-2-table-4.1-terrain-height-multipliers.png]]

**Figure 4.1 — averaging terrain height multipliers**

![[as1170-2-fig-4.1-averaging-terrain-height-multipliers.png]]

**Figure 4.2 — upwind buildings on a slope**

![[as1170-2-fig-4.2-upwind-buildings-on-a-slope.png]]

**Table 4.2 — shielding multiplier**

![[as1170-2-table-4.2-shielding-multiplier.png]]

**Figure 4.3 — hills and ridges**

![[as1170-2-fig-4.3-hills-and-ridges.png]]

**Figure 4.4 — escarpments**

![[as1170-2-fig-4.4-escarpments.png]]

**Figure 4.5 — hills and escarpments slope over 0.45**

![[as1170-2-fig-4.5-hills-and-escarpments-slope-over-0.45.png]]

**Table 4.3 — hill shape multiplier at crest**

![[as1170-2-table-4.3-hill-shape-multiplier-at-crest.png]]

**Table 4.4 — new zealand lee zones**

![[as1170-2-table-4.4-new-zealand-lee-zones.png]]

**Figure 4.6 — new zealand lee zone locations**

![[as1170-2-fig-4.6-new-zealand-lee-zone-locations.png]]

**Table 4.5 — new zealand lee zone coordinates**

![[as1170-2-table-4.5-new-zealand-lee-zone-coordinates.png]]

## Related

- [[as-1170.2-2021-wind-actions]] — source register
- [[as1170-2-wind-design-procedure-and-pressures]]
- [[as1170-2-enclosed-building-pressure-coefficients]]

## Sources

- `raw/0-standards/AS 1170-2-2021-reprint.pdf` — printed pp. 24-39 (Tables 3.1-3.3, 4.1-4.5, Figs 3.1, 4.1-4.6).
