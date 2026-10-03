---
title: AS/NZS 1170.2 dynamic response factor, crosswind response and accelerations
category: 0-standards
tags: [as1170-2, wind, dynamic, cdyn, crosswind, vortex-shedding, towers, poles]
standards: [AS/NZS 1170.2:2021 Cl 6.1-6.6, AS/NZS 1170.2:2021 App E.1-E.2]
status: draft
reviewed: 2026-10-03
---

# AS/NZS 1170.2 dynamic response (Section 6)

> Scope: Section 6 and App E.1-E.2. Equations are transcribed from scanned
> pages and should be checked against the printed standard before use.

## Summary

`[code]` C_dyn multiplies the design pressure for dynamically wind-sensitive
structures (Eq 2.4(1), [[as1170-2-wind-design-procedure-and-pressures]]).

## Detail

### Exclusions (Cl 6.1)

`[code]` Section 6 gives no C_dyn for: first-mode frequency < 0.2 Hz, height
> 200 m, or significant modal coupling in the first three modes; buildings
with two sway modes within 10 % of each other and both < 0.4 Hz; height-to-width
ratio > 6; linked buildings with first-mode < 0.5 Hz; aerodynamic interference
excitation; roofs supported on two or more sides with f < 0.8 Hz; cantilevered
roofs f < 0.5 Hz; facade elements.

### C_dyn = 1.0 (Cl 6.2)

`[code]` Buildings and free-standing towers with first-mode frequency > 1 Hz;
poles and chimneys with height/average diameter < 5; ground-mounted solar
panels with f > 5 Hz.

### Other structures (Cl 6.3)

`[code]` Frequencies 0.2-1 Hz: along-wind C_dyn from Cl 6.2 (equations below)
and crosswind from Cl 6.3 (as numbered in the standard). Cantilevered roofs
0.5-1 Hz: Cl B.5. Circular poles, masts and chimneys with aspect ratio > 5:
Cl 6.2.2 and 6.3.3. Horizontal slender structures 0.5-1 Hz: Cl 6.2.3. Wind-tunnel
tests are recommended where crosswind exceeds along-wind (Note 3).

### Along-wind C_dyn (Cl 6.4)

`[code]` Tall buildings and free-standing towers, at height s < z < h:

C_dyn = [1 + 2 I_h √(g_v² B_s + H_s g_R² S E_t / ζ)] / [1 + 2 g_v I_h] — Eq 6.2(1)

with g_v = 3.4; B_s = 1/(1 + √(0.26(h−s)² + 0.46 b_sh²)/L_h) — Eq 6.2(2);
L_h = 85(h/10)^0.25 — Eq 6.2(3); H_s = 1 + (s/h)²; g_R = √(1.2 + 2 ln(600 n_a))
— Eq 6.2(4); S per Eq 6.2(5); E_t = πN/(1 + 70.8N²)^(5/6) — Eq 6.2(6), with
N = n_a L_h[1 + g_v I_h]/V_des,θ; turbulence intensity I_h from Table 6.1 at z = h
(e.g. TC2 at 10 m: 0.183; TC3 at 20 m: 0.215). For base moments, deflection and
acceleration take s = 0. V_des,θ at h. Damping ζ (Notes): ultimate limit states
steel 0.015-0.02, reinforced concrete 0.02-0.03 of critical.

Towers/poles/masts with large headframes: Eq 6.2(7)-(8) with h_eff, b_eff
(Fig 6.2). Horizontal slender structures (elevated pipelines, gantries):
Eq 6.2(9)-(11), B′ = 1.0 in Regions A0, A2, A3, A5 and B1, else 1/(1 + 0.68b/L_h).

### Crosswind response (Cl 6.5)

`[code]` Not required for porous lattice towers (Cl 6.5.1). Rectangular tall
buildings/towers: equivalent static force w_eq(z) = 0.5 ρ_air [V_des,θ]² d C_shp
C_dyn — Eq 6.3(1), with (C_shp C_dyn) = 1.5 g_R (b/d) K_m/(1 + g_v I_h)² (z/h)^k
√(π C_fs/ζ) — Eq 6.3(2); K_m = 0.76 + 0.24k; mode-shape exponent k = 1.5
(uniform cantilever), 0.5 (slender moment frame), 1.0 (core with moment façade),
2.3 (tower with decreasing stiffness or large top mass). Base moment Eq 6.3(3).
C_fs from Eqs 6.3(5)-6.3(9) with reduced velocity V_n = V_des,θ/(n_c b(1 + g_v I_h));
above V_n = 8 the method is for preliminary design only (wind-tunnel testing is
advised); no extrapolation.

