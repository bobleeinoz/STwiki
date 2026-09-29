---
title: Wall design basis — scope, design procedures, braced walls and effective height
category: 2-concrete
tags: [walls, design-basis, braced-walls, effective-height]
standards: [AS 3600:2018 Cl 11.1, AS 3600:2018 Cl 11.2, AS 3600:2018 Cl 11.3, AS 3600:2018 Cl 11.4]
status: draft
reviewed: 2026-09-12
---

# Wall design basis

> Scope: AS 3600 Section 11's scope and routing logic (Cl 11.1–11.2), the
> definition of a braced wall (Cl 11.3), and effective height for slenderness
> purposes (Cl 11.4).

## Summary

`[code]` Section 11 is fundamentally a **routing** section: depending on
loading (in-plane only vs. combined in-plane/out-of-plane), bracing, and
stress level, a wall is designed either by this section's own simplified
method, or by treating it as a slab (Section 9) or a column (Section 10)
instead. `fsy` for wall reinforcement is capped at 500 MPa throughout this
section — lower than the general 500+ MPa ceiling elsewhere.

## Detail

### Scope and routing (Cl 11.1)

`[code]` **Braced walls under in-plane load only**: designed per Cl 11.2–11.7
(this section's own method). **Braced walls under combined in-plane +
out-of-plane load, and all unbraced walls**: designed either as a slab
(Section 9 — permitted where mid-height stress from factored in-plane
bending+axial stays within `0.03√f'c`, provided second-order/long-term
deflection effects are considered and effective-height-to-thickness ratio
≤50, noting fire resistance may restrict this ratio further, see
[[concrete-fire-resistance-design]]) or as a column (Section 10, using
Cl 11.4 instead of Cl 10.5.3 for the slenderness factor `k`). In-plane shear
uses Cl 11.6 or Cl 8.2; out-of-plane shear always uses Section 8.

### Design procedures (Cl 11.2)

`[code]` **Braced wall, section entirely in compression**: horizontal shear
per Cl 11.6 always; vertical compression either via the Cl 11.5 simplified
segment method (if within its limits) or as a column per Section 10 with
reinforcement on each face (Cl 11.7.4 may override Cl 10.7.4's restraint
rules; Cl 10.7.1(b), 11.4 and 11.7 still apply regardless). **Braced wall,
part of section in tension**: designed for in-plane bending as strut-and-tie
(Section 12, see [[concrete-non-flexural-members-and-strut-tie-models]]) where the wall's
height-to-length ratio `H/L ≤ 2`, or as a column (Section 10, same
face-reinforcement/override provisions as above) where `H/L > 2` — the
distinction reflects deep-beam-like behaviour (strut-and-tie) versus
column-like behaviour (interaction diagram) at different aspect ratios.
`[code]` For earthquake actions specifically, whether a wall's horizontal
section is fully in compression is assessed using a structural ductility
factor `μ = 1.00` and structural performance factor `Sp = 1.0` per AS 1170.4
— i.e. an elastic (unreduced) assessment, not the ductility-reduced design
forces used for strength.

`[code]` **Groups of interconnected walls** (Cl 11.2.2): in-plane load
distribution between linked/coupled walls comes from linear elastic analysis
of the overall structure, apportioned by relative stiffness (gross
cross-sectional properties). Interconnected vertical edges must be designed
for the transmitted vertical shear.

### Braced wall definition (Cl 11.3)

`[code]` A wall is braced if it's part of a structure not relying on the
wall's own out-of-plane strength/stiffness, **and** its connection to the
rest of the structure can transmit both the calculated load effects and a
minimum tie force — 2.5% of the total vertical load the wall carries at the
lateral-support level, but not less than 2 kN per metre of wall length (a
robustness-style minimum tie force, similar in spirit to the Cl 2.1.3
structural-integrity requirement).

### Effective height (Cl 11.4)

`[code]` `Hwe = k·Hw` (`Hw` = floor-to-floor unsupported height, `L1` =
horizontal length between lateral-restraint centres or to a free edge).
`k` depends on the buckling/restraint pattern:

- **One-way buckling**, floor-supported at both ends: `k = 0.75` if
  rotational restraint is provided at both ends, `k = 1.0` otherwise.
- **Two-way buckling, three-sided support** (floors + intersecting walls):
  `k` from a formula in `Hw/L1`, floored at 0.3 and capped at whatever the
  one-way-buckling formula would give.
- **Two-way buckling, four-sided support**: one formula for `Hw ≤ L1`, a
  different (linear) formula for `Hw > L1`.

`[code]` Openings are ignored if their total area is <1/10 of the wall area
and no single opening's height exceeds 1/3 of the wall height; otherwise the
wall area between support and opening is treated as three-sided-supported,
and the area between openings as two-sided-supported. An intersecting wall
of length ≥`0.2Hw` may itself count as a lateral restraint.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-wall-simplified-axial-design]] — Cl 11.5, the segment method
  referenced from Cl 11.2.
- [[concrete-wall-in-plane-shear]] — Cl 11.6.
- [[concrete-wall-reinforcement-requirements]] — Cl 11.7, overriding some
  Cl 10.7.4 provisions per this page's routing logic.
- [[concrete-column-strength-interaction]], [[concrete-slab-strength-in-bending]]
  — the Section 10/Section 9 methods a wall may be routed into.
- [[concrete-non-flexural-members-and-strut-tie-models]] — Section 12's
  strut-and-tie method for low-aspect-ratio walls in net tension, which in
  turn relies on the Section 7 rules in [[concrete-strut-and-tie-modelling]].

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clauses 11.1–11.4.
