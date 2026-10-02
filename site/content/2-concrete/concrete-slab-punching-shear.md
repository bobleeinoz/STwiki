---
title: Strength of slabs in shear (punching shear at columns)
category: 2-concrete
tags: [slabs, punching-shear, flat-slabs, critical-shear-perimeter]
standards: [AS 3600:2018 Cl 9.3]
status: draft
reviewed: 2026-09-12
---

# Strength of slabs in shear (punching shear)

> Scope: AS 3600 Cl 9.3 — local (punching) shear strength of flat slabs
> around a support or concentrated load, with and without moment transfer.
> Wide-beam-type slab shear (failure across the width of the slab) is
> designed per Cl 8.2 instead — see
> [[concrete-beam-shear-and-torsion-design]].

## Summary

`[code]` Cl 9.3.2 splits slab shear into two failure modes: **wide-beam
shear** across the slab width (design per Cl 8.2, same method as a beam) and
**local/punching shear** around a support or concentrated load (design per
this clause). Punching shear strength `Vu` = `Vuo` (Cl 9.3.3) when no moment
is transferred to the support (`Mv* = 0`), or the reduced/adjusted value from
Cl 9.3.4 when moment transfer is present.

## Detail

### Definitions (Cl 9.3.1)

`[code]` **Effective area of a support/load** — the minimum-perimeter area
fully enclosing it. **Critical opening** — a slab opening whose edge sits
within `2.5bo` of the critical shear perimeter (openings closer than this
reduce the effective perimeter). **Critical shear perimeter** — a line
geometrically similar to the effective loaded area's boundary, offset by
`dom/2` (`dom` = mean effective depth around the perimeter). **Torsion
strip** — a slab strip of width `a`, aligned perpendicular to the direction
of the transferred moment `Mv*`, used in the Cl 9.3.4 reduction.

### Ultimate shear strength with no moment transfer (Cl 9.3.3)

`[code]` Without a shear head: `Vuo = u·dom·(fcv + 0.3σcp)`, where `u` is the
critical shear perimeter length, `fcv` is a concrete shear-stress term built
from `√f'c` and the loaded-area aspect ratio `βh` (capped at an absolute
`√f'c`-based ceiling), and `σcp` is average effective prestress at the
centroid — assessed separately for corner, edge and internal columns since
the perimeter geometry differs. With a shear head: a different, more
conservative form applies, still built from `√f'c`, `σcp` and an absolute
ceiling term.

### Ultimate shear strength with moment transfer (Cl 9.3.4)

`[code]` Where `Mv* ≠ 0` and any shear reinforcement present conforms with
Cl 9.3.5/9.3.6 (below), `Vu` follows one of four routes depending on what
reinforcement is provided:

- No special torsion-strip/spandrel-beam reinforcement: `Vu` is `Vuo` divided
  by a factor that grows with `Mv*` relative to `V*`, the perimeter length,
  and `dom` — i.e. moment transfer *reduces* the punching capacity relative
  to the no-moment case.
- Minimum closed fitments in the torsion strip: a higher `Vu.min` applies (a
  1.2× multiplier on an equivalent no-moment-style term), reflecting the
  fitments' confinement/tying benefit.
- Minimum closed fitments in perpendicular spandrel beams: a similar
  `Vu.min` form, scaled additionally by the spandrel beam's depth ratio to
  the slab.
- More than minimum closed fitments: `Vu` builds on `Vu.min` by adding a
  reinforcement-area term (`Asw/s`) scaled by fitment dimension and yield
  strength.

In every case, `Vu` is capped at `Vu.max = 3·Vu.min·(x/y)`, where `x` and `y`
are the shorter and longer cross-section dimensions of the torsion strip or
spandrel beam.

### Minimum closed fitments and detailing (Cl 9.3.5–9.3.6)

`[code]` Minimum fitment area: `Asw/s ≥` a formula in `y1` (larger overall
fitment dimension) and `fsy.f`. Detailing: fitments extend along the torsion
strip/spandrel beam at least `Lt/4` from the support/load face (one or both
sides of the centroidal axis as applicable), first fitment within `0.5s` of
the support face, spacing capped at the lesser of 300 mm and the beam/slab
depth, at least one longitudinal bar per fitment corner, dimensions per
Fig 9.3.6.

`[practice]` Types of shear reinforcement other than those in Cl 9.3.3/9.3.4
(e.g. proprietary shear studs/rails) may have their strength established by
testing under Appendix B instead of by this clause's formulas.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-beam-shear-and-torsion-design]] — the Cl 8.2 method used for
  wide-beam-type slab shear instead of this clause.
- [[concrete-slab-strength-in-bending]] — Cl 9.1.2's reinforcement
  concentration rule near columns, closely tied to punching performance.
- [[concrete-idealized-frame-method]] — Cl 6.9.5.4/6.10.4.5 unbalanced-moment
  values that feed `Mv*` here.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clause 9.3 (Figures 9.3(A),
  9.3(B), 9.3.6 not reproduced).