Circular chimneys, masts and poles (Cl 6.5.3): tip deflection from vortex shedding
Eqs 6.3(10)-6.3(11), constants a_L, K_a,max, C_c in Table 6.2 (by Reynolds
number), Strouhal St = 0.20; equivalent static force
w_eq(z) = m(z)(2πn₁)² y_max φ₁(z), φ₁ = (z/h)²; critical speed ≈ 5 n₁ b_t.
Damping for unlined welded steel poles/stacks 0.002 of critical; reinforced
concrete towers/chimneys 0.005.

### Combining along-wind and crosswind (Cl 6.6)

`[code]` Base-moment combinations (Table 6.3(A), buildings < 70 m): 1.0 along ± 0.8
across, and 0.8 along ± 1.0 across; Table 6.3(B) (> 70 m) adds offsets of 0.15B
or 0.2B. Combined scalar effect (Eq 6.4(1)):
ε_t = ε_a,m + √((ε_a,p − ε_a,m)² + ε_c,p²). The method assumes independent,
random along-wind and crosswind responses and is not for circular cross-sections
under vortex shedding (Note).

### Informative accelerations (App E.1-E.2)

`[code]` Serviceability indicator: acceleration may be exceeded if h^1.3/m₀ > 0.0016
(Eq E.1). Peak along-wind acceleration at the top: Eq E.2 (based on the resonant
base bending moment). E.3-E.6 (rotational velocity, torsion, combined) not yet
ingested.

`[derived]` For conveyor gantries and transfer towers the Section 6.1 exclusions
and the 1 Hz threshold mean many stiff mining structures take C_dyn = 1.0, but
tall slender stacks, flares and long-span gantries can fall in the 0.2-1 Hz band
and need the dynamic method; frequency should be confirmed from the analysis
model before choosing the path.

## Worked reference

None yet.

## Contradictions

None recorded.

## Figures and tables

`[code]` Page crops from the source scan (AS/NZS 1170.2:2021), stored in `0-standards/assets`. They are the authoritative reproduction of the tabulated values; prose transcriptions above are `[derived]` and must be checked against these images.

**Figure 6.1 — notation for heights**

![[as1170-2-fig-6.1-notation-for-heights.png]]

**Figure 6.2 — dimensions of pole or mast with headframe**

![[as1170-2-fig-6.2-dimensions-of-pole-or-mast-with-headframe.png]]

**Table 6.1 — turbulence intensity**

![[as1170-2-table-6.1-turbulence-intensity.png]]

**Figure 6.3 — crosswind force spectrum 3to1to1 square**

![[as1170-2-fig-6.3-crosswind-force-spectrum-3to1to1-square.png]]

**Figure 6.4 — crosswind force spectrum 6to1to1 square**

![[as1170-2-fig-6.4-crosswind-force-spectrum-6to1to1-square.png]]

**Figure 6.5 — crosswind force spectrum 6to2to1 rectangle**

![[as1170-2-fig-6.5-crosswind-force-spectrum-6to2to1-rectangle.png]]

**Figure 6.6 — crosswind force spectrum 6to1to2 rectangle**

![[as1170-2-fig-6.6-crosswind-force-spectrum-6to1to2-rectangle.png]]

**Table 6.2 — vortex shedding constants**

![[as1170-2-table-6.2-vortex-shedding-constants.png]]

**Table 6.3A — equivalent static load combinations below 70m**

![[as1170-2-table-6.3A-equivalent-static-load-combinations-below-70m.png]]

**Table 6.3B — equivalent static load combinations above 70m**

![[as1170-2-table-6.3B-equivalent-static-load-combinations-above-70m.png]]

## Related

- [[as-1170.2-2021-wind-actions]] — source register
- [[as1170-2-wind-design-procedure-and-pressures]]
- [[as1170-2-exposed-members-frames-and-lattice-towers]]

## Sources

- `raw/0-standards/AS 1170-2-2021-reprint.pdf` — printed pp. 58-69 and 108.
