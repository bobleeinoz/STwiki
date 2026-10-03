---
title: AS 3774 special service loads — rapid filling, pneumatic, impact, gas pressure, platforms, restraints
category: 0-standards
tags: [as3774, silo, impact, rapid-filling, pneumatic, gas-pressure, live-load]
standards: [AS 3774:1996 Cl 6.2.1.5-6.2.1.7, AS 3774:1996 Cl 6.7, AS 3774:1996 Cl 6.8, AS 3774:1996 Cl 6.9, AS 3774:1996 Cl 6.12]
status: draft
reviewed: 2026-10-02
---

# AS 3774 special service loads

> Scope: AS 3774:1996 normal-service loads outside the Janssen/flow
> framework: rapid filling of powders, pneumatic blending, lump impact on
> walls, live loads on platforms/roofs (B.5), gas pressure/suction (B.6),
> lateral restraint forces (B.7), and roof spillage.

## Summary

`[code]` These loads modify or add to the initial pressures of
[[as3774-silo-wall-pressures-initial-and-flow]] and enter Table 4.1
([[as3774-load-combinations-and-factors]]).

## Detail

### Powders: rapid filling and pneumatic blending

`[code]` **Rapid filling of powders (Cl 6.2.1.5)** without experimental data:
p_ni is the lesser of 0.6 γ z (Eq 6.2.1.5(1)) and p_niF = c_F v_F γ
(Eq 6.2.1.5(2), acting below z_m = c_F v_F/0.60), linear between z = 0 and
z_m. The result is not less than Eq 6.2.1.1. Filling rate v_F is the
volumetric filling rate divided by the cross-section area (m/h); c_F from
Table 6.4.

![[as3774-table-6.4-coefficient-of-rapid-filling.png]]
*Table 6.4 — coefficient of rapid filling c_F (h): flour 0.14, ground phosphate 0.14, pulverised coal 0.15, powdered coal 1.18, cement 0.19, lime powder 0.36.*

`[derived]` The printed 1.18 for powdered coal is an order of magnitude above
the other entries and is probably a misprint (0.18); verify before use.

`[code]` **Pneumatic blending (Cl 6.2.1.6)**: p_np = 0.6 γ z; the Cl 6.3
flow multiplier does not apply; design pressure is the greater of p_np and
Eq 6.3.2.1(1).

![[as3774-fig-6.3-initial-pressure-modifications.png]]
*Figure 6.3 — initial pressure modifications: (a) pneumatic blending p_np, (b) rapid filling p_niF with depth z_m, versus slow-filling p_ni.*

### Impact of lumps on vertical walls (Cl 6.2.1.7)

`[code]` Local force F_w = 0.1 m v_E (kN; m in kg), with
v_E = √(v_c² + 2 g h_1) unless reliable data exist; it acts on a wall area equal
to 0.25 of the projected area of the lump and not at all points around the
perimeter simultaneously.

### Platforms, roofs and spillage (Cl 6.7, 6.12)

`[code]` Individual live-load members follow AS 1170.1; for global design of a
large untrafficable platform or roof the live load may be 1.0 kPa unless
dust collection is possible; platforms, walkways and ladders follow AS 1657
(Cl 6.7). Spillage onto roofs after overfilling is assessed allowing for
caking from weather exposure (Cl 6.12).

### Gas pressure and suction (Cl 6.8)

`[code]` Dust-extraction suction comes from the fan manufacturer, but not less
than 0.3 kPa; safety vents where blocked filters could exceed design values
(Cl 6.8.1). Adiabatic suction from temperature drop below dewpoint in
moist grain/foodstuff containers is investigated (Cl 6.8.2). **Pneumatic
discharge (Cl 6.8.3)**: local peak p_c = 0.8 p_B (blower pressure), declining
linearly to zero at h_B = 1.3 p_B/γ above the blower outlet; combined with the
initial pressure as p_nB = 1.2 p_ni + p_c, and need not be combined with flow
pressures; a safety vent is required. **Rapid discharge of low-permeability
solids (Cl 6.8.4)**: the upper part is designed for negative pressure of 1.2
times the vent opening pressure (from the manufacturer).

### Lateral restraint (Cl 6.9)

`[code]` Where the substructure restrains the container, forces follow the
appropriate design standard with a **minimum lateral force of 2.5 % of loads of
types A.1, B.1, B.4 and B.5** (Cl 6.9.1). Where the container restrains other
structures, forces are determined per AS 1250 and applied recognising local
joint conditions (Cl 6.9.2). `[derived]` AS 1250 is superseded by AS 4100
(see [[as-4100-2020-steel-structures]]); the cross-reference needs updating
when applied.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as-3774-1996-loads-on-bulk-solids-containers]]
- [[as3774-silo-wall-pressures-initial-and-flow]]
- [[as3774-hopper-pressures-and-feeder-loads]]
- [[as3774-environmental-and-accidental-loads]]

## Sources

- `raw/0-standards/AS 3774-reprint.pdf` — AS 3774—1996 incl. Amdt 1, 2 (1998), Cl 6.2.1.5-6.2.1.7, 6.7-6.9, 6.12.
