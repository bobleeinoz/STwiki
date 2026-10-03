---
title: Design properties of reinforcement (yield, ductility class, elasticity)
category: 0-standards
tags: [material-properties, reinforcement, ductility-class]
standards: [AS 3600:2018 Cl 3.2]
status: draft
reviewed: 2026-09-12
---

# Design properties of reinforcement

> Scope: characteristic yield strength, ductility classification, elastic
> modulus, stress-strain form and thermal expansion of reinforcing steel
> under AS 3600 Cl 3.2.

## Summary

`[code]` Characteristic yield strength `fsy` for design must not exceed the
value in Table 3.2.1 for the reinforcement type —
covers plain bar, deformed bar/mesh, and stainless steel plain/ribbed bar,
each tied to AS/NZS 4671 or BS 6744 designations.

![[as3600-table-3.2.1-yield-strength-ductility-class.png]]
*Table 3.2.1 — yield strength and ductility class of reinforcement, by
product type and designation (AS 3600:2018).*

`[code]` Ductility is classified as
Low (L) or Normal (N) by uniform strain `εsu` and the tensile-to-yield stress
ratio, per AS/NZS 4671 — `εsu` there is called `Agt` and `fsy` is called `Re`
(terminology cross-walk worth keeping, since the two standards use different
symbols for the same quantities).

## Detail

### Higher-grade steels (Cl 1.1.2(d) cross-referenced from 3.2.1 Note 2)

`[code]` For reinforcing grades above the standard Ductility-Class table,
AS 3600 imposes its own chemical-composition and mechanical limits: maximum
carbon/phosphorus/sulphur by cast analysis, a maximum carbon-equivalent
value, a cap on how far actual yield can exceed nominal yield, and — banded
by yield-strength range (500–700 MPa vs 700–800 MPa) — minimum uniform
elongation and minimum tensile-to-yield ratio. `[derived]` Treat any specific
numeric limit here as needing a direct clause check before use in a
calculation; this page only flags that the limit set exists and is banded by
strength range.

### Modulus of elasticity (Cl 3.2.2)

`[code]` `Es` for stresses up to `fsy` is either taken as equal to
200 × 10³ MPa (200 GPa), or determined by test (Cl 3.2.2) — this is a single
fixed value stated directly in the clause text, not a data table.

### Stress-strain curve and thermal expansion (Cl 3.2.3–3.2.4)

`[code]` Stress-strain curve either a recognised simplified form or from test
data. Coefficient of thermal expansion either a fixed standard value or from
test data — note this differs slightly from concrete's own coefficient
(see [[as3600-properties-of-concrete]]), which matters for
composite/thermal-restraint checks.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-properties-of-concrete]], [[as3600-properties-of-tendons-and-prestress-losses]]
- `EA1`–`EA13` style shorthand section tags (per `CLAUDE.md` §6) are a
  steelwork/structural-steel practice, not reinforcement — do not conflate
  with reinforcement Ductility Class designations (N/L/E) on this page.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 3.2 (Table 3.2.1
  reproduced).
