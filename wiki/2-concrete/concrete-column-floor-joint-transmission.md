---
title: Transmission of axial force through floor systems, and column crack control
category: 2-concrete
tags: [columns, joints, floor-systems, crack-control]
standards: [AS 3600:2018 Cl 10.8, AS 3600:2018 Cl 10.9]
status: draft
reviewed: 2026-09-12
---

# Transmission of axial force through floor systems

> Scope: AS 3600 Cl 10.8 — how a column's axial force is designed to pass
> through a floor system of lower concrete strength, and Cl 10.9 — a pointer
> clause for column crack control.

## Summary

`[code]` Where floor-system concrete is markedly weaker than the column
concrete (common where columns use high-strength mixes but floors don't),
the joint region itself needs either continuous reinforcement or an
effective-strength calculation — otherwise the floor concrete becomes the
weak link in the column's load path.

## Detail

### Transmission through floor systems (Cl 10.8)

`[code]` **Deemed adequate** if floor-system concrete strength ≥0.75× column
concrete strength **and** longitudinal reinforcement is continuous through
the joint — no calculation needed. Otherwise, additional longitudinal
reinforcement through the joint is required, sized using an effective joint
compressive strength `f'ce` that blends column and floor concrete
strengths, banded by how many sides restrain the joint:

- **Restrained on four sides** by beams of approximately equal depth or a
  slab: `f'ce` from a formula combining `f'cs` (slab/beam strength) and `f'cc`
  (column strength) weighted by the joint depth-to-column-width ratio `h/b`
  (floored at 0.33), bounded between the lesser of `f'cc`/`1.33·f'cs` and the
  lesser of `f'cc`/`2.5·f'cs`.
- **Restrained on two opposing sides**: a similar but more conservative
  form, bounded between the lesser of `f'cc`/`1.33·f'cs` and the lesser of
  `f'cc`/`2.0·f'cs`.
- **Restrained on two adjacent sides**: `f'ce` taken directly as
  `1.33·√(f'cs·f'cc)` — own-words: a geometric-mean-style blend, no h/b
  weighting, reflecting the weaker confinement of an adjacent-side-only
  condition.

`[practice]` Confining reinforcement may be used to increase the joint's
effective strength beyond the bare formula; beams/slabs should restrain over
the full width of the column joint for these formulas to apply as stated.

### Crack control (Cl 10.9)

`[code]` Flexural cracking in a column is controlled by satisfying Cl 8.6 —
see [[concrete-beam-crack-control]]. No column-specific crack-control method
exists; the beam clause is applied directly.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-column-reinforcement-detailing]] — Cl 10.7, the preceding
  Section 10 clause on fitments/splicing.
- [[concrete-beam-crack-control]] — Cl 8.6, applied directly per Cl 10.9.
- [[concrete-properties-of-concrete]] — `f'c` grade selection feeding the
  `f'ce` blend calculation.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clauses 10.8, 10.9.
