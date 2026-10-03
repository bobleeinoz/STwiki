---
title: AS/NZS 1170.2 wind on exposed members, open frames, lattice towers and porous plant (Appendix C)
category: 0-standards
tags: [as1170-2, wind, lattice-tower, open-frame, pipe-rack, conveyor-gantry, drag-coefficient, solidity]
standards: [AS/NZS 1170.2:2021 App C.1-C.4]
status: draft
reviewed: 2026-10-03
---

# AS/NZS 1170.2 exposed members, frames and lattice towers

> Scope: Appendix C. This is the wind route for open-framed mining structures —
> pipe racks, conveyor gantries, transfer-tower frames — and lattice towers.
> Tables are transcribed from scanned pages; check against the printed standard
> before use.

## Summary

`[code]` Appendix C gives C_shp for exposed structural members, frames, trusses and
towers. Use wind speed at the height of the component (C.1). Force is calculated
with Eq 2.5(3) using the reference area A_z for the member or section
([[as1170-2-wind-design-procedure-and-pressures]]).

## Detail

### Individual members, aspect ratio > 8 (C.2.1)

`[code]` Wind axes: C_shp = K_ar K_i C_d — Eq C.2(1). Body axes:
C_shp = K_ar K_i C_F,x (major axis), K_ar K_i C_F,y (minor axis) — Eqs C.2(2)-(3).
K_i = 1.0 for wind normal to the member, sin²θ_m for rounded cylinders, sin θ_m
for sharp-edged prisms (b/r > 16). K_ar (Table C.1, l/b): ≤ 8 → 0.7; 14 → 0.8;
30 → 0.9; ≥ 40 → 1.0 (linear interpolation).

### Single open frame (C.2.2)

`[code]` For 0.2 < δ_e < 0.8 and 1/3 < l/b < 3: C_shp = 1.2 + 0.26(1 − δ_e) —
Eq C.2(4), reference area = sum of projected member areas normal to the frame.
δ_e = δ for flat-sided members and 1.2 δ^1.75 for circular members (δ = solidity
ratio = solid area/total area). Otherwise sum the effects on individual members
and attachments (Cl 2.5.3.3 and C.2.1).

### Multiple open frames and porous industrial plant (C.2.3)

`[code]` C_shp = C_shp,1 + Σ K_sh C_shp,1 — Eq C.2(5), with K_sh from Table C.2 by
wind angle (0° or 45°), frame spacing ratio λ (centre-to-centre spacing divided by
the smaller of l or b) and effective solidity δ_e. At 0° with λ = 1.0: K_sh = 1.0
(δ_e 0-0.1), 0.8 (0.2), 0.7 (0.3), 0.5 (0.4), 0.3 (0.5), 0.2 (0.7, 1.0). K_sh = 1.0
for λ ≥ 8. Linear interpolation applies.

`[code]` Note on porous industrial complexes such as petrochemical plants:
divide the plant into 4-6 (not more than 8) sections by planes normal to the wind;
section spacing s is the along-wind length divided by the number of sections,
chosen to coincide with key columns; compute element drag coefficients as if
unshielded; K_sh = 1.0 for the first windward section, Table C.2 for downwind
sections using frame spacing ratio s divided by a representative plant height and
the combined effective solidity of all upwind elements seen in cross-section.

### Force coefficients for sections (C.3)

`[code]`

- Rounded cylinders (Table C.3, C_d): cylinder 1.2 for bV_des,θ < 4 m²/s and,
  above 10 m²/s, C_d = 1.0 + 0.033[log₁₀(V_des,θ h_r)] − 0.025[log₁₀(V_des,θ h_r)]²
  or 0.6 if greater; typical h_r: galvanised steel 150 × 10⁻⁶ m, light rust
  2.5 × 10⁻³ m, heavy rust 15 × 10⁻³ m, painted metal 30 × 10⁻⁶ m. Attachments
  projecting > 1 % of the diameter give C_d = 1.2. Ellipse narrow side to wind
  0.7 / 0.3 (b/d = 1/2); broad side 1.7 / 1.5 (b/d = 2). Helically wound cables:
  1.2 (bV_des,θ < 0.5 m²/s), 1.0 (> 5 m²/s).
- Sharp-edged prisms (Table C.4, C_d): square face-on 2.2, corner-on 1.5;
  equilateral triangle apex to wind 1.2, face to wind 2.0; hexagon 1.2 face / 1.5
  corner; octagon 1.4; 12-sided 1.3; 16-sided 1.0.
- Structural sections (Table C.5, C_F,x / C_F,y) for angles, channels, tees and
  I-sections at θ = 0°, 45°, 90°, 135°, 180°; for an I-section with d = 0.48b at
  0°: 2.05 / 0. Rectangular prisms: Figure C.2 (e.g. d/b = 1 at 0°: C_F,x 2.2).
  Rectangular sections can experience dynamic crosswind forces; seek specialist
  advice (Note C.3.2).

