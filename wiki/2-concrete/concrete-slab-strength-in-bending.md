---
title: Strength of slabs in bending, reinforcement detailing and structural integrity
category: 2-concrete
tags: [slabs, bending, flexure, integrity-reinforcement, detailing]
standards: [AS 3600:2018 Cl 9.1, AS 3600:2018 Cl 9.2]
status: draft
reviewed: 2026-09-12
---

# Strength of slabs in bending, detailing and structural integrity

> Scope: AS 3600 Cl 9.1 (bending strength, minimum reinforcement, detailing
> arrangements for one-way and two-way slabs) and Cl 9.2 (structural
> integrity/progressive-collapse reinforcement at slab-column connections).

## Summary

`[code]` Slab bending strength reuses the beam method (Cl 8.1.1–8.1.8, see
[[concrete-beam-strength-in-bending]]) wholesale, but with slab-specific
minimum reinforcement ratios for two-way slabs and a large body of
deemed-to-conform reinforcement *arrangement* rules tied to which
Section 6 analysis method was used.

## Detail

### Bending strength and minimum reinforcement (Cl 9.1.1)

`[code]` Determined per Cl 8.1.1–8.1.8, except that for two-way reinforced
slabs the Cl 8.1.6.1 minimum-strength requirement is deemed satisfied by a
minimum `Ast/bd` ratio (in each direction) that differs by support type:
column-corner-supported slabs need a higher ratio than slabs supported by
beams/walls on all four sides — both forms scale with `√f'ct.f/fsy` and a
depth ratio, mirroring the beam formula's structure.

### Reinforcement distribution in two-way flat slabs (Cl 9.1.2)

`[code]` At least 25% of the total design negative moment in a column strip
plus its adjacent half-middle-strips must be resisted by reinforcement/
tendons concentrated in a slab cross-section centred on the column, of width
equal to twice the slab (or drop panel) depth plus the column width — this
is the "column strip within the column strip" concentration rule that
limits punching-related over-cracking near the support.

### Detailing of tensile reinforcement (Cl 9.1.3)

`[code]` **General procedure** (9.1.3.1): where the moment envelope is
calculated, curtailment/anchorage is based on a hypothetical moment diagram
displaced by `D` from each side of the maximum-moment sections — at least a
third of negative-moment support reinforcement extends `12dᵦ` or `D` (greater
governs) past the contraflexure point; at a simply-supported discontinuous
end, at least half the positive-moment reinforcement anchors by the same
`12dᵦ`/`D` extension past the support face (reducible to `8dᵦ` or `4dᵦ` where
no shear reinforcement is required and half/all of the reinforcement is so
extended); at a continuous/restrained support, at least a quarter of the
positive-moment reinforcement continues past the near face. Lateral-load
frames incorporating slabs must not shorten these lengths below the
deemed-to-conform figures.

`[practice]` Three deemed-to-conform arrangements exist, each tied to the
matching Section 6 analysis method — using one without having run the
matching analysis method is not a valid shortcut:

- **One-way slabs** (9.1.3.2), for slabs analysed by the Cl 6.10.2 simplified
  method (see [[concrete-simplified-flexural-analysis]]) under the same
  span-ratio/load-ratio gates.

![[as3600-fig-9.1.3.2-one-way-slab-reinforcement-arrangement.png]]
*Figure 9.1.3.2 — deemed-to-conform reinforcement arrangement for one-way
slabs designed by the Cl 6.10.2 simplified method (AS 3600:2018).*
- **Two-way slabs on four sides** (9.1.3.3), for slabs analysed by the
  Cl 6.10.3 method: negative-moment reinforcement at a discontinuous edge
  extends 0.15× the shorter span into the slab; **exterior-corner**
  reinforcement (both top and bottom, two perpendicular layers, each
  extending 0.2× the shorter span from the edge) is required where the
  corner is restrained against uplift, sized as a fraction of the maximum
  positive-moment reinforcement — a larger fraction where neither edge at
  the corner is continuous, a smaller fraction where one edge is continuous.
- **Two-way flat slabs** (9.1.3.4), for slabs analysed by the Cl 6.10.4
  idealized-frame-derived method: reinforcement perpendicular to a
  discontinuous edge extends past the internal face of the spandrel/wall/
  column by a minimum length for positive-moment steel (or as close to the
  edge as possible if there's no spandrel/wall), and far enough to develop
  the calculated force (Cl 13.1) for negative-moment steel.

![[as3600-fig-9.1.3.4-two-way-flat-slab-reinforcement-arrangement.png]]
*Figure 9.1.3.4 — deemed-to-conform reinforcement arrangement for two-way
flat slabs designed by the Cl 6.10.4 idealized-frame-derived method
(AS 3600:2018).*

## Detail — Structural integrity reinforcement (Cl 9.2)

### General and minimum (Cl 9.2.1–9.2.2)

`[code]` Connections need reinforcement to resist progressive collapse at
walls/columns: at least two column-strip bottom bars/strands per direction
must pass within the column's longitudinal-reinforcement envelope, continuous
through interior supports and fully anchored beyond exterior-support faces.
The summed bottom-reinforcement area connecting slab/drop-panel/slab-band to
the column across the column periphery must be at least `2N*/fsy`, where
`N*` is the ULS column reaction from the floor slab — a direct
tie-force-to-reaction sizing rule, not a moment-based one. Not required
where beams with shear reinforcement and ≥2 continuous bottom bars frame into
the column from all spans.

`[code]` Minimum reinforcement in the secondary direction is also required
purely for load distribution (Cl 9.2.3) — shrinkage/temperature effects are
handled separately under Cl 9.5.3 (see [[concrete-slab-crack-control]]).

### Spacing (Cl 9.2.4)

`[code]` Minimum clear spacing per Cl 17.1.3 placement rules; maximum spacing
for crack control per Cl 9.5. Unreinforced prestressed slabs need transverse
reinforcement wherever the plain concrete between tendons can't safely
distribute load to them; absent supporting calculation, tendon spacing under
uniform load is capped at the lesser of 10× slab thickness and 1500 mm — tighter
near a supporting column where Cl 9.1.2's concentration rule may govern
instead.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-beam-strength-in-bending]] — the Cl 8.1 method this clause
  reuses.
- [[concrete-simplified-flexural-analysis]] — Cl 6.10.2/6.10.3/6.10.4, each
  paired with one of the three deemed-to-conform arrangements above.
- [[concrete-slab-punching-shear]] — the companion Section 9 strength check
  interacting with the Cl 9.1.2 reinforcement-concentration rule.
- [[concrete-slab-crack-control]] — Cl 9.5.3 shrinkage/temperature
  reinforcement, distinct from the Cl 9.2.3 load-distribution minimum.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clauses 9.1, 9.2 (Figures
  9.1.3.2, 9.1.3.4 reproduced as image assets above).
