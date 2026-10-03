---
title: Simplified methods of flexural analysis
category: 0-standards
tags: [structural-analysis, simplified-method, coefficients, two-way-slabs]
standards: [AS 3600:2018 Cl 6.10]
status: draft
reviewed: 2026-09-12
---

# Simplified methods of flexural analysis

> Scope: AS 3600's coefficient-based shortcuts for continuous beams/one-way
> slabs, two-way slabs on four sides, and multi-span two-way slab systems
> (Cl 6.10) — used in lieu of a full elastic or idealized-frame analysis.

## Summary

`[code]` Cl 6.10.1: reinforced concrete beams and slabs may be designed for
strength using one of three coefficient-based methods (6.10.2–6.10.4)
instead of a full analysis, each gated by its own applicability conditions
(span-ratio limits, load pattern, load level, reinforcement layout). All
three ultimately express a design moment or shear as a **coefficient × a
reference load term** (e.g. `Fd·L²n` for one-way members); the coefficients
themselves are code-calibrated data — Cl 6.10.3 and 6.10.4 tables are
reproduced as image assets below, Cl 6.10.2's coefficients are not (no
single numbered table covers them; see the raw source).

## Detail

### Continuous beams and one-way slabs (Cl 6.10.2)

`[code]` Applicable (6.10.2.1) where: adjacent-span length ratio ≤ 1.2, loads
essentially uniform, imposed action ≤ 2×permanent action, uniform member
cross-section, and reinforcement arranged per Cl 8.1.10.6 (beams) or
Cl 9.1.3.2 (slabs). Within those limits:

- **Negative design moment** (6.10.2.2) at the critical section (support
  face) is a coefficient times `Fd·L²n`, with different coefficients for: the
  first interior support of a two-span member (further split by Ductility
  Class N vs. L), the first interior support with more than two spans, other
  interior supports, and interior faces of exterior supports (further split
  by whether the support is a column or a beam).
- **Positive design moment** (6.10.2.3): separate coefficients for an end
  span vs. an interior span (interior span further split by Ductility Class
  N vs. L).
- **Transverse design shear** (6.10.2.4): separate coefficients for an end
  span (at the interior support face, at midspan, at the end support face)
  vs. an interior span (at support faces, at midspan) — the end-span
  interior-support-face coefficient carries an explicit multiplier above the
  simple `Fd·Ln/2` baseline, reflecting the asymmetry of an end span.

### Two-way slabs supported on four sides (Cl 6.10.3)

`[code]` Applicable (6.10.3.1) where: loads essentially uniform,
reinforcement per Cl 9.1.3.3, support moments arise only from applied load
(not restraint), openings don't adversely affect strength/stiffness, and any
Ductility Class L slab is continuously wall-supported. Corners must be
prevented from lifting.

- **Positive design moments** at midspan in each direction come from
  `M* = coefficient × Fd·L²` (short-span and long-span coefficients,
  Cl 6.10.3.2(1)/(2)), read from Table 6.10.3.2(A) (Ductility Class N,
  9 edge-condition rows × span-ratio columns) or Table 6.10.3.2(B) (N or L
  mesh, similar structure but no moment redistribution credit at either limit
  state). Moments apply over the central
  three-quarters of each span; outside that, only the Cl 9.1.1 minimum
  strength applies.

![[as3600-table-6.10.3.2a-bending-moment-coefficients-class-n.png]]
*Table 6.10.3.2(A) — bending moment coefficients for rectangular slabs
supported on four sides, Ductility Class N reinforcement, by edge condition
and span ratio (AS 3600:2018).*

![[as3600-table-6.10.3.2b-bending-moment-coefficients-class-n-or-l.png]]
*Table 6.10.3.2(B) — bending moment coefficients for rectangular slabs
supported on four sides, Ductility Class N or L reinforcement
(AS 3600:2018).*
- **Negative design moments** at a continuous edge are a fixed multiple of
  the midspan value when using Table (A), or the same table's own
  coefficient when using Table (B); unbalanced moment at a common support
  either redistributes by adjacent-panel stiffness (Ductility Class N) or
  requires reinforcing both sides for the larger moment.
- **Discontinuous-edge negative moment**: a fixed fraction of the midspan
  value, again differing between Table (A) and Table (B) conventions.
