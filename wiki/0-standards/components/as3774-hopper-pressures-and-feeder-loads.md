---
title: AS 3774 hopper wall pressures, gate/feeder loads and internal elements
category: 0-standards
tags: [as3774, hopper, feeder, gate, wall-pressure, impact]
standards: [AS 3774:1996 Cl 6.2.3.3-6.2.3.6, AS 3774:1996 Cl 6.3.5-6.3.7, AS 3774:1996 Cl 6.6, AS 3774:1996 Cl 6.10, AS 3774:1996 Cl 6.11]
status: draft
reviewed: 2026-10-02
---

# AS 3774 hopper pressures, gate/feeder loads and internal elements

> Scope: AS 3774:1996 initial and flow pressures on hopper walls (conical,
> pyramidal, wedge/slot), dumping impact, gate/feeder vertical and horizontal
> loads, loads on internal structural elements, and loads to supports.
> Cylinder-wall loads: [[as3774-silo-wall-pressures-initial-and-flow]].

## Summary

`[code]` Hopper design uses the transition (cylinder-to-hopper) mean vertical
pressure p_vit from Eq 6.2.3.1(1) at z = h_o + h_c, with φ_i upper and φ_w
lower (Table 6.1). For a pure hopper container p_vit = 0 at height h_o above the
highest contact (Cl 6.2.3.3, 6.3.5).

## Detail

### Initial hopper pressures (Cl 6.2.3.3-6.2.3.6)

`[code]` p_nhi = k_h (γ z_h + p_vit) (Eq 6.2.3.3(1)) at depth z_h below the
transition, and p_nti = k_h p_vit just below it (Eq 6.2.3.3(2)); k_h = tan α /
(tan α + μ_h) or from Figure 6.6. Frictional traction p_qhi = μ_h p_nhi
(Eq 6.2.3.4), used for liners and fixings.

![[as3774-fig-6.5-initial-wall-pressure-hopper-surcharge.png]]
*Figure 6.5 — distributions of initial wall pressure in a hopper with surcharge (p_ni upper body, p_nhi, p_qhi, z_g, z_h, h_h).*

![[as3774-fig-6.6-initial-hopper-pressure-ratio-kh.png]]
*Figure 6.6 — initial hopper normal pressure ratio k_h vs half-angle α for φ_w = 0° to 50°.*

`[code]` **Dumping impact (Cl 6.2.3.5)**: where hard lumpy material is dumped
in discrete volumes, hopper wall pressures are multiplied by Table 6.5
(concrete 1.10-1.40; steel 1.35-1.75, rising with dumped/hopper volume ratio
< 0.2, 0.3, 0.4, 0.5-1.0). Where too little material cushions the impact, a
local force F_h = 0.3 m_1 v_E (m_1 in tonnes, v_E from Eq 6.2.1.7(2)) acts on
area A_w = 0.30 V_D^0.67 and is not applied at all points simultaneously.

![[as3774-table-6.5-hopper-impact-load-coefficient.png]]
*Table 6.5 — impact load coefficient for hopper by construction and dumped-volume ratio.*

`[code]` **End walls of slot hopper (Cl 6.2.3.6)**: p_nhi = 0.3(1 + k_m)
(γ z_h + p_vi), k_m the smaller of 0.5[0.5/(1 + μ cot α) + 0.4] and 1.0.

### Flow pressures on hoppers (Cl 6.3.5-6.3.7)

