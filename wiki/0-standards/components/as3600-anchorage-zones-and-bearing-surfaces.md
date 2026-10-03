---
title: Anchorage/bearing zone reinforcement and bearing surface stress limits
category: 0-standards
tags: [anchorage-zones, bearing, prestressing, bursting-reinforcement]
standards: [AS 3600:2018 Cl 12.5, AS 3600:2018 Cl 12.6]
status: draft
reviewed: 2026-09-12
---

# Anchorage/bearing zone reinforcement and bearing surface stress limits

> Scope: AS 3600 Cl 12.5 (reinforcement behind concentrated forces and
> prestressing anchorages — a simplified alternative to full strut-and-tie
> modelling for simple anchorage layouts) and Cl 12.6 (the bearing stress
> limit at a concrete surface).

## Summary

`[code]` Cl 12.5.1: components with concentrated forces, including
post-tensioned anchorage zones, are designed per Section 7 (strut-and-tie —
see [[as3600-strut-and-tie-modelling]]) in general, but **may** instead use
this section's simplified formulas where there are no more than two
anchorages in any elevation or plan — more than two anchorages pushes the
design back to full Section 7 strut-and-tie modelling.

## Detail

### Reinforcement basis (Cl 12.5.2)

`[code]` Bursting/spalling stresses disperse through both the depth and
width of the anchorage/bearing zone, so reinforcement is provided in two
orthogonal planes parallel to the end faces, each assessed by its own
two-dimensional analysis. Tensile forces are calculated on longitudinal
sections through the anchorage/bearing zone and on sections where peak
transverse moments occur — the "transverse moment on a longitudinal section"
being the equilibrating moment on the free body bounded by that section, a
parallel free surface, the loaded face, and a parallel plane at the
anchorage/bearing zone's inner end.

### Loading cases (Cl 12.5.3)

`[code]` Must consider: all anchorages loaded simultaneously, and critical
loadings *during* the stressing operation (i.e. not just the final,
fully-stressed state — partial stressing sequences can be more critical
locally). Where two anchorages sit closer than 0.3× the member's total
depth/breadth, they must be assessed as if acting like a single anchorage
carrying their combined force — the "pair acts as one" concession only
applies below that spacing threshold.

### Tensile force along the load/anchorage line (Cl 12.5.4)

`[code]` `T = 0.25·P·(1 − kr)`, where `P` is the maximum applied load
(for prestressing, the maximum jacking load) and `kr` is the ratio of the
bearing plate's depth/breadth to the corresponding dimension of the
**symmetrical prism** — a notional prism centred on the anchorage, with
depth/breadth equal to twice the distance from the anchorage/bearing-plate
centre to the nearer concrete face. `[derived]` Own-words: this is the
bursting-force formula for load dispersing symmetrically into a prism —
`kr → 1` (bearing plate nearly fills the prism) drives `T → 0`, since
there's little dispersion left to resist; `kr → 0` (a small plate in a wide
prism) drives `T` toward its maximum, `0.25P`.

### Tensile force near the loaded face (Cl 12.5.5)

`[code]` Where the transverse-moment sense indicates the tensile stress
resultant acts near the loaded face (single eccentric anchorage/bearing
plate, or between widely-spaced anchorages): for a single eccentric
anchorage/plate, divide the peak transverse moment by a lever arm of half
the member's overall depth; between a pair of anchorages, divide by a lever
arm of 0.6× the anchorage spacing.

### Reinforcement sizing and distribution (Cl 12.5.4–12.5.5, continued)

`[code]` Reinforcement area for each situation = the relevant tensile force
÷ 150 MPa (own-words: a fixed, conservative serviceability-level stress
limit rather than a yield-strength-based capacity factor — this is a
crack-control-driven sizing, not a strength-driven one). Distribution:
reinforcement for the Cl 12.5.4 (dispersion) force is spread uniformly from
`0.2D` to `1.0D` from the loaded face, with similar reinforcement placed
between `0.2D` and as close as practicable to the loaded face itself (`D`
here being the symmetrical prism's own depth/breadth); side slopes of 1
(longitudinal) to 1 (transverse) relative to the load direction. At any
plane parallel to the loaded face, reinforcement is governed by whichever
longitudinal section demands the most at that plane, and extends over the
full depth/breadth of the end zone.

## Detail — Bearing surfaces (Cl 12.6)

`[code]` Absent special confinement reinforcement, maximum design bearing
stress at a concrete surface is capped at the **lesser** of `0.9√f'c·√(A2/A1)`
and `1.8√f'c`, where `A1` is the bearing area and `A2` is the largest area of
the supporting surface that's geometrically similar to and concentric with
`A1` — own-words: the `√(A2/A1)` term credits load spreading into a larger
supporting area, but the flat `1.8√f'c` ceiling stops that credit from
growing without bound. For a sloped/stepped supporting structure, `A2` may
be taken as the base area of the largest right pyramid/cone frustum with
`A1` as its opposite end, side slopes of 1 (longitudinal) to 2 (transverse)
relative to the load direction, contained wholly within the supporting
structure. **Does not apply** to nodes within a strut-and-tie model — those
use the Cl 7.4 nodal-strength rules instead (see
[[as3600-strut-and-tie-modelling]]).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-strut-and-tie-modelling]] — Section 7, the general method this
  clause's simplified two-anchorage case substitutes for, and the Cl 7.4
  nodal rules that govern instead of Cl 12.6 within a strut-and-tie model.
- [[as3600-properties-of-tendons-and-prestress-losses]] — jacking force
  `P` and anchorage-related context.
- [[as3600-non-flexural-members-and-strut-tie-models]] — Cl 12.1's
  "end zones of prestressed members" scope item, of which this clause is the
  detailed treatment.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clauses 12.5, 12.6.
