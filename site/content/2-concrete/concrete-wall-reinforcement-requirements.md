---
title: Wall reinforcement requirements (minimum ratios, spacing, restraint, dowels)
category: 2-concrete
tags: [walls, detailing, minimum-reinforcement, earthquake]
standards: [AS 3600:2018 Cl 11.7]
status: draft
reviewed: 2026-09-12
---

# Wall reinforcement requirements

> Scope: AS 3600 Cl 11.7 — minimum vertical/horizontal reinforcement ratios,
> horizontal crack-control steel, spacing, restraint of vertical
> reinforcement (including earthquake-specific provisions), and dowels at
> wall-to-wall or wall-to-floor joints.

## Summary

`[code]` This clause is where a wall's reinforcement ratio, restraint detail
and joint dowelling all get fixed — feeding directly into the `ρw` term used
in [[concrete-wall-in-plane-shear]] and interacting closely with earthquake
design (Section 14, not yet ingested).

## Detail

### Minimum reinforcement (Cl 11.7.1)

`[code]` **Vertical**: `ρw ≥` the larger of 0.0025 or whatever strength
requires — reducible to 0.0015 where design axial compressive force doesn't
exceed the lesser of `0.03√f'c` and 2 MPa (i.e. lightly-loaded walls get a
relaxed minimum). **Horizontal**: `ρw ≥ 0.0025` generally, reducible for a
one-way-buckling wall (Cl 11.4(a)) with no restraint against horizontal
shrinkage/thermal movement — to zero if the wall is <2.5 m wide, or to
0.0015 otherwise. For walls >500 mm thick, the minimum near each surface may
be calculated using 250 mm as the effective `tw` (same concession as slabs,
Cl 9.5.3.1).

### Horizontal reinforcement for crack control (Cl 11.7.2)

`[code]` Where a wall is restrained against horizontal shrinkage/temperature
movement, minimum horizontal `ρw` is banded by exposure classification and
desired crack-control degree: for A1/A2, three tiers (minor/moderate/strong)
with increasing ratio; for B1/B2/C1/C2, always the strongest tier (0.006) —
directly mirroring the slab shrinkage/temperature tiering in
[[concrete-slab-crack-control]] Cl 9.5.3.4. Walls longer than 8 m may need
additional base crack-control reinforcement for early-age hydration/
shrinkage restraint cracking.

### Spacing (Cl 11.7.3)

`[code]` Minimum clear spacing per Cl 17.1.3 placement needs, but never less
than `3dᵦ`. Maximum centre-to-centre spacing: the lesser of `2.5tw` and
350 mm — this maximum tightens (implicitly, via the restraint requirements
below) for thicker walls, walls in net tension, two-way-buckling walls, and
tall/slender walls, since those conditions each independently trigger
additional restraint requirements in Cl 11.7.4.

### Restraint of vertical reinforcement (Cl 11.7.4)

`[code]` Beyond ordinary transverse reinforcement for design actions:

- **Any wall in a structure with structural ductility factor `μ > 1.0`**:
  vertical reinforcement restrained per Cl 14.6 (earthquake-specific,
  Section 14 not yet ingested).
- **`f'c ≤ 50 MPa`, designed as a column (Section 10)**: restrained per
  Cl 10.7.4 (see [[concrete-column-reinforcement-detailing]]) **unless** one
  of three relief conditions holds: `N* ≤ 0.5·φNu`; the vertical
  reinforcement isn't used as compression reinforcement; or `ρw ≤ 0.01` with
  a minimum 0.0025 horizontal ratio provided — any one of these three avoids
  the full column-style restraint detail.
- **`f'c ≤ 50 MPa`, designed by the simplified method (Cl 11.5)**: no
  restraint of vertical reinforcement required at all — see
  [[concrete-wall-simplified-axial-design]].
- **`f'c > 50 MPa`**: the core must be confined, with restraint per
  Cl 14.5.4 where the wall (as a column) exceeds `N* > 0.15·f'c·Ag` and
  `M* > 0.6·φMu`, or (as a simplified-method wall) where any portion exceeds
  `N* > 0.5·φNu`; otherwise, a prescriptive detail applies instead — U-bars
  fully lapped with horizontal reinforcement at wall ends/corners (max
  spacing the lesser of `tw`/200 mm), with column-style ties (Cl 10.7.3/
  10.7.4) required over a region extending the greater of `2tw` or `0.15Lw`
  from each end/corner.

### Dowels (Cl 11.7.4, final provisions)

`[code]` Dowels at joints must satisfy axial force, bending, horizontal
shear and any other joint load effects, with minimums that scale with
earthquake ductility demand: where `μ > 1.0` was used in the earthquake
analysis, dowels must transfer the *yield* force of the wall's vertical
reinforcement (`Ast,dowel ≥ Ast,wall`); for `μ = 1.0` with structural
performance factor `Sp ≥ 0.77` (i.e. effectively elastic or near-elastic
earthquake design) and for any non-earthquake case (e.g. wind): walls
remaining in net compression need no special dowel provision, but walls not
remaining in net compression need `Ast,dowel ≥ 0.5·Ast,wall`. In every case,
dowel reinforcement must still meet the Cl 11.7.1 minimum ratio and be fully
anchored per Section 13.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-wall-in-plane-shear]] — `ρw` used directly in the Cl 11.6.4
  shear-reinforcement contribution.
- [[concrete-column-reinforcement-detailing]] — Cl 10.7.4 restraint rules
  this clause conditionally invokes or overrides.
- [[concrete-slab-crack-control]] — Cl 9.5.3.4 shrinkage/temperature tiering,
  structurally identical to Cl 11.7.2 here.
- [[concrete-wall-simplified-axial-design]] — Cl 11.5, whose walls are
  exempt from vertical-reinforcement restraint at `f'c ≤ 50 MPa`.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clause 11.7.
