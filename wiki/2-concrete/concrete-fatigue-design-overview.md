---
title: Concrete fatigue design — overview and applicability
category: 2-concrete
tags: [fatigue, applicability]
standards: [AS 3600:2018 Cl 2.4, AS 3600:2018 Cl 18.2, AS 3600:2018 Cl 18.8]
status: draft
reviewed: 2026-09-12
---

# Concrete fatigue design — overview and applicability

> Scope: pointer clause only — when fatigue design applies and where its
> method and capacity factors live. Full method is Section 18, not yet
> ingested.

## Summary

`[code]` Cl 2.4 requires fatigue design to be carried out per Section 18, with
strength reduction factors from Table 2.4 — distinct, lower factors for
concrete and for steel under fatigue loading, each identified by its own
subscripted symbol. See
[[concrete-limit-state-design-basis]] Cl 2.1.5 for the applicability
threshold (foreseen cycles < 10 000 → fatigue need not be considered) and the
restriction on moment redistribution in fatigue analysis.

![[as3600-table-2.4-fatigue-strength-reduction-factors.png]]
*Table 2.4 — strength reduction factors for fatigue, concrete (φc,fat) and
steel (φs,fat) (AS 3600:2018).*

## Detail

`[derived]` This page is intentionally a stub: Section 18 (Design for
Fatigue) covers the actual stress-range and cycle-counting method and has not
been fully ingested (Sections 1–7 only). The two data tables below are added
here as image assets ahead of a full Section 18 ingest pass — extend this
page with the surrounding clause text once that pass happens.

### Maximum compressive stress in concrete (Cl 18.2)

`[code]` Detailed fatigue design for concrete in compression is not required
if the calculated maximum compressive stress `σc,max` under the Cl 2.5.2.3
load combination satisfies `σc,max ≤ 0.45·φc,fat·fc,fat`, where `fc,fat`
scales `f'c` by a concrete-age term and a coefficient of strength gain
`βcc(t0)` read from Table 18.2 by concrete class and age at first cyclic
loading. Otherwise, fatigue is deemed satisfied by a cycle-count check
`log(nsc) ≤ log(N)` against resisting cycles `N` calculated from the maximum
and minimum compressive stress levels (Eq 18.2(3)–(5)); variable-amplitude
loading uses a Palmgren-Miner linear damage sum (Eq 18.2(6)).

![[as3600-table-18.2-coefficient-of-strength-gain.png]]
*Table 18.2 — coefficient of strength gain βcc(t0) by concrete class and age
at first cyclic loading (7/56/90/360 days) (AS 3600:2018).*

### S-N curve parameters for reinforcement and tendons (Cl 18.8)

`[code]` Fatigue resistance of reinforcement and tendons is checked against a
characteristic S-N curve (indicative form in Figure 18.8), with the governing
parameters — reference number of cycles `NRsk`, slope exponents `m1`/`m2`
either side of the knee point, and reference stress range `ΔσRsk(NRsk)` — read
from Table 18.8 by detail category (straight/bent bar by diameter, welded bar
or mesh, mechanical connectors, marine-environment bar, and five
pretensioning/post-tensioning tendon categories). Bent-bar categories (C, D)
apply a mandrel-diameter factor `kd = 0.35 + 0.026(di/db) ≤ 1.0`.
Variable-amplitude loading again uses a linear damage sum (Eq 18.8(2)); the
calculated stress range must not exceed the steel's design yield strength,
and welded lap splices are prohibited in areas of high fluctuating stress.

![[as3600-table-18.8-sn-curve-parameters.png]]
*Table 18.8 — parameters for characteristic S-N curves for reinforcing steel
and tendons, by detail category (AS 3600:2018).*

## Contradictions

None recorded.

## Related

- [[concrete-limit-state-design-basis]] — Cl 2.1.5 applicability and
  redistribution restriction.
- [[concrete-strength-check-procedures]] — Cl 2.2 general strength-check
  framework that Table 2.4's factors plug into.
- `wiki/0-standards/as-3600-2018-concrete-structures.md` — notes Section 18
  as new in the 2018 edition.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 2.4, Clause 18.2 and
  Clause 18.8 (Tables 2.4, 18.2 and 18.8 reproduced as image assets above;
  remainder of Section 18 not yet ingested).
