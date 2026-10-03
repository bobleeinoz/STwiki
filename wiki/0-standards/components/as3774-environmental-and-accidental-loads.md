---
title: AS 3774 environmental and accidental loads — wind, settlement, temperature, seismic, swelling, explosion
category: 0-standards
tags: [as3774, silo, wind, seismic, thermal, settlement, swelling, explosion]
standards: [AS 3774:1996 Section 7, AS 3774:1996 Section 8, AS 3774:1996 App D]
status: draft
reviewed: 2026-10-02
---

# AS 3774 environmental and accidental loads

> Scope: AS 3774:1996 Group C (wind C.1, differential settlement C.2,
> differential temperature C.3, seismic C.4, swelling C.5) and Group D
> (vehicle impact, internal explosion, contained water) plus Appendix D.

## Summary

`[code]` Group C and D loads are factored per Table 4.2 (1.5 / 1.25) and
combined only in combination 3 of Table 4.1
([[as3774-load-combinations-and-factors]]).

## Detail

### Wind (Cl 7.1)

`[code]` Design to AS 1170.2; interaction between grouped containers may
produce significantly different loads and specialist advice is advised
(Note to Cl 7.1.1). Wind suction on unroofed containers, containers under
construction or with large self-opening vents is considered separately, with
negative pressure coefficient **−0.8** (Cl 7.1.2). `[derived]` AS 1170.2 has
been superseded by AS/NZS 1170.2; the −0.8 value is the 1996 value and
should be checked against the current wind standard.

`[derived]` **Cross-reference.** The current wind route for circular bins, silos
and tanks is [[as1170-2-bins-silos-and-tanks-wind-pressures]] (AS/NZS 1170.2:2021
App A.5), which gives open-top internal pressure C_p,i = −0.9 − 0.35 log₁₀(c/b) in
place of the flat −0.8. See that page's Contradictions section; flagged for human
review. General procedure: [[as1170-2-wind-design-procedure-and-pressures]].

### Differential settlement (Cl 7.2)

`[code]` Assess settlement patterns by a rational method, splitting them into
uniform, linear (tilt), warping and local parts (Cl 7.2.1). For
column-supported containers a stiff shell (with roof and hopper or stiffening
rings) can lose axial force at a settling column; the reduction ΔF is assessed
rationally but not more than the working-load axial force, and adjacent
columns gain ΔN = 0.75 ΔF (more than four columns) or ΔN = ΔF (four columns)
(Cl 7.2.2). Ground-supported containers: rational analysis, rigorous analysis
for warping/local settlement, and consider serviceability and strength failure
(Cl 7.2.3).

### Differential temperature (Cl 7.3)

`[code]` Solar heating: wall temperature 30 °C above ambient shade for steel,
20 °C for concrete. Sudden ambient change: differential 1.2 times the largest
known ambient drop in 24 h (Cl 7.3.1). Circular containers cooled relative to
contents: added normal pressure
p_nT = ε_w θ E_w c_nT / [(r/t) + (E_w/E_s)(1 − ν)] (Eq 7.3.2), ν = 0.3, with
c_nT = 10.0 for cycling/racketing absent a rational method; added to the
initial pressures; reduction of vertical wall compression also to be checked
(Cl 7.3.2).

`[code]` **Supporting columns (Cl 7.3.3)**: with rigid foundation and
container, the subject column gets N_a = E_c A_c ε_c Δθ_1 (s − 3)/s and every
other column N_i = −E_c A_c ε_c Δθ_1 (1 + 2 x_1/r_1)/s (s columns on pitch
circle radius r_1), superposed over each column in turn.
**Hot solids (Cl 7.3.4)**: absent better data the inside wall temperature is
20 °C below the mean solid temperature.

![[as3774-fig-7.1-column-pitch-circle.png]]
*Figure 7.1 — column pitch circle (r_1, x_1, subject column).*

### Seismic (Cl 7.4)

`[code]` Assess per AS 1170.4 but where AS 3774 and AS 1170.4 both define a
quantity, **AS 3774 takes precedence** (Cl 7.4.1). Base shear
V = I (C S / R_f) G_g, with I = 1.25 (1.0 only with clear justification),
S = 1.5 (2.0 poor soil, V_s < 150 m/s in the upper 10 m; 1.0 on bedrock),
R_f = 2.5 for elevated structures designed for ductility, 1.0 for non-ductile
elevated and ground-supported structures.