`[code]` p_nhf = k_hf p_vhf (Eq 6.3.5(1)); k_hf = [1 + sin φ_i cos 2η] /
[1 − sin φ_i cos(2(α + η))] (Fig 6.10), η = 0.5[φ_w + sin⁻¹(sin φ_w/sin φ_i)]
≤ 90°; p_vhf is the flow-state vertical pressure
γ(h_h − z_h)/(j − 1) + [p_vit − γ h_h/(j − 1)] ((h_h − z_h)/h_h)^j; hopper
exponent j = c_h[k_hf(μ_h cot α + 1) − 1], c_h = 2 conical/pyramidal (H1),
1 wedge/slot (H2). Uses lower φ_i, lower φ_w, lower μ_h. Frictional traction
p_qhf = μ_h p_nhf with **upper** μ_h (Cl 6.3.6). Slot hopper end walls:
p_nhf = 0.3(1 + k_hf) p_vhf (Cl 6.3.7). For hopper containers substitute z for
z_h and h_k for h_h (Fig 6.9).

![[as3774-fig-6.8-hopper-wall-pressure-during-flow-surcharge.png]]
*Figure 6.8 — distributions of wall pressure in a hopper with surcharge during flow (p_ni, p_nf, p_nhf, p_qhf).*

![[as3774-fig-6.9-hopper-wall-pressure-during-flow.png]]
*Figure 6.9 — normal wall pressure in hopper containers during flow (p_vit = 0, h_k, z_g).*

![[as3774-fig-6.10-hopper-normal-pressure-ratio-khf.png]]
*Figure 6.10 — normal pressure ratio k_hf for hoppers during flow (φ_i = 30°, 40°, 50°, 60°).*

### Gates and feeders (Cl 6.6)

`[code]` Initial vertical pressure at the gate/feeder is the larger of
p_g = γ(h_h − z_g)/(j − 1) + [p_vit − γ h_h/(j − 1)]((h_h − z_g)/h_h)^j and p_nv
(Eq 6.6.1(1)); j = 0.1 very incompressible solids over stiff feeders, 0.45
moderately compressible over flexible feeders, 0.9 very compressible over soft
feeders. Gate load F_g = p_g A_D + W_g (Eq 6.6.1(2)).
`[code]` Large drop/rapid fill: deceleration force F_k = γ q_f v_E/3600
(kN; q_f m³/h), spread over the wetted hopper area: conical
p_nv = F_k / [π h_k² tan α (μ_h + tan α)]; wedge
p_nv = F_k / [2 h_k l_h (μ_h + tan α)]; p_qv = μ_h p_nv (Eq 6.6.2(1)-(5)).
`[code]` Unattached feeder: horizontal force H_1 = p_g A_D sin φ_i + W_g a/g
(Eq 6.6.3).

`[derived]` The wedge-hopper equation is numbered "6.6.4(4)" on the printed
page; it belongs to Cl 6.6.2 (Eq 6.6.2(4)).

### Internal elements and supports (Cl 6.10-6.11)

`[code]` Internal structural elements above the transition use **flow**
pressures; below it the initial pressures may be substituted for flow pressures.
Vertical pressure p_v,str = c_vf p_vbf (inside the apex pile above first wall
contact p_v,str = γ z_str); horizontal p_n,str = p_nf; frictional traction
p_q,str = p_qf (all at element height z). Vertical force
F_str = 2 A_str p_v,str + ∫p_q,str l_str dz (Eq 6.10.5); friction may act in
the same direction on both inside and outside of a tube-like element.
Loads to supports use **upper-bound density** and **no flow multipliers**
(Cl 6.11).

`[derived]` The printed Eq 6.10.5 lists the factor "2 A_str" — the source gives
no explanation of the 2; do not use it without checking the Commentary
(AS 3774 Supplement 1, not in the wiki).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as-3774-1996-loads-on-bulk-solids-containers]]
- [[as3774-silo-wall-pressures-initial-and-flow]]
- [[as3774-eccentric-filling-and-discharge-loads]]
- [[as3774-special-service-loads]]
- [[as3774-load-combinations-and-factors]]

## Sources

- `raw/0-standards/AS 3774-reprint.pdf` — AS 3774—1996 incl. Amdt 1, 2 (1998), Cl 6.2.3.3-6.2.3.6, 6.3.5-6.3.7, 6.6, 6.10-6.11.
