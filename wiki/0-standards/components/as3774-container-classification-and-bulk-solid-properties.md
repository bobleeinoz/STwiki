---
title: AS 3774 container classification, geometry and bulk solid properties
category: 0-standards
tags: [as3774, silo, bin, hopper, bulk-solids, flow-mode, wall-friction]
standards: [AS 3774:1996 Cl 1.3, AS 3774:1996 Section 2, AS 3774:1996 Section 3, AS 3774:1996 App B, AS 3774:1996 App C]
status: draft
reviewed: 2026-10-02
---

# AS 3774 container classification, geometry and bulk solid properties

> Scope: AS 3774:1996 Sections 2-3 and Appendices B-C — the A/B/C/D/E/F/G/H/J
> classification of bulk solids containers, geometric parameters (h_b, d_c,
> r_c, h_o), bulk solid property selection (γ, φ_i, φ_w, φ_r), wall roughness
> D1-D4, characteristic values, and testing guidance. Register page:
> [[as-3774-1996-loads-on-bulk-solids-containers]].

## Summary

`[code]` The Standard applies to bins, silos, bunkers and dump hoppers for
mass storage of **granular** bulk solids; it does **not** apply to silage
containers or containers whose parameters fall outside Section 2 (AS 3774:1996
Cl 1.1). `[code]` Every container is classified by nine characteristics
(Cl 2.1.1): geometry (A), flow mode (B), flow geometry (C), wall roughness (D),
hoop flexibility (E), vertical continuity (F), cross-section (G), outlet
configuration (H) and flow promotion (J). The classification selects which
load equations apply in [[as3774-silo-wall-pressures-initial-and-flow]].

`[code]` Two representative values — an **upper** and a **lower
characteristic value** (95 % / 5 % probability of not being exceeded,
Cl 1.3.27, 1.3.19) — are required for every property, and the one that
maximises the load effect under consideration is used (Cl 3.4.1, 3.5).

## Detail

### Classification (Cl 2.1)

`[code]` **Geometry (Cl 2.1.2)** by effective height / largest inscribed
diameter: A1 squat h_b/d_c < 1.0; A2 medium 1.0 ≤ h_b/d_c ≤ 3.0; A3 tall
> 3.0.

![[as3774-fig-2.1-container-geometries.png]]
*Figure 2.1 — container geometries: flat-bottom, funnel-flow hopper and mass-flow hopper containers at A1/A2/A3, with effective transition (ET), primary/secondary flow zones and dead zone (AS 3774:1996).*

`[code]` **Flow mode (Cl 2.1.3)**: B1 mass flow, B2 funnel flow, B3 pipe flow,
B4 expanded flow, B5 eccentric flow. The mode descriptions are approximations
of real flow, and the possibility of mode change with wall roughness or
material change must be considered.

![[as3774-fig-2.2-symmetrical-flow-modes.png]]
*Figure 2.2 — symmetrical flow modes B1-B4.*

![[as3774-fig-2.3-eccentric-flow-channel-configurations.png]]
*Figure 2.3 — eccentric flow channel configurations (type B5): semi-mass, pipe, segregation, unsymmetrical hopper.*

`[code]` Figure 2.4 gives preliminary boundaries between mass and funnel flow
as a function of hopper half-angle α and wall friction μ, for conical and wedge
hoppers. Because of material and roughness uncertainty the plots show an upper
and lower bound; for **reliable mass flow the half-angle is chosen using the
lower-bound curve** (Cl 2.1.3).

![[as3774-fig-2.4-mass-flow-funnel-flow-boundaries.png]]
*Figure 2.4 — boundaries between mass flow and funnel flow (conical and wedge hoppers).*

`[code]` **Flow geometry (Cl 2.1.4)**: C1 axisymmetric, C2 planar, C3 eccentric
path, C4 eccentric free surface in squat containers.

![[as3774-fig-2.5-unsymmetrical-conditions-squat-containers.png]]
*Figure 2.5 — unsymmetrical conditions in squat containers (eccentric filling, eccentric cleanout, diametral trough slot outlet).*