- **Torsional moment at exterior corners** (6.10.3.3): deemed resisted by
  conforming with Cl 9.1.3.3(e) corner-reinforcement requirements.
- **Load allocation to supports** (6.10.3.4): tributary-area-style
  allocation to supporting beams/walls (Figure 6.10.3.4, reproduced below),
  with a stated 10% increase on continuous-edge reactions and 20% decrease
  on a discontinuous-edge reaction when one edge is discontinuous; adjacent
  discontinuous edges are handled by separate per-span elastic-shear
  adjustment instead.

![[as3600-fig-6.10.3.4-load-allocation.png]]
*Figure 6.10.3.4 — tributary-area load allocation from a two-way slab to
its supporting beams/walls (AS 3600:2018).*

### Multi-span two-way slab systems (Cl 6.10.4)

`[code]` Applicable (6.10.4.1) to solid slabs (with/without drop panels),
two-way ribbed (waffle) slabs, and beam-and-slab systems with thickened slab
bands, where: at least two continuous spans each way, a near-rectangular
support grid (offsets ≤10% of span), successive span lengths within one-third
of each other with no end span longer than its adjacent interior span,
lateral force resisted by shear walls/braced frames (i.e. not by slab-column
frame action), uniform vertical load, imposed action ≤ 2×permanent action,
reinforcement per Cl 9.1.3.4/8.1.11.6, and no Ductility Class L flexural
reinforcement.

`[code]` **Total static moment** for a span (6.10.4.2):
`Mo = Fd·Lt·L²o / 8` (a direct formula, not a table) — the standard
"total statical moment" concept familiar from other two-way-slab design
methods. **Design moments** (6.10.4.3) split `Mo` into exterior-negative/
positive/interior-negative shares via factor tables for end spans
(6.10.4.3(A), further split by exterior-edge restraint condition — free,
column-only, spandrel-beam-and-column, or fully restrained/beam-and-slab)
and interior spans (6.10.4.3(B), a single factor pair for all system types);
up to 10% redistribution between these design moments
is allowed provided `Mo` itself for that span isn't reduced.

![[as3600-table-6.10.4.3a-design-moment-factors-end-span.png]]
*Table 6.10.4.3(A) — design moment factors for an end span, by exterior-edge
restraint condition (AS 3600:2018).*

![[as3600-table-6.10.4.3b-design-moment-factors-interior-span.png]]
*Table 6.10.4.3(B) — design moment factors for an interior span
(AS 3600:2018).* Where two spans
frame into a common support with different negative moments, the larger
governs unless stiffness-based redistribution is used. **Transverse
distribution** (6.10.4.4) to column/middle strips reuses Cl 6.9.5.3 (see
[[as3600-idealized-frame-method]]). **Moment transfer for shear at flat
slabs** (6.10.4.5): the unbalanced moment transferred to an interior support
has its own minimum formula (Eq. 6.10.4.5, combining factored dead/live load
terms across adjoining spans); exterior supports use the actual moment
directly. Beam shear in beam-and-slab construction may use rigorous
calculation or the Cl 6.10.3.4 load-allocation shortcut. **Openings**
(6.10.4.7) are restricted to the same size/position rules as Cl 6.9.5.5(a)/(b)
— the third (column-strip-interior) opening allowance from the idealized
frame method does **not** carry over to this simplified method.

## Worked reference

None yet — a strong candidate for the first `Worked reference` in this wiki
once a human supplies an actual span/load case, since the method is
explicitly a "plug numbers into a coefficient" workflow.

## Contradictions

None recorded.

## Related

- [[as3600-idealized-frame-method]] — the fuller method this simplifies;
  shares column/middle-strip distribution (Cl 6.9.5.3) and opening rules.
- [[as3600-limit-state-design-basis]] — Cl 2.5 load combinations feeding
  `Fd`.
- [[as3600-structural-analysis-overview]] — parent method menu.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 6.10 (Tables
  6.10.3.2(A)/(B) and 6.10.4.3(A)/(B), and Figure 6.10.3.4, reproduced as
  image assets above; the Cl 6.10.2 continuous-beam/one-way-slab
  coefficients remain un-reproduced — no single numbered table exists for
  that sub-clause).
