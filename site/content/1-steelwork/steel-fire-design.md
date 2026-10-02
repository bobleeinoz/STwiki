---
title: Fire design — period of structural adequacy, limiting temperature, protected and unprotected members
category: 1-steelwork
tags: [fire, fire-resistance-level, FRL, period-of-structural-adequacy, PSA, limiting-temperature, three-sided-exposure, web-penetrations]
standards: [AS 4100:2020 Section 12]
status: draft
reviewed: 2026-09-13
---

# Fire design

> Scope: AS 4100:2020 Section 12 — determining a steel member's period of
> structural adequacy (PSA) against its required fire-resistance level
> (FRL): limiting steel temperature, variation of yield stress/modulus with
> temperature, time-to-limiting-temperature for protected members (test
> regression / single test) and unprotected members (closed-form), PSA from
> a single test, three-sided fire exposure, and special considerations for
> connections and web penetrations.

## Summary

`[code]` Requirement (Cl 12.1): protected members — fire protection
thickness `h_i` ≥ that giving PSA = required FRL; unprotected members —
exposed surface-area-to-mass ratio `k_sm` ≤ that giving PSA = required FRL.
PSA is determined per Cl 12.3, using the Cl 12.4 temperature-dependent
mechanical properties.

`[code]` Limiting steel temperature: `T_l = 905 − 690 r_f` (Cl 12.5), where
`r_f` = ratio of the fire-limit-state design action (AS/NZS 1170.0
Section 4) to the room-temperature design capacity `φR_u`.

## Detail

### Definitions (Cl 12.2)

