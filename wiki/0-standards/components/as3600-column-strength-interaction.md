---
title: Column strength in combined bending and compression (interaction diagram)
category: 0-standards
tags: [columns, interaction-diagram, biaxial-bending, squash-load]
standards: [AS 3600:2018 Cl 10.6]
status: draft
reviewed: 2026-09-12
---

# Column strength in combined bending and compression

> Scope: AS 3600 Cl 10.6 — the axial-load/moment interaction diagram method
> for column cross-sections, including the biaxial-bending shortcuts.

## Summary

`[code]` Column section strength is represented as an interaction diagram
(`N` vs. `M`, Fig 10.6.2.1) built from four defined points/regions: the
squash load (pure compression), the decompression point, a linear
transition between them, and a rectangular-stress-block-based transition
down to pure bending strength — the same basis-of-calculation assumptions as
beam bending (Cl 10.6.1: plane sections remain plane, no concrete tension,
Cl 3.1.4/3.2.3 stress-strain relationships, compression-reinforcement strain
capped at 0.003), plus an explicit requirement to consider cover spalling
where the neutral axis lies outside the section.

![[as3600-fig-10.6.2.1-axial-load-moment-diagram.png]]
*Figure 10.6.2.1 — axial load/moment (`N`–`M`) interaction diagram for a
column section, showing the squash load, decompression point and
intermediate transitions (AS 3600:2018).*

## Detail

### Squash load `Nuo` (Cl 10.6.2.2)

`[code]` Pure-compression strength, assuming a uniform concrete stress
`α1·f'c` (`α1` reduces from a fixed upper value as `f'c` increases, bounded
0.72–0.85 — this already folds in the Cl 3.1.4 0.9 modifier) and a
reinforcement strain capped at 0.0025 (note: tighter than the general 0.003
cap, specific to the squash-load calculation).

### Decompression point and transitions (Cl 10.6.2.3–10.6.2.5)

`[code]` **Decompression point**: extreme-compression-fibre strain 0.003,
extreme-tension-fibre strain zero, using the Cl 10.6.2.5 rectangular stress
block. **Transition, decompression → squash load** (neutral axis outside the
section): a straight-line interpolation between the two points. **Transition,
decompression → pure bending** (Cl 10.6.2.5): same rectangular-stress-block
form as beams (Cl 8.1.3, see [[as3600-beam-strength-in-bending]]) — uniform
stress `γ2·f'c` over the area bounded by the section edges and a line at
`kᵤd` from the extreme compression fibre, with the same `γ2` reductions for
circular sections (−5%) and sections narrowing toward the compression face
(−10%). The clause explicitly flags that cover spalling under high-strength
concrete is a real risk here, and notes that confinement effects may be
credited provided secondary effects like spalling are also considered.

### Biaxial bending (Cl 10.6.3–10.6.4)

`[practice]` **Separate-axis shortcut** (10.6.3): for a rectangular section
with cross-sectional aspect ratio ≤3.0 under simultaneous biaxial bending
plus axial force, each axis may be designed for its moment independently
provided the resultant force's line of action stays within a defined
central region of the section (Fig 10.6.3) — a geometric check that the
combined eccentricity isn't large enough on both axes at once to invalidate
treating them separately.

![[as3600-fig-10.6.3-limitation-line-of-action.png]]
*Figure 10.6.3 — limitation on the line of action of the resultant force,
central region of the section within which the Cl 10.6.3 separate-axis
shortcut applies (AS 3600:2018).*

`[code]` **Full biaxial check** (10.6.4), where the separate-axis shortcut
doesn't apply: `(Mx*/Mux)^αn + (My*/Muy)^αn ≤ 1.0`, where `Mux`/`Muy` are the
section's uniaxial bending strengths (calculated separately about each axis
under the actual design axial force `N*`), `Mx*`/`My*` are the (possibly
slenderness-magnified) design moments about each axis, and the exponent
`αn = 0.7 + 1.7·N*/Nuo` is bounded between 1 and 2 — own-words: the
interaction curve is closer to linear (`αn≈1`) at low axial load and closer
to a rounder, more forgiving curve (`αn≈2`) at higher axial load, reflecting
how biaxial interaction actually softens as compression dominates. `φ` for
this check is 0.65 generally (see Table 2.2.2).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-beam-strength-in-bending]] — Cl 8.1.3 rectangular stress block,
  reused directly by Cl 10.6.2.5.
- [[as3600-column-slenderness-and-moment-magnification]] — the magnified
  moments `Mx*`/`My*` checked against this page's interaction diagram.
- [[as3600-column-reinforcement-detailing]] — Cl 10.7, confinement/spalling
  mitigation referenced by Cl 10.6.1/10.6.2.5.
- [[as3600-strength-check-procedures]] — Table 2.2.2 `φ`.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clause 10.6 (Figures 10.6.2.1,
  10.6.3 reproduced as image assets above).
