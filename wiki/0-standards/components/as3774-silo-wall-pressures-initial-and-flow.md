---
title: AS 3774 vertical wall pressures — initial (filling) and flow, flat-bottom bases
category: 0-standards
tags: [as3774, silo, janssen, wall-pressure, flow-pressure, flat-bottom]
standards: [AS 3774:1996 Cl 6.1, AS 3774:1996 Cl 6.2, AS 3774:1996 Cl 6.3.1-6.3.4, AS 3774:1996 Cl 6.4]
status: draft
reviewed: 2026-10-02
---

# AS 3774 vertical wall pressures — initial and flow

> Scope: AS 3774:1996 symmetric initial loads on vertical walls and closures
> (Cl 6.2.1-6.2.3.2), flow loads on vertical walls and flat bottoms
> (Cl 6.3.1-6.3.4), and eccentric filling (Cl 6.4). Hopper walls are in
> [[as3774-hopper-pressures-and-feeder-loads]]; eccentric discharge in
> [[as3774-eccentric-filling-and-discharge-loads]].

## Summary

`[code]` Initial (filling/storage) pressure is the Janssen-type pressure
p_ni = γ r_c c_z / μ (Eq 6.2.1.1), with c_z = 1 − e^(−z/z_o) and z_o = r_c/(μk).
Flow pressure is the initial pressure times a flow multiplier, constant over the
full wall height and over a flat bottom (Cl 6.3.1).

`[code]` Which characteristic value governs depends on the effect (Table 6.1):
maximum normal pressure on cylinder wall — φ_w lower, k upper, φ_i lower;
maximum frictional traction — φ_w upper, k upper, φ_i lower; maximum vertical
load on hopper — φ_w lower, k lower, φ_i upper; maximum hopper pressures —
φ_w lower (for hopper), φ_i upper. For wall liners both "liner present" and
"liner absent" friction values are evaluated (Cl 6.1.3).

![[as3774-table-6.1-appropriate-property-values.png]]
*Table 6.1 — appropriate characteristic values of properties by application.*

## Detail

### Initial pressures on vertical walls (Cl 6.2.1)

`[code]` Lateral pressure ratio
k = [1 + sin²φ_i − 2√(sin²φ_i − μ²cos²φ_i)] / (4μ² + cos²φ_i), **not less than
0.35** (Cl 6.2.1.1). Table 6.3 / Figure 6.1 tabulate k; Table 6.2 tabulates c_z
(e.g. z/z_o = 2.2 → 0.89). Rectangular containers need separate assessments for
long and short walls with the respective r_c.

![[as3774-table-6.2-janssen-depth-function.png]]
*Table 6.2 — Janssen depth function c_z.*

![[as3774-table-6.3-lateral-pressure-ratio-k.png]]
*Table 6.3 — lateral pressure ratio k vs φ_i and φ_w.*

![[as3774-fig-6.1-lateral-pressure-ratio.png]]
*Figure 6.1 — lateral pressure ratio k vs wall friction angle, with lower limit 0.35 and the φ_w = φ_i limit.*

`[code]` Values of φ_i and μ are taken to maximise pressure per Table 6.1 (the source text says "lower characteristic value of d_i", which `[derived]` is read as φ_i): tall (A3)
containers use lower φ_w; very squat (A1) containers can have higher pressure at
the upper φ_w; intermediate (A2) must check both (Cl 6.2.1.1).

`[code]` **Squat containers (Cl 6.2.1.2)**: pressure at the highest solid–wall
contact may be reduced to zero, linearly increasing to the Eq 6.2.1.1 value at
z = 1.5 h_o: p_ni = (z − h_o)/(0.5 h_o) · p_1 for h_o < z < 1.5 h_o, with
p_1 = γ r_c c_1/μ and c_1 = 1 − e^(−1.5h_o/z_o).

![[as3774-fig-6.2-initial-pressure-squat-containers.png]]
*Figure 6.2 — initial pressure distribution in squat containers.*

`[code]` **Overfilled squat container (Cl 6.2.1.3)**: upward roof pressure
p_U = 0.1 γ z_c, normal to the roof. **Wall flexibility (Cl 6.2.1.8)**:
squat circular containers may use p_ni,red = ψ p_ni, ψ = 1 − E_s(d_c/2)/(E_w t)
≥ 0.85. **Minimum pressure (Cl 6.2.1.9)** where it matters for vertical wall
force: 0.8 γ r_c c_z/μ for free-flowing, 0.5 γ r_c c_z/μ for cohesive solids,
with c_z and μ chosen to maximise vertical load.
**Vibration (Cl 6.2.1.10)**: where induced accelerations exceed 0.05 g
(vibratory feeders, screens, crushers, flow aids) the increase in bulk density
must be investigated. Other increases in normal pressure are listed in
Cl 6.2.1.4 (rapid filling, pneumatic blending, swelling, temperature, eccentric
filling, vibration, gas pressure, suction) — see
[[as3774-special-service-loads]] and [[as3774-environmental-and-accidental-loads]].

### Initial wall friction and vertical wall force (Cl 6.2.2)

`[code]` p_qi = γ r_c c_z (Eq 6.2.2.1), using upper μ, upper k_u, lower φ_i,
z_o = r_c/(μ k_u). Squat container tractions follow the same linear ramp
(Eq 6.2.2.2). Vertical wall load per unit circumference
N_zi = γ r_c (z − z_o c_z) (Eq 6.2.2.3(1)); for squat containers
N_zi = ∫p_qi dz (Eq 6.2.2.3(2)).