`[code]` **Wall roughness (Cl 2.1.5, Table 2.1)**: D1 polished (0.01-1 µm),
D2 smooth (1-10 µm), D3 rough (10-1000 µm), D4 corrugated (> 1000 µm,
horizontal ribs). Roughness is a variable over the design life: design for the
widest range expected; D1 may deteriorate to D3 but D3 cannot deteriorate to
D4; polishing D4 need not be considered; carbon steel in moisture can span
D1-D3.

![[as3774-table-2.1-surface-roughness-designation.png]]
*Table 2.1 — designation of surface roughness.*

`[code]` **Hoop flexibility (Cl 2.1.6)**: E1 rigid d_c/t < 100; E2 semirigid
100-500; E3 flexible > 500 or metal square/rectangular. **Vertical continuity
(Cl 2.1.7)**: F1 two-way continuous (fully welded steel; reinforced/prestressed
concrete with ≥ 0.35 % vertical steel); F2 discontinuous (segmental concrete,
horizontally corrugated metal). **Outlets (Cl 2.1.9)**: H1 central, H2 slot,
H3 eccentric, H4 wall outlet — H3/H4 give eccentric flow and non-uniform loads.
**Flow promotion (Cl 2.1.10)**: J1 gravity, J2 vibrators, J3 air induction,
J4 impulsive devices, J5 combined.

`[code]` **Cross-section shapes (Cl 2.1.8, Table 2.2)**: G1-G7, each with a
characteristic dimension r_c used in every pressure equation (e.g. 0.25 d_c for
circular/square; rectangular r_c depends on l/b and on which wall is being
assessed; annular 0.35 d_a).

![[as3774-table-2.2-cross-sectional-shape-designation.png]]
*Table 2.2 — designation of cross-sectional shapes and characteristic dimension r_c.*

### Geometric parameters and capacity (Cl 2.2-2.3)

`[code]` The toe of the filling surface is at the top of the vertical section.
The origin of the vertical coordinate z is point F, at height h_o above the
highest bulk-solid/wall contact: h_o = 0 level surface; h_s/3 conical surface;
h_s/2 long prismatic pile, with h_s = (d_c/2) tan φ_r (Cl 2.2.2). Capacity is
stated as "level full" or "peaked", open- or tight-eave; nominal mass capacity
uses the **average** bulk density of Table 3.1 (Cl 2.3).

![[as3774-fig-2.6-characteristic-geometric-parameters.png]]
*Figure 2.6 — characteristic geometric parameters (h_b, h_c, h_s, h_o, α, d_c, φ_r, point F).*

### Bulk solid properties (Section 3)

`[code]` Size classes: powder < 0.15 mm, fine grain < 3 mm, coarse grain
< 12 mm, lumpy > 12 mm, irregular (Cl 3.1). Properties for load calculation are
γ, φ_i, φ_w and φ_r (Cl 3.2); also consider flowability, abrasiveness,
corrosiveness, dust/gas explosion susceptibility, volumetric stability and
degradation (Cl 3.3). Characteristic values come from (a) agreement between
parties, (b) Table 3.1 or (c) test data using Appendix B procedure B2
(Cl 3.4.1).

![[as3774-table-3.1-bulk-solids-characteristic-properties.png]]
*Table 3.1 — characteristic values (mean/upper γ; φ_r; lower/upper φ_i; lower/upper φ_w for D1-D3; vertical pressure multiplier c_vf) for 22 materials incl. coal, coke, cement, clinker, fly ash, iron ore, lime, limestone powder, phosphate rock, sand, slag, sugar, grains.*

`[code]` Selection rules: loading calcs use the **upper** characteristic unit
weight, volume estimates the average (Cl 3.4.2); φ_i and φ_w take upper or
lower values by application (Cl 3.4.3-3.4.4, Table 6.1); φ_r is the mean
(Cl 3.4.5). For profiled sheeting with corrugations parallel to flow, the upper
wall friction coefficient is the greater of c_p × measured flat-sheet value and
the Table 3.1 upper value, with c_p = profile contact circumference/nominal
pitch (Cl 3.4.4). Upper-bound solid modulus E_s = χ p_vi (Eq 3.4.6(1)) with
χ = 3γ^1.5 (γ in kN/m³) absent tests, or 70 (dry agricultural grains), 100
(small mineral particles), 150 (very hard mineral particles) (Cl 3.4.6).
Characteristic values must be combined to give the **maximum calculated load
effect** (Cl 3.5); Cl 6.1.5 additionally requires a single consistent set per
load case and φ_w ≤ φ_i.

