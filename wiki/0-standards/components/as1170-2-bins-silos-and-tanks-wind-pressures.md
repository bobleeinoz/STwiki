---
title: AS/NZS 1170.2 wind pressures on circular bins, silos and tanks (Appendix A.5)
category: 0-standards
tags: [as1170-2, wind, silo, bin, tank, cylinder, roof, internal-pressure]
standards: [AS/NZS 1170.2:2021 App A.5, AS/NZS 1170.2:2021 Cl 5.2(b)]
status: draft
reviewed: 2026-10-03
---

# AS/NZS 1170.2 wind on circular bins, silos and tanks

> Scope: Appendix A.5 of AS/NZS 1170.2:2021, the wind-pressure route for
> circular bins, silos and tanks that AS 3774 defers to
> ([[as3774-environmental-and-accidental-loads]]). Equations are transcribed from
> scanned pages — check against the printed standard before use.

## Summary

`[code]` Cl 5.2(b) sends circular bins, silos and tanks to Appendix A. Use design
speed per [[as1170-2-wind-design-procedure-and-pressures]] and multipliers per
[[as1170-2-regional-wind-speeds-and-site-multipliers]]. Standard M_d = 1.0 applies
for tanks and chimneys of circular or polygonal section (Cl 3.3(a)).

## Detail

### Grouped containers (A.5.1)

`[code]` Spacing between walls greater than two diameters: treat as isolated
silos. Closely spaced groups (spacing < 0.1 diameter): treat as a single
structure using Tables 5.2(A)-(C) and 5.3(A)-(C). Intermediate spacing: linear
interpolation.

### Walls (A.5.2.1)

`[code]` C_shp = C_p,b(θ_b) = k_b C_p1(θ_b) — Eq A.5(1), for a cylinder standing on
the ground or on columns not higher than the cylinder height c, and 0.25 ≤ c/b
≤ 4.0 (b = diameter, θ_b = angle from the wind direction):

- k_b = 1.0 for C_p1 ≥ −0.15; otherwise k_b = 0.55[C_p1(θ_b) + 0.15] log₁₀(c/b)
  — Eq A.5(2)
- C_p1(θ_b) = −0.5 + 0.4 cos θ_b + 0.8 cos 2θ_b + 0.3 cos 3θ_b − 0.1 cos 4θ_b −
  0.05 cos 5θ_b — Eq A.5(3) (Fig A.6 plots C_p1 for c/b = 1.0: about +0.8 at the
  windward generator, zero near 30°, minimum about −1.4 near 80-90°, about
  −0.4 at the rear).

`[code]` Overall drag on the wall section (elevated or on ground): C_shp = 0.63,
based on elevation area b × c. Underside of elevated bins: as elevated enclosed
rectangular buildings (Cl 5.4.1,
[[as1170-2-enclosed-building-pressure-coefficients]]).

### Roofs and lids (A.5.2.2)

`[code]` C_shp = C_p,e K_a K_ℓ — Eq A.5(4), with C_p,e from Table A.4: Zone A −0.8,
Zone B −0.5 (zones in Fig A.7, 0.25 < c/b < 4.0; conical α < 10° or average domed
α < 10°; 10° ≤ α ≤ 30°). K_a per Cl 5.4.2 and K_ℓ per Cl 5.4.4. The local
pressure factor applies to windward edges of roofs with slope ≤ 30° and to the
region near the cone apex for slopes greater than 15°; local zone dimensions a = 0.1b
and ℓ = 0.25c (Fig A.7).

### Internal pressure (A.5.2.3)

`[code]` Vented-roof containers: area-weighted average of the external pressures
at the vents and openings (per A.5.2.2). Open-top containers:
C_shp = C_p,i = −0.9 − 0.35 log₁₀(c/b) — Eq A.5(5).

`[derived]` For a 10 m diameter × 20 m high open-top bin (c/b = 2),
Eq A.5(5) gives C_p,i ≈ −0.9 − 0.35 × 0.301 = −1.01. This is arithmetic from the
equation as transcribed here, not a clause statement.

## Worked reference

None yet.

## Contradictions

- AS 3774-1996 Cl 7.1.2 specifies suction coefficient −0.8 for unroofed
  containers, containers under construction or with large self-opening vents
  ([[as3774-environmental-and-accidental-loads]]). AS/NZS 1170.2:2021 Eq A.5(5)
  gives −0.9 − 0.35 log₁₀(c/b) for open-top containers (≈ −0.9 at c/b = 1, more
  negative for taller containers, less negative below c/b = 1). Both are recorded;
  the current wind standard is the later one. Flagged for the human.

## Figures and tables

`[code]` Page crops from the source scan (AS/NZS 1170.2:2021), stored in `0-standards/assets`. They are the authoritative reproduction of the tabulated values; prose transcriptions above are `[derived]` and must be checked against these images.

**Figure A.5 — circular bin wall cpb parameters**

![[as1170-2-fig-A.5-circular-bin-wall-cpb-parameters.png]]

**Figure A.6 — circular bin wall cp1 plot**

![[as1170-2-fig-A.6-circular-bin-wall-cp1-plot.png]]

**Table A.4 and Figure A.7 — circular bin silo roof cpe**

![[as1170-2-table-A.4-and-fig-A.7-circular-bin-silo-roof-cpe.png]]

## Related

- [[as-1170.2-2021-wind-actions]] — source register
- [[as1170-2-wind-design-procedure-and-pressures]]
- [[as1170-2-enclosed-building-pressure-coefficients]]
- [[as3774-environmental-and-accidental-loads]]
- [[as3774-load-combinations-and-factors]] — where wind enters the silo combinations

## Sources

- `raw/0-standards/AS 1170-2-2021-reprint.pdf` — printed pp. 73-76 (A.5), p. 42 (Cl 5.2(b)).
