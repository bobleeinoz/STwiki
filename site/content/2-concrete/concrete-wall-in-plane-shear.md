---
title: Design of walls for in-plane shear forces
category: 2-concrete
tags: [walls, in-plane-shear, shear-walls]
standards: [AS 3600:2018 Cl 11.6]
status: draft
reviewed: 2026-09-12
---

# Design of walls for in-plane shear forces

> Scope: AS 3600 Cl 11.6 — in-plane shear strength of walls, split into
> concrete and reinforcement contributions, with an absolute upper limit.

## Summary

`[code]` Same overall structure as beam shear (`Vu = Vuc + Vus`, see
[[concrete-beam-shear-and-torsion-design]]), but with wall-specific formulas
keyed to the wall's aspect ratio `H/Lw` rather than the MCFT strain-based
`kv`/`θv` method used for beams.

## Detail

### Critical section and strength check (Cl 11.6.1–11.6.2)

`[code]` Every wall section is designed for its actual shear force, but the
maximum transverse shear near the wall base may conservatively be taken as
the value at a distance `Lw/2` or `H/2` from the base, whichever is less
(analogous to the beam Cl 8.2.3.2 "at `dv` from the support" concession).
Design check: `φVu ≥ V*`, `Vu = Vuc + Vus`, capped at an absolute maximum
`Vu.max = 0.2√f'c·0.8·Lw·tw` regardless of how much reinforcement is added —
a web-crushing-style ceiling analogous to beam `Vu.max` (Cl 8.2.3.3). `φ`
from Table 2.2.2.

### Concrete contribution `Vuc` (Cl 11.6.3)

`[code]` Two formulas depending on aspect ratio:

- `H/Lw ≤ 1`: `Vuc` from a formula combining `√f'c` and an `H/Lw`-dependent
  term (Eq 11.6.3(1)), scaled by `0.8·Lw·tw`.
- `H/Lw > 1`: the *lesser* of the Item-(a) value and a second formula
  (Eq 11.6.3(2)) that reduces as `H/Lw` grows further beyond 1 — but never
  taken below a fixed floor of `0.17√f'c·0.8·Lw·tw`.

`[derived]` Own-words: this is structurally the same logic as a beam's
concrete shear contribution reducing with span-to-depth-like ratio, capped
at both ends (an upper formula for squat walls, a lower floor for slender
walls) rather than the continuous MCFT strain-based scaling used for beams.

### Reinforcement contribution `Vus` (Cl 11.6.4)

`[code]` Built from a wall reinforcement ratio `ρw`, itself defined
differently by aspect ratio: for `H/Lw ≤ 1`, `ρw` is the **lesser** of the
vertical or horizontal reinforcement ratios (cross-sectional area over wall
area, in the respective direction) — i.e. whichever direction is more
sparsely reinforced governs; for `H/Lw > 1`, `ρw` is simply the horizontal
reinforcement ratio per vertical metre — reflecting that horizontal steel is
what resists shear in a taller, more slender (cantilever-shear-wall-like)
wall, while a squat wall's shear resistance can be limited by either
direction.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-beam-shear-and-torsion-design]] — the conceptually parallel
  `Vuc + Vus` beam method.
- [[concrete-wall-reinforcement-requirements]] — Cl 11.7, minimum vertical/
  horizontal reinforcement ratios that set a floor under the `ρw` used here.
- [[concrete-wall-design-basis-and-classification]] — Cl 11.2, which routes
  a wall to this clause for horizontal shear regardless of which vertical-
  force method (segment, column, or strut-and-tie) applies.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clause 11.6.