### Appendix B — normative property guidance

`[code]` Table B1 gives descriptor codes (size S1-S5, flowability F1-F4,
abrasiveness A1-A3, corrosiveness C1-C3, dust D1-D2); Table B2 lists typical
codes per material; Table B3 typical coefficients of variation δ.
When a material is unlisted: x₀.₉₅ = x̄(1.0 + 1.89δ) and x₀.₀₅ = x̄(0.2 − 0.3 ln δ)
for 0.1 < δ < 1.0 (Eq B2(1), B2(2)). Typical δ: unit weight ≈ 0.10, φ_i
0.1-0.25, φ_w 0.10-0.20 (Cl B2). For D4 wall friction use
μ_eff = u₂ μ_i + u₃ μ_w, u₂ = y₁/(x₂+y₁), u₃ = x₂/(x₂+y₁) (Eq B3, Fig B1); for
coarse spherical grains on D3/D4 walls use u₂ = 1, u₃ = 0 (Cl B4).

![[as3774-table-B1-bulk-solids-material-characteristics.png]]
*Table B1 — characteristics of bulk solids materials.*

![[as3774-table-B2-typical-bulk-solids-properties.png]]
*Table B2 — typical properties of bulk solids (size, flowability, abrasiveness, corrosiveness, dust).*

![[as3774-table-B3-coefficient-of-variation.png]]
*Table B3 — typical coefficient of variation of φ_i and φ_w (D1-D3).*

![[as3774-fig-B1-profile-sheeting-dimensions.png]]
*Figure B1 — profile sheeting dimensions x₂, y₁ for u₂, u₃.*

`[derived]` Table B3 lists δ = 1.10 for cement on D1 walls; this is outside the
0.1-1.0 validity range of Eq B2(1)-(2) and is probably a misprint for 0.10.
Confirm against another copy before using.

### Appendix C — testing (normative, descriptive)

`[code]` Test method detail is outside the Standard's scope, but guidance is
given: samples must span extremes of moisture, particle size (smallest for
flow, largest for wall friction), fresh/aged, temperature/vibration and
run-of-mine conditions; shear testing normally cuts out particles > ~3 mm;
the Jenike cell is recommended over annular and Peschl cells (Cl C1).
Flow data derive from bulk density variation, instantaneous yield loci, wall
yield loci and poured angle of repose. Factors modifying flow properties are
size/distribution, moisture (flowability minimum at ~70-90 % saturation),
aeration/fluidisation, cohesion, vibration, slip-stick and others (C2.1-C2.7).
Measurement scatter is at best 5 % and 10 % or more for non-uniform materials,
so upper and lower bounds are adopted (Cl C3).

![[as3774-fig-C1-yield-loci-determination.png]]
*Figure C1 — determination of yield loci (instantaneous, effective, valid range, time, wall).*

![[as3774-fig-C2-flow-function-typical-plot.png]]
*Figure C2 — flow function, typical plot.*

![[as3774-fig-C3-bulk-density-typical-plot.png]]
*Figure C3 — bulk density vs consolidation stress, typical plot.*

`[derived]` Table 3.1 is a 1996 judgement-based table (Cl B2). For a real
mining material (run-of-mine ore, coal of a given rank/moisture) a
shear-cell test per Appendix C is the defensible basis; Table 3.1 is
preliminary only.

## Worked reference

None yet — no numeric worked example has been built on this page.

## Contradictions

None recorded against other wiki pages. Internal note: Cl 6.2.1.2 refers to
"Clause 2.12" for h_o; the definition is Cl 2.2.2 (see
[[as3774-silo-wall-pressures-initial-and-flow]]).

## Related

- [[as-3774-1996-loads-on-bulk-solids-containers]] — source register.
- [[as3774-silo-wall-pressures-initial-and-flow]] — uses the classification and property selection.
- [[as3774-hopper-pressures-and-feeder-loads]]
- [[as3774-load-combinations-and-factors]]

## Sources

- `raw/0-standards/AS 3774-reprint.pdf` — AS 3774—1996 (second edition, incorporating Amdt 1 and 2, 1998), Sections 1-3, Appendices B and C.