**Elevated containers (Cl 7.4.2)**: if the fundamental mode is not simple
translation of container and contents on the support stiffness, a more
complete analysis is needed; otherwise C = 1.25 a / T^(2/3) with a ≥ 0.03,
T = 2.0 (G_g/K_str)^0.5 — direction chosen for least favourable effect, force
applied at the centre of mass of the stored solid.

![[as3774-fig-7.2-elevated-container-vibration-mode.png]]
*Figure 7.2 — fundamental vibration mode for elevated containers: equivalent lateral load V and weight G_g on the support structure.*

**Ground-supported (Cl 7.4.3)**: cylindrical — normal pressure
p_nw = u_1 γ I S a cos β_1 (not less than 1.5 u_1 γ a cos β_1) and traction
p_q = u_1 γ I S a sin β_1 (not less than u_1 γ a sin β_1), constant with
height, u_1 = 0.25 d_c for d_c/h_b < 2 and 0.50 h_b for d_c/h_b > 2; base shear
p_qb = h_b γ I S a (≥ 1.5 h_b γ a) for h_b/d_c > 2, and
(2/(d_c/h_b)) h_b γ I S a (≥ 1.5 × that factor × h_b γ a) for h_b/d_c < 2.
Rectangular — p_nw = u_1 γ I S a (≥ 1.5 u_1 γ a) uniformly on up- and
down-stream walls, same for side-wall traction, u_1 = 0.5 l_w for h_b/l_w > 2
and h_b for < 2; base traction equals the sum of wall pressures and friction
divided by plan area.

![[as3774-fig-7.3-ground-supported-container-earthquake-pressures.png]]
*Figure 7.3 — pressures on ground-supported containers during earthquakes: (a) top view with β_1 and earthquake direction, (b) section with pressure increase over h_b.*

`[code]` The minimum 1.5 I S a constraint (not less than 1.5 × 0.03 ≈ 0.05)
is deliberate because of the complexity of bin seismic response (Note to
Cl 7.4.3.2). `[derived]` AS 1170.4:1993 is superseded by AS 1170.4:2007; seismic
parameters (a, S, R_f, I) in this Standard are 1993-vintage and cannot be
reused with the current seismic standard without a documented
reconciliation. See [[as4100-earthquake-design-requirements]] for the steelwork
ductility basis.

### Swelling of stored solids (Cl 7.5)

`[code]` For agricultural products where moisture rises by more than 1 % and
the base is very stiff, p_sw = γ r_c c_sw/μ with c_sw = e^(+z/z_o) − 1 (note the
positive sign), z_o = r_c/(μ k_sw), k_sw = 1.0 absent better data, lower μ
(Eq 7.5(1)). Upward vertical friction p_q,sw = μ p_sw (upper μ); vertical wall
tension N_ten = γ r_c (z_o c_sw − z) (Eq 7.5(3)); floor designed for
p_v = γ r_c c_sw/(μ k_sw) (Eq 7.5(4)). A separate load case, not added to
filling/flow pressures; also used for moisture changes under 1 % unless a
rational assessment is made.

### Accidental loads (Section 8, Appendix D)

`[code]` **Vehicle impact (Cl 8.1)**: appropriate impact forces unless positive
protection is provided. **Internal explosion (Cl 8.2)**: investigate where
the solid contains ignitable fines (vegetable, animal, carbonaceous,
synthetic organic) or emits flammable gas; test where necessary.
**Contained water (Cl 8.3)**: hydrostatic loads where fire-protection water or
other accumulation is possible, including near-empty containers whose outlet
is plugged by the stored material.

`[code]` Appendix D (informative): calculated explosion pressures (Schofield
1984) are usually too large to contain; fit bursting panels or rapid-opening
hatches opening at ≤ 2.5 kPa; absent precise calculation the walls should
withstand ≥ 100 kPa without rupture. Gas or gas-dust explosions are more
severe and it is often uneconomic to design for them — prevent gas build-up.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as-3774-1996-loads-on-bulk-solids-containers]]
- [[as3774-load-combinations-and-factors]]
- [[as3774-silo-wall-pressures-initial-and-flow]]
- [[as3774-special-service-loads]]

## Sources

- `raw/0-standards/AS 3774-reprint.pdf` — AS 3774—1996 incl. Amdt 1, 2 (1998), Sections 7-8, Appendix D.