### Initial forces on closures (Cl 6.2.3)

`[code]` Mean vertical pressure on any horizontal plane
p_vi = γ r_c c_z/(μ k_l) for A2/A3 and γ z for A1 (Eq 6.2.3.1(1),(2)), using
lower k_l, lower μ, upper φ_i (the clause defines φ_i upper, φ_w lower).
Flat bottoms: circular p_vix = 1.25 p_vi [1 − 1.6 (x/d_c)²]; horizontal shear
p_Six = 0.3 p_vi [2x/d_c − (2x/d_c)²]; rectangular
p_vix = 1.36 p_vi [1 − 1.6 (x/b)² − (y/l)²] with shears 0.3 p_vi [2x/b − (2x/b)²]
and 0.3 p_vi [2y/l − (2y/l)²] (Eq 6.2.3.2(1)-(5)).

![[as3774-fig-6.4-pressures-on-flat-bottomed-bases.png]]
*Figure 6.4 — pressures on flat-bottom container bases: vertical pressure distribution p_vix and horizontal base traction p_Six.*

`[derived]` Transcribed from the printed page; Eq 6.2.3.2(3) as printed has
the bracket "(x/b)² − (y/l)²" with a single square on y/l — confirm the exact
bracket grouping against the source page before use in a calculation.

### Flow loads on vertical walls (Cl 6.3.1-6.3.4)

`[code]` p_nf = c_nf p_ni (Eq 6.3.2.1(1)); c_nf is the larger of
[7.6 (h_b/d_c)^n − 6.4] c_c and 1.2 c_c, with n = 0.06; c_c = 1.0 axisymmetric
(C1), 1.2 planar (C2). Figure 6.7 gives c_nf vs aspect ratio h_b/d_c.

![[as3774-fig-6.7-normal-wall-pressure-multiplier-cnf.png]]
*Figure 6.7 — normal wall pressure multiplier c_nf for vertical walls (axisymmetric and planar flow; cut-offs 1.2 and 1.44).*

`[code]` **Funnel flow containers (Cl 6.3.2.2)**: the multiplier may be reduced
below the effective transition. The lower-bound transition height above the
outlet is h_t = 0.4 d_c tan φ_i; at the transition the multiplier is c_nf, at
the outlet 1.2 c_c, with linear interpolation. **Severe external vibration
(Cl 6.3.2.3)**: where accelerations exceed 0.05 g, the vertical-wall friction
coefficient is taken as 0.6 μ unless tests justify more.

`[code]` Flow traction p_qf = c_qf p_qi, c_qf = 1.2 axisymmetric, 1.4 planar;
vertical wall load N_zf = c_qf N_zi; strongly cohesive solids: N_zf increased by
a further 30 % (Cl 6.3.3). Flat-bottom vertical pressure at flow is the smaller
of c_vf p_vi (with z = h_b) and γ z (Eq 6.3.4(1),(2)), with c_vf from Table 3.1,
or for unlisted materials 1.0 + tan φ_i (agricultural grains/flours) or
1.0 + 0.4 tan φ_i (other granular) (Eq 6.3.4(3),(4)).

### Eccentric filling of squat or medium containers (Cl 6.4)

`[code]` Initial pressure p_ni = γ r_c c_ze/μ (Eq 6.4.1(1)) with eccentric
Janssen function c_ze = 1 − e^(−(z − z_e)/z_o) using upper k_u; the effective
surface origin is raised by
h_o = (h_s/4)(1 − r_e/(2 r_c))(1 − r_c/d_c) (Eq 6.4.1(2)) and z_e varies around the
circumference as z_e = r_e tan φ_r (1 − cos β) (Eq 6.4.1(3), circular
containers; β from point H, the highest wall contact). No special calculation
is required for eccentric filling of tall (A3) containers. Traction
p_qie = γ r_c c_ze (Eq 6.4.2).

![[as3774-fig-6.11-eccentric-filling-squat-container.png]]
*Figure 6.11 — eccentric filling of a squat container (r_e, h_s, z_e, points H and P).*

`[derived]` The clause text says the h_o expression in Eq 6.4.1(2) was
typeset with nested brackets; reading as above matches the printed page but
the nesting should be verified before use.

## Worked reference

None yet.

## Contradictions

None recorded. `[derived]` Printed cross-reference oddities: Cl 6.2.1.2 and
6.2.2.2 cite "Clause 2.12" for h_o (the definition is Cl 2.2.2); the definition
of p_vi in Cl 6.2.3.1 lists "φ_i upper/φ_w lower" while Cl 6.2.2.1 uses
"φ_i lower" for friction — these are different load effects (Table 6.1), not a
conflict.

## Related

- [[as-3774-1996-loads-on-bulk-solids-containers]]
- [[as3774-container-classification-and-bulk-solid-properties]]
- [[as3774-hopper-pressures-and-feeder-loads]]
- [[as3774-eccentric-filling-and-discharge-loads]]
- [[as3774-load-combinations-and-factors]]

## Sources

- `raw/0-standards/AS 3774-reprint.pdf` — AS 3774—1996 incl. Amdt 1, 2 (1998), Cl 6.1-6.4.
