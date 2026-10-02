---
title: Standard test for evaluation of slip factor
category: 1-steelwork
tags: [slip-factor, friction-connection, test-procedure, bolt-tension, laboratory-test]
standards: [AS 4100:2020 App J]
status: draft
reviewed: 2026-09-13
---

# Standard test for evaluation of slip factor

> Scope: AS 4100:2020 Appendix J (normative) — the standard laboratory test
> for determining a friction-connection slip factor `μ` other than the
> default 0.35 for clean as-rolled surfaces (Cl 9.2.3.2). Specimen geometry,
> instrumentation, loading method, slip-load definition, and the statistical
> reduction to a design `μ`. Primarily of interest to accredited test
> laboratories and to specifiers of non-standard friction-connection
> surface treatments (e.g. specific paint or galvanizing systems, blast
> profiles) rather than day-to-day member design.

## Summary

`[code]` Test ≥ 3 symmetrical double-cover-plated butt-joint specimens (5
preferred), each with 2 bolts, tensile-loaded until slip. The design slip
factor is a **statistically reduced** value:

`μ = k(μ_m − 1.64δ)`

`k = 0.85` (3 specimens) or `0.90` (≥5 specimens); `μ_m` = mean of all
per-bolt slip-factor estimates; `δ` = their standard deviation — i.e. a
lower-5th-percentile-style characteristic value, scaled down further by
`k` for a small sample.

## Detail

### Test specimens (Cl J.1)

`[code]` **Form** (J.1.1): symmetrical double cover-plated butt connection
(Figure J.1), inner plates of equal thickness. Suggested convenient sizing:
M20 bolts, 25 mm inner plates, 12 mm outer (cover) plates.

![[as4100-fig-J.1-standard-test-specimen.png]]
*Figure J.1 — standard test specimen: test section, bolt spacing and plate thickness dimensioned in terms of bolt diameter d_f (AS 4100:2020).*

`[code]` Key dimensions (in terms of `d_f`, minimums shown): test section
length ≥ `200 mm` or `10 d_f`; bolt-to-edge and bolt-to-bolt spacing per the
figure (e.g. `60 mm` or `3 d_f` min. edge distances, `120 mm` or `6 d_f`
min. bolt spacing); cover plate `t ≥ 12 mm` or `(d_f/2 + 2) mm`; inner
plate `t ≥ 25 mm` or `(d_f + 5) mm`. Hole sizes: cover plates 22 mm or
`d_f + 2 mm`; inner plates 23 mm or `d_f + 3 mm`. Inner-plate length/width
outside the test section may be enlarged to suit the test lab. Dimensions
scale for bolts other than M20 (`d_f ≥ 16 mm`).

`[code]` **Assembly and measurement** (J.1.2): neither bolt may bear in the
loading direction; friction-face surface condition must match the intended
field condition (no machining-oil contamination if plate ends are
machined for the grips). Bolts tensioned as in the field, to at least the
Table 15.2.2.2 minimum bolt tension. Bolt extension measured (dial gauge or
displacement transducer, resolution ≤ 0.003 mm) between snug-tight and
final tensioning, immediately before testing (cone-sphere anvil technique
per AS/NZS 1252 proof-load measurement, or equivalent).

`[code]` Bolt tension from a **calibration curve** (load-cell tests of ≥ 3
bolts from the test batch, same grip length, extension-measurement and
tensioning method, calibration based on the mean result; snug-tight =
finger-tight for calibration purposes). **Alternative** without a load
cell: tension bolts to 80–100% of specified proof load, and calculate the
induced tension from:

`N_ti = EΔ×10⁻³ / [a_o/A_o + (a_t + t_n/2)/A_s]` — Eq J.1

`E = 200 000 MPa`; `Δ` = measured total bolt extension, finger-tight to
final tension (mm); `a_o` = unthreaded shank length within the grip
(including washer thickness), mm; `A_o` = plain shank area, mm²; `a_t` =
threaded length within the grip (incl. washer thickness), mm; `t_n` = nut
thickness, mm; `A_s` = tensile stress area (AS 1275), mm². The two bolts in
one specimen need not have identical induced tension.

`[code]` **Number of specimens** (J.1.3): ≥ 3 tested; **5 preferred** as a
practical minimum.

### Instrumentation (Cl J.2)

`[code]` Two pairs of dial gauge micrometers or displacement transducers
(resolution ≤ 0.003 mm), symmetrically placed over gauge lengths of `3d_f`
on each specimen edge, measuring deformation between the inner plates from
the bolt positions to the cover-plate centreline. Each half-joint's
deformation = the mean of its two edge readings (this combines elastic
cover-plate extension and any bolt-position slip). Transducers must be
securely mounted — slip can shock-load them.

![[as4100-fig-J.2-instrumented-test-assembly.png]]
*Figure J.2 — typically instrumented test assembly (AS 4100:2020).*

### Method of testing (Cl J.3)

`[code]` (a) **Loading type**: tensile only. (b) **Loading rate**: up to the
slip load, increments not exceeding the lesser of 25 kN and `0.25 ×` the
slip load computed assuming `μ = 0.35` and the calculated bolt tension;
loading rate ≤ 50 kN/min within an increment (slower preferred); apply the
next increment only after creep from the preceding increment has
effectively ceased. (Note 1: one bolt position may slip into bearing
before the other reaches its own slip load. Note 2: after the first
bolt-position slip is reached, loading rate/increment size are at the
operator's discretion.)

### Slip load (Cl J.4)

`[code]` Slip is usually a well-defined sudden deformation jump (often with
an audible report). Where not clearly defined, use the load corresponding
to a **0.13 mm** slip as the slip load.

### Slip factor (Cl J.5)

`[code]` Design slip factor:

`μ = k(μ_m − 1.64δ)`

`k = 0.85` (3 specimens tested) or `0.90` (≥5 specimens);

`μ_m = (1/2n) Σᵢ₌₁²ⁿ μᵢ`, `μᵢ = (1/2)(V_si/N_ti)`

`δ = sqrt[ (1/(2n−1)) Σᵢ₌₁²ⁿ (μᵢ − μ_m)² ]`

`n` = number of specimens tested (each gives **2** estimates of `μ`, one
per bolt position); `V_si` = measured slip load at bolt position `i`;
`N_ti` = tension induced in bolt `i` (Eq J.1 or calibration curve).
**Exception**: if the calculated `μ` is less than the lowest individual
`μᵢ`, take `μ` = that lowest `μᵢ` instead.

`[derived]` The `1.64δ` term is the standard one-sided 95th-percentile
normal-distribution offset (`z = 1.64`) — i.e. `μ_m − 1.64δ` estimates a
5th-percentile slip factor from the sample, before the further `k = 0.85`
or `0.90` reduction for small-sample statistical uncertainty. This mirrors
the general reliability-based characteristic-value logic used elsewhere in
AS 4100 (e.g. Table 17.5.2's use of more-samples-lower-factor), applied
here specifically to friction-connection surface qualification.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[steel-bolt-design]] — Cl 9.2.3.2, the friction-connection slip factor
  `μ` this test qualifies (default 0.35 for clean as-rolled surfaces).
- [[steel-fabrication-and-erection-requirements]] — Table 15.2.2.2 minimum
  bolt tension, referenced for specimen assembly.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Appendix J
  (pp. 203–206). Figures J.1, J.2 reproduced in `wiki/1-steelwork/assets/`.
