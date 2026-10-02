---
title: Deflection of slabs
category: 2-concrete
tags: [slabs, deflection, serviceability, equivalent-beam]
standards: [AS 3600:2018 Cl 9.4]
status: draft
reviewed: 2026-09-12
---

# Deflection of slabs

> Scope: AS 3600 Cl 9.4 — slab deflection by refined calculation, by an
> equivalent-beam simplified calculation reusing the Cl 8.5 beam method, and
> by a deemed-to-comply span-to-depth ratio.

## Summary

`[code]` Three routes (Cl 9.4.1), directly paralleling
[[concrete-beam-deflection]]: refined calculation (Cl 9.4.2), simplified
calculation via an equivalent beam (Cl 9.4.3, which explicitly reuses
Cl 8.5.3), or — reinforced slabs only — a deemed-to-comply span-to-depth
ratio (Cl 9.4.4). Steel-fibre slabs (with or without conventional
reinforcement/tendons) use Cl 16.4.7.3 instead — not yet ingested.

## Detail

### Refined calculation (Cl 9.4.2)

`[code]` Must allow for: two-way action (the one addition beyond the beam
clause's list); cracking and tension stiffening; shrinkage/creep; expected
load history and construction procedure; and formwork deflection/prop
settlement during construction, particularly where slab formwork is itself
supported off suspended floors below.

### Simplified calculation via equivalent beam (Cl 9.4.3)

`[code]` For uniformly distributed load, deflection is calculated per
Cl 8.5.3 on an equivalent beam:

- **One-way slab**: a unit-width prismatic beam.
- **Rectangular slab on four sides**: a unit-width prismatic beam through the
  slab centre, spanning the short direction `Lx` with the slab's own
  continuity conditions in that direction, carrying a load fraction built
  from the span ratio `Ly/Lx` and an edge-condition coefficient `α` from
  Table 9.4.3 — same nine-edge-condition structure as the
  Cl 6.10.3.2 bending-coefficient tables, since it's derived from the same
  yield-line-type behaviour.

![[as3600-table-9.4.3-coefficient-of-proportionality.png]]
*Table 9.4.3 — coefficient of proportionality (α) for the equivalent-beam
deflection load fraction, by edge condition and span ratio (AS 3600:2018).*
- **Multi-span two-way flat slab**: the idealized-frame column strips
  (Cl 6.9, see [[concrete-idealized-frame-method]]), for deflections on
  column lines or midway between supports.

### Deemed-to-comply span-to-depth ratio (Cl 9.4.4)

`[code]` **One-way slabs and multi-span two-way flat slabs** (9.4.4.1):
applies to essentially-uniform-depth slabs, fully propped during
construction, uniform load, imposed action ≤ permanent action. `Lef/d`
checked against a formula combining a slab-type coefficient `k3` (1.0 for
one-way, a value below 1.0 for a two-way flat slab without drop panels, a
value above 1.0 for a two-way flat slab *with* drop panels meeting minimum
extent/depth criteria — drop panels measurably help), a support-condition
coefficient `k4` (different fixed values for simply-supported vs. end-span
vs. interior-span continuous slabs, again gated by the same span-ratio/
end-span-length conditions used elsewhere), the chosen deflection limit
`Δ/Lef` (per Cl 2.3.2, see [[concrete-serviceability-design]]), `Ec`, and an
effective design load `Fd.ef` built the same way as the beam version
(`kcs`-scaled dead load plus short/long-term-factored live load).
**Rectangular slabs on four sides** (9.4.4.2): same formula structure but
`k3 = 1.0` always, and `k4` instead comes from Table 9.4.4.2, keyed to edge
condition and span ratio `Ly/Lx` — checked on the
*shorter* effective span.

![[as3600-table-9.4.4.2-slab-system-multiplier-k4.png]]
*Table 9.4.4.2 — slab-system multiplier (k4) for rectangular slabs supported
on four sides, by edge condition and span ratio (AS 3600:2018).*

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-beam-deflection]] — the Cl 8.5.3 method this clause reuses
  directly.
- [[concrete-serviceability-design]] — Cl 2.3.2 deflection limits.
- [[concrete-idealized-frame-method]] — Cl 6.9 column strips used for
  multi-span flat-slab deflection.
- [[concrete-simplified-flexural-analysis]] — Cl 6.10.3 edge-condition
  categories shared with Table 9.4.3.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 9.4 (Tables 9.4.3,
  9.4.4.2 reproduced as image assets above).