`[code]`
- **Exposed surface area to mass ratio** `k_sm`: ratio of fire-exposed
  surface area to steel mass (for protected members, use the fire
  protection material's internal surface area).
- **Three-sided fire exposure**: member incorporated in or in contact with
  a concrete/masonry floor or wall (a member with more than one face in
  contact may still be treated as three-sided); considered separately
  unless Cl 12.9 groups it with others.
- **Four-sided fire exposure**: member exposed to fire on all sides.
- **Fire protection system**: the protection material and its attachment
  method.
- **Fire-resistance level (FRL)**: required fire-resistance grading period
  for structural adequacy only, minutes, from the standard fire test.
- **Period of structural adequacy (PSA)**: time `t` (minutes) for the
  member to reach the structural-adequacy limit state in the standard fire
  test (AS 1530.4).
- **Prototype**: test specimen representing a member + fire protection
  system, subjected to the standard fire test.
- **Standard fire test**: per AS 1530.4.
- **Stickability**: the fire protection system's ability to stay in place
  as the member deflects under load during the test (AS 1530.4).
- **Structural adequacy**: ability to carry the AS 1530.4 test load during
  the test.

### Section k_sm tables and exposure cases (practice cross-check)

`[practice]` The ASI *Design Capacity Tables for Structural Steel, Vol 1:
Open Sections* (DCT/V1/03-1999, Section 3.3) tabulates `k_sm` for every
open section, in six exposure cases per I, C (channel), angle and T
cross-section shape — three 4-sided cases (total-perimeter, profile- or
box-protected, with/without a 25 mm air gap) and three 3-sided cases (top
flange excluded, same three protection variants). For **unprotected**
4-sided/3-sided members, use Case 1 / Case 4 respectively. This is a
pre-computed lookup for the `k_sm` this page's Cl 12.6/12.7 equations need
as an input — it does not change the AS 4100:2020 method above. See
[[asi-design-capacity-tables-vol1-open-sections]] for the source register.

![[dct-fig-3.1-fire-exposure-cases.png]]
*DCT Vol 1 Figure 3.1 — the six cases used to tabulate k_sm per section:
Cases 1–3 total-perimeter (4-sided) exposure, Cases 4–6 top-flange-excluded
(3-sided) exposure, each with total-perimeter / box-protected-no-gap /
box-protected-25mm-gap variants (source: DCT/V1/03-1999, p. 3-5).*

### Determination of PSA (Cl 12.3)

`[code]` Three methods: (a) by calculation — (i) limiting temperature `T_l`
(Cl 12.5), then (ii) PSA = time to reach `T_l` (Cl 12.6 protected /
Cl 12.7 unprotected); (b) direct application of a single test (Cl 12.8);
or (c) structural analysis (Section 4) using temperature-dependent
properties (Cl 12.4), with steel temperature from a rational,
test-confirmed method.

### Variation of mechanical properties with temperature (Cl 12.4)

`[code]` **Yield stress** (12.4.1):

`f_y(T)/f_y(20) = 1.0` for `0 °C < T ≤ 215 °C`

`f_y(T)/f_y(20) = (905 − T)/690` for `215 °C < T ≤ 905 °C`

`[code]` **Modulus of elasticity and shear modulus** (12.4.2):

`E(T)/E(20) = 1.0 + T / {2000 ln(T/1100)}` for `0 °C < T ≤ 600 °C`

`E(T)/E(20) = [690(1 − T/1000)] / (T − 53.5)` for `600 °C < T ≤ 1000 °C`

`G(T) = E(T) / [2(1+ν)]`

![[as4100-fig-12.4-property-variation-with-temperature.png]]
*Figure 12.4 — variation of mechanical properties of steel with temperature: Curve 1 yield stress ratio, Curve 2 modulus of elasticity ratio (AS 4100:2020).*

`[code]` **Slenderness at elevated temperature** (12.4.3): in the
`sqrt(f_y/250)`, `sqrt(250/f_y)`, `(f_y/250)`, `(250/f_y)` terms of
Cl 5.2.2, 5.3.2.4, 5.10, 5.11, 5.14, 6.2.3, 6.3.3, 8.4.3.3 and 8.4.6, use
`f_y(20)` (room temperature). **All other** occurrences of `f_y` use
`f_y(T)`. (Note 1: slenderness calculations implicitly assume `E(20)` —
adjusting `f_y` for temperature without adjusting `E` could give unsafe
results, hence the room-temperature `f_y` is retained specifically in the
slenderness terms. Note 2: this simplified method implicitly assumes
`E(T)` and `f_y(T)` reduce by the same fraction with temperature, so
slenderness ratios stay effectively unchanged and only section capacities
reduce with `f_y(T)`.)

### Determination of limiting steel temperature (Cl 12.5)

`[code]` `T_l = 905 − 690 r_f`, `r_f` = ratio of the design action on the
member under the AS/NZS 1170.0 Section 4 fire design load, to the member's
room-temperature design capacity `φR_u`.

### Time to limiting temperature — protected members (Cl 12.6)

`[code]` Methods (12.6.1): from a fire-test series (12.6.2) or a single test
(12.6.3); EN 13381-4/13381-8 assessment methods may also be used. For beams
and all four-sided members, `T_l` = average of all AS 1530.4 thermocouple
readings. For three-sided columns, `T_l` = average of thermocouples on the
face **farthest from the wall** (or use four-sided-condition data at the
same `k_sm`).

`[code]` **Temperature based on a test series — regression analysis**
(12.6.2): interpolate a series of fire tests using least-squares regression:

`t = k_0 + k_1 h_i + k_2(h_i/k_sm) + k_3 T + k_4 h_i T + k_5(h_i T/k_sm) + k_6(T/k_sm)`

`t` = time from test start (min); `k_0`–`k_6` = regression coefficients;
`h_i` = fire protection thickness (mm); `T` = steel temperature (°C,
`> 250 °C`); `k_sm` = exposed surface-area-to-mass ratio (m²/tonne).

`[code]` **Limitations on regression analysis** (12.6.2.3): (a) protection
by board, sprayed blanket or similar insulation, dry density < 1000 kg/m³
(intumescent/ablative coatings also usable if correlation coefficient
> 0.9); (b) all tests use the same fire protection system; (c) all members
share the same fire exposure condition; (d) test series ≥ 9 tests; (e)
unloaded prototypes permitted if stickability is separately demonstrated;
(f) three-sided members must be grouped per Cl 12.9. **Interpolation
only** — the valid window is defined graphically (Figure 12.6.2.3). The
regression equation may transfer between fire protection **systems**
sharing the same material and exposure condition (stickability
demonstrated), and between four-sided prototype data and a three-sided
application (stickability demonstrated for the three-sided case).

![[as4100-fig-12.6.2.3-interpolation-window.png]]
*Figure 12.6.2.3 — definition of window for interpolation limits: fire protection thickness h_i vs exposed surface-area-to-mass ratio k_sm, test data points bound a polygon within which interpolation is valid (AS 4100:2020).*

`[code]` **Temperature based on a single test** (12.6.3): may be used
without modification if: (a) same fire protection system as the prototype;
(b) same fire exposure condition; (c) `h_i` ≥ prototype's; (d) `k_sm` ≤
prototype's; (e) if the prototype was tested unloaded, stickability
separately demonstrated.

### Time to limiting temperature — unprotected members (Cl 12.7)

`[code]` **Three-sided exposure**:

`t = −5.2 + 0.0221T + 0.433T/k_sm`

**Four-sided exposure**:

`t = −4.7 + 0.0263T + 0.213T/k_sm`

Valid for `500 °C ≤ T ≤ 750 °C` and `2 ≤ k_sm ≤ 35 m²/tonne`. Below 500 °C,
linearly interpolate between `t` at 500 °C and `t = 0` at `T = 20 °C`
(initial temperature).

### Determination of PSA from a single test (Cl 12.8)

`[code]` The AS 1530.4 PSA from a single test may be applied unmodified if:
(a) same fire protection system; (b) same fire exposure condition; (c)
`h_i` ≥ prototype's; (d) `k_sm` ≤ prototype's; (e) support conditions the
same and restraints no less favourable; (f) the fire-design-load-to-
capacity ratio ≤ that of the prototype.

### Three-sided fire exposure condition (Cl 12.9)

`[code]` Members are treated as **separate groups** unless: (a) within a
group, concrete density ratio (highest/lowest) ≤ 1.25 **and** effective
thickness `h_e` ratio (largest/smallest) ≤ 1.25 (`h_e` = cross-sectional
area excluding voids, per unit width); (b) rib voids are either **all
open** or **all blocked**. Concrete slabs may incorporate permanent steel
deck formwork.

![[as4100-fig-12.9a-effective-thickness.png]]
![[as4100-fig-12.9b-blocking-rib-voids.png]]
*Figure 12.9 — three-sided fire exposure condition requirements: (a) effective thickness h_e of a ribbed/waffle slab; (b) blocking of rib voids with fire protection material around the top flange (AS 4100:2020).*

### Special considerations (Cl 12.10)

`[code]` **Connections** (12.10.1): protect with the **maximum** thickness
of fire protection material required by any member framing into the
connection to achieve its own FRL; maintain this over all connection
components — bolt heads, welds, splice plates.

`[code]` **Web penetrations** (12.10.2): protection thickness at and
adjacent to a penetration = the **greatest** of: (a) the area above the
penetration as a three-sided condition (`k_sm1`); (b) the area below as a
four-sided condition (`k_sm2`); (c) the section as a whole, three-sided
(`k_sm`). Apply over the full beam depth, extending each side of the
penetration by at least the beam depth and not less than 300 mm.

![[as4100-fig-12.10.2-web-penetrations.png]]
*Figure 12.10.2 — web penetrations: k_sm1 above the penetration (three-sided), k_sm2 below (four-sided), k_sm for the section away from the penetration (AS 4100:2020).*

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[steel-limit-state-design-basis]] — Cl 3.10 routing to this Section;
  AS/NZS 1170.0 Section 4 fire design actions feeding `r_f`.
- [[steel-materials-and-design-strengths]] — room-temperature `f_y`, `E`,
  `G` that the temperature ratios scale.
- [[steel-compression-member-capacity]] / [[steel-beam-section-moment-capacity]]
  — `φR_u` at room temperature, the denominator of `r_f`.
- [[asi-design-capacity-tables-vol1-open-sections]] — per-section `k_sm`
  lookup tables and the six exposure cases (Fig 3.1).
- [[asi-dct-vol1-fire-surface-area-tables]] — full transcription of the
  Part 3.2 surface-area and `k_sm` tables for every open section.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Section 12
  (pp. 162–170). Figures 12.4, 12.6.2.3, 12.9, 12.10.2 reproduced in
  `wiki/1-steelwork/assets/`.
