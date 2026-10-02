---
title: ACI 318M-19 strength evaluation of existing structures (analysis and load testing)
category: 2-concrete
tags: [aci, existing-structures, strength-evaluation, load-test, cores]
standards: [ACI 318M-19 Cl 27.1, ACI 318M-19 Cl 27.2, ACI 318M-19 Cl 27.3, ACI 318M-19 Cl 27.4, ACI 318M-19 Cl 27.5, ACI 318M-19 Cl 27.6]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 strength evaluation of existing structures

> Scope: ACI 318M-19 Chapter 27 in full. **ACI 318M-19 page, kept separate from the AS 3600:2018
> pages** (see [[aci-318m-19-building-code-concrete]]). Typical trigger: failed core tests under
> [[aci318-concrete-acceptance-testing-and-inspection]] (Cl 26.12.6.1(g)).

## Summary

`[code]` Where there is doubt that part or all of a structure meets the Code and it stays in
service, a strength evaluation is carried out as required by the licensed design professional or
building official (Cl 27.2.1). If the effect of a deficiency is well understood and dimensions and
material properties can be measured, an **analytical evaluation** is allowed (Cl 27.2.2, 27.3); if
not, a **load test** is required (Cl 27.2.3, 27.4). Where doubt concerns deterioration and the load
test is passed, the structure may stay in service for a period set by the design professional, with
periodic re-evaluation if deemed necessary (Cl 27.2.4). A structure that fails may be used at a lower
load rating, based on analysis or test results and if the building official approves (Cl 27.2.5).

## Detail

### Analytical evaluation (Cl 27.3)

`[code]` As-built dimensions are field-verified at critical sections; reinforcement location and size are
measured, though drawings may be used if verified at representative locations (Cl 27.3.1.1–27.3.1.2). If
required, an equivalent `f'c` is estimated from original cylinder data, core tests (ASTM C42), or both,
representative of the area of concern (Cl 27.3.1.3–27.3.1.4). Reinforcement properties may come from tensile
tests of representative samples (Cl 27.3.1.5).

With dimensions, reinforcement and material properties established per Cl 27.3.1, φ may exceed the design
values elsewhere in the Code, within Table 27.3.2.1 (Cl 27.3.2.1):

![[aci318-table-27.3.2.1-max-permissible-phi-strength-evaluation.png]]
*Table 27.3.2.1 — maximum permissible φ: tension-controlled 1.0 (all cases); compression-controlled 0.9
with spirals (satisfying Cl 10.7.6.3, 20.2.2, 25.7.3) or 0.8 other transverse steel; shear and/or torsion
0.8; bearing 0.8 (ACI 318M-19).* Compare design φ values in [[aci318-strength-reduction-factors]].

### Load-test general requirements (Cl 27.4)

`[code]` Tests are monotonic (Cl 27.5) or cyclic (Cl 27.6) (Cl 27.4.1) and are run safely for life and
structure, with safety measures not affecting results (Cl 27.4.2–27.4.3). The tested part is at least
**56 days** old unless all parties agree to test earlier (Cl 27.4.4). A precast member to be made composite
may be tested alone in flexure if calculations show it will not fail by compression or buckling and the
test load produces the same total tensile steel force as the composite loading (Cl 27.4.5).

Test load arrangement maximises load effects in the critical regions (Cl 27.4.6.1). The total test load `T_t`,
including dead load already in place, is at least the greatest of (Cl 27.4.6.2):

![[aci318-eq-27.4.6.2-total-test-load.png]]
*Eq. 27.4.6.2a–c — `T_t = 1.0D_w + 1.1D_s + 1.6L + 0.5(L_r or S or R)`; `T_t = 1.0D_w + 1.1D_s + 1.0L +
1.6(L_r or S or R)`; `T_t = 1.3(D_w + D_s)` (ACI 318M-19).* The symbols `D_w` and `D_s` are the dead load
of the structure's self-weight and the superimposed dead load respectively **(the definition is not
restated in the clauses read; confirm in Chapter 2 before use)** `[derived]`. `L` may be reduced per the general building code (Cl 27.4.6.3). The live-load factor
in Eq. 27.4.6.2b may be reduced to **0.5**, except for parking structures, public-assembly areas, and where
`L > 4.8 kN/m²` (Cl 27.4.6.4). Normalweight concrete density is taken as **2400 kg/m³** unless documented
(Cl 27.4.6.5).

### Monotonic load test (Cl 27.5)

`[code]` **Application:** `T_t` is applied in at least four approximately equal increments, uniformly
distributed without arching in the apparatus, held for at least **24 hours** unless distress appears, then
removed as soon as practical (Cl 27.5.1.1–27.5.1.4). **Measurements:** deflection, strain, slip and crack width
at points of maximum response; initial readings within 1 hour before the first increment; a set after each
increment and after 24 hours of `T_t`; a final set **24 hours after removal** (Cl 27.5.2).

**Acceptance (Cl 27.5.3).** `[code]` No spalling, crushing or other failure evidence; no cracks indicating
imminent shear failure; in regions without transverse reinforcement, inclined structural cracks with
horizontal projection greater than the member depth are evaluated; short inclined cracks or horizontal cracks
along reinforcement at anchorages and laps are evaluated (Cl 27.5.3.1–27.5.3.4). Residual deflection must satisfy:

![[aci318-eq-27.5.3.5-residual-deflection-first-test.png]]
*Eq. 27.5.3.5 — `Δ_r ≤ Δ_1/4` (ACI 318M-19).*

If the maximum test deflection `Δ_1` does not exceed the larger of **1.3 mm** and `ℓ_t/2000`, the residual
requirement is waived (Cl 27.5.3.6). If neither is met, the test may be repeated no earlier than **72 hours**
after load removal, with acceptance if:

![[aci318-eq-27.5.3.8-residual-deflection-second-test.png]]
*Eq. 27.5.3.8 — `Δ_r2 ≤ Δ_2/5` (ACI 318M-19).*

### Cyclic load test (Cl 27.6)

`[code]` A cyclic test per ACI 437.2M may be used, with acceptance criteria and retest rules from that document;
the ACI 437.2M maximum-deflection limit (`ℓ_t/180`) that precludes retesting may be waived (Cl 27.6.1–27.6.3).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[aci-318m-19-building-code-concrete]] — source register.
- [[aci318-concrete-acceptance-testing-and-inspection]] — Cl 26.12.6 core investigation leading here.
- [[aci318-strength-reduction-factors]] — design φ values that Table 27.3.2.1 relaxes.
- [[aci318-loads-and-load-combinations]] — dead/live load factors comparison.
- [[aci318-serviceability-deflection-and-cracking]] — deflection background.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 27 Cl 27.1–27.6 (printed pp. 559–565).