### Lattice towers (C.4)

`[code]` Divide the tower into vertical sections (at least 10 where possible);
design for eight wind directions with V_des,θ the maximum V_sit,β within ±22.5° of
the 45° direction considered (C.4.1). C_shp for guy cables: 1.2 sin²θ_m at wind speed
for 2/3 of the cable height. Sections without ancillaries: C_d from Tables
C.6(A)-(C) (Table C.6(A), flat-sided members, square-in-plan onto face: 3.5
(δ_e ≤ 0.1), 2.8 (0.2), 2.5 (0.3), 2.1 (0.4), 1.8 (≥ 0.5); onto corner 3.9, 3.2, 2.9,
2.6, 2.3; equilateral triangle 3.1, 2.7, 2.3, 2.1, 1.9). Circular-member towers
(Tables C.6(B)-(C)) are split by b_i V_des,θ < 3 or ≥ 6 m²/s and flagged as sparse
data to be used with caution.

`[code]` Sections with ancillaries (C.4.2.2): C_de = C_d + ΣΔC_d — Eq C.4(1),
ΔC_d = C_da K_ar K_in (A_a/A_z) — Eq C.4(2). Interference factor K_in
(C.4.2.3): ancillary on the face of a square tower
[1.5 + 0.5 cos 2(θ_a − 90°)] exp[−1.2(C_d δ)²]; triangular tower with 1.8 in the
exponent; lattice-like ancillary inside the tower exp[−1.4(C_d δ)^1.5] (square) or
exp[−1.8(C_d δ)^1.5] (triangular); cylindrical ancillaries use exponent
a = 2.7 − 1.3 exp[−3(b/w)²] (square) and c = 6.8 − 5 exp[−40(b/w)³] (triangular).
UHF antennas: Table C.7 (1.3-1.5) and Figure C.3.

`[derived]` For a conveyor gantry modelled as a truss, the K_sh route
(C.2.3) with δ_e from the member solidity applies to the second and subsequent
truss planes only when they are of similar open-frame type; belt, covers and
walkway cladding are better treated by Cl 5.2/Appendix B rather than as
open-frame solidity. This selection is judgement, not a clause statement.

## Worked reference

None yet.

## Contradictions

None recorded.

## Figures and tables

`[code]` Page crops from the source scan (AS/NZS 1170.2:2021), stored in `0-standards/assets`. They are the authoritative reproduction of the tabulated values; prose transcriptions above are `[derived]` and must be checked against these images.

**Table C.1 — aspect ratio correction factors kar**

![[as1170-2-table-C.1-aspect-ratio-correction-factors-kar.png]]

**Figure C.1 — notation for frame dimensions**

![[as1170-2-fig-C.1-notation-for-frame-dimensions.png]]

**Table C.2 — shielding factors multiple frames**

![[as1170-2-table-C.2-shielding-factors-multiple-frames.png]]

**Table C.3 — drag coefficients rounded cylindrical shapes**

![[as1170-2-table-C.3-drag-coefficients-rounded-cylindrical-shapes.png]]

**Table C.4 — drag coefficients sharp edged prisms**

![[as1170-2-table-C.4-drag-coefficients-sharp-edged-prisms.png]]

**Table C.5 — force coefficients structural sections**

![[as1170-2-table-C.5-force-coefficients-structural-sections.png]]

**Table C.5 — force coefficients structural sections continued**

![[as1170-2-table-C.5-force-coefficients-structural-sections-continued.png]]

**Figure C.2 — force coefficients rectangular prisms**

![[as1170-2-fig-C.2-force-coefficients-rectangular-prisms.png]]

**Table C.6A — lattice towers square and triangle flat sided**

![[as1170-2-table-C.6A-lattice-towers-square-and-triangle-flat-sided.png]]

**Table C.6B — lattice towers square circular members**

![[as1170-2-table-C.6B-lattice-towers-square-circular-members.png]]

**Table C.6C — lattice towers triangle circular members**

![[as1170-2-table-C.6C-lattice-towers-triangle-circular-members.png]]

**Table C.7 — uhf antenna drag coefficient**

![[as1170-2-table-C.7-uhf-antenna-drag-coefficient.png]]

**Figure C.3 — uhf antenna sections**

![[as1170-2-fig-C.3-uhf-antenna-sections.png]]

**Figure C.4 — tower sections with ancillaries**

![[as1170-2-fig-C.4-tower-sections-with-ancillaries.png]]

## Related

- [[as-1170.2-2021-wind-actions]] — source register
- [[as1170-2-wind-design-procedure-and-pressures]]
- [[as1170-2-dynamic-response-and-crosswind]]
- [[as1170-2-freestanding-walls-roofs-and-flags]]
- [[as4100-member-effective-length-and-frame-buckling]] — downstream member checks (AS 4100)

## Sources

- `raw/0-standards/AS 1170-2-2021-reprint.pdf` — printed pp. 92-105 (Appendix C).
