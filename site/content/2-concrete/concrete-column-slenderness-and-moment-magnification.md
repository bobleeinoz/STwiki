---
title: Column slenderness, short/slender classification and moment magnification
category: 2-concrete
tags: [columns, slenderness, moment-magnifier, effective-length, buckling]
standards: [AS 3600:2018 Cl 10.3, AS 3600:2018 Cl 10.4, AS 3600:2018 Cl 10.5]
status: draft
reviewed: 2026-09-12
---

# Column slenderness and moment magnification

> Scope: AS 3600 Cl 10.3 (short-column test and small-force/small-moment
> shortcuts), Cl 10.4 (moment magnifier for braced/unbraced slender columns
> and the buckling load `Nc`), and Cl 10.5 (slenderness ratio limit, radius
> of gyration, effective length).

## Summary

`[code]` A column is **short** (Cl 10.3.1) if its slenderness ratio `Le/r`
stays below a threshold: a fixed limit for unbraced columns (22), and for
braced columns the *greater* of a fixed limit (25) or a moment-ratio-
dependent expression that relaxes as the end-moment ratio `M1*/M2*` becomes
more favourable (double curvature) and tightens as axial load ratio
`N*/Nuo` rises — with a different formula split depending on whether
`N*/Nuo` is above or below 0.15. Everything not short is **slender** and
needs Cl 10.4's moment magnification on top of Cl 10.3/10.6/10.7.

## Detail

### Short-column test details (Cl 10.3.1)

`[code]` `M1*/M2*` is the ratio of smaller to larger end moment — negative
for single curvature, positive for double curvature; taken as 1.0 (i.e. the
least favourable, single-curvature-like assumption) if `|M2*| ≤ 0.05·D·N*`
(i.e. once the end moment is small enough to be dominated by the Cl 10.1.2
minimum-moment floor, the ratio stops being a meaningful discriminator).
`Le` per Cl 10.5.3, or simplified defaults: `Lu` for a braced column
restrained by a flat-slab floor, `0.9Lu` for one restrained by beams.

### Short columns with small force or moment (Cl 10.3.2)

`[practice]` Where `N* < 0.1·f'c·Ag`, the section may be designed for bending
only (axial force effectively ignored). Separately, an interior column in a
braced rectangular framed building may have its bending moments disregarded
entirely — provided a specific bundle of conditions holds (span-ratio ≤1.2,
essentially uniform load, imposed ≤ 2×permanent, uniform cross-section,
symmetric reinforcement) — in which case design axial strength is capped at
`0.75·φNuo`, a blunt but conservative simplification for genuinely
axial-dominated interior columns.

### Moment magnifier (Cl 10.4)

`[code]` Additional slenderness moment = largest design moment × magnifier
`δ`. For bending about both principal axes, each axis gets its own `δ` using
that axis's own restraint conditions. Additional end moments from
magnification may be found by rational calculation or distributed to joint
members in proportion to stiffness.

- **Braced column** (10.4.2): `δ = δb = km/(1 − N*/Nc) ≥ 1`, where `km`
  depends on the end-moment ratio (a `0.6 + 0.4·M1*/M2*` form, floored at
  0.4) but is taken as 1.0 outright wherever the column carries significant
  transverse load between its ends (absent more exact calculation) — since
  the end-moment-ratio logic doesn't represent a mid-height-loaded column
  well.
- **Unbraced column** (10.4.3): `δ` is the *larger* of `δb` (as if braced,
  per 10.4.2) and a storey/sway magnifier `δs`, calculated either per-column
  (`1/(1 − N*/Nc)`) or as a single frame-wide value from a rigorous elastic
  critical-buckling analysis — the frame-wide form uses a stability index
  built from the dead/live load ratio (floored at zero once slenderness or
  axial-load/moment ratios are low enough that second-order sway effects are
  negligible), a fixed correlation factor, and the frame's overall buckling-
  load ratio (computed using reduced flexural stiffnesses — a fraction of
  gross `EI` for both beams/slabs and columns, distinctly *lower* fractions
  than the Cl 6.2.4.2 general-analysis stiffness table since this is
  specifically a stability calculation). The frame must be proportioned so
  no column's `δs` exceeds 1.5 — above that, the frame is considered too
  sway-sensitive for this simplified approach.

### Buckling load `Nc` (Cl 10.4.4)

`[code]` `Nc` is an Euler-type buckling load, built from effective length
`Le`, a factor `d` reflecting long-term (sustained-load creep) softening,
and a moment capacity term `Mc` evaluated at a fixed neutral-axis parameter
`ku = 0.545` (own-words: `Mc` is the section's bending capacity at a
reference ductility/curvature state used specifically for the buckling-load
calculation, not the section's actual ultimate moment capacity `Muo`).

### Slenderness ratio limit and section properties (Cl 10.5)

`[code]` `Le/r` capped at 120 outright, unless a rigorous analysis (Cl 6.4,
6.5 or 6.6) is used with design per Cl 10.2.3 instead. **Radius of
gyration** `r`: `0.3D` for a rectangular section, `0.25D` for circular,
always on the *gross* section. **Effective length** `Le = k·Lu`, with `k`
read from standard alignment charts for simple end restraints, or derived
more generally from end-restraint coefficients:

- **Regular rectangular framed structures** (10.5.4): `k` from an
  end-restraint-coefficient chart, where each end's coefficient is the ratio
  of column-stiffness-sum to beam/slab-stiffness-sum at that joint, the
  beam/slab term itself scaled by a fixity factor (Table 10.5.4 — higher for
  a beam rigidly connected to another column at its
  far end, lower for a pinned far end) accounting for restraint conditions
  at the beam's far end.

![[as3600-table-10.5.4-fixity-factor.png]]
*Table 10.5.4 — fixity factor (kf) by restraint condition at the beam/slab's
far end, for regular rectangular framed structures (AS 3600:2018).*
- **Any framed structure** (10.5.5): a more general ratio of column
  stiffness to the sum of all other framing-member stiffnesses at the joint,
  explicitly accounting for far-end fixity and axial-compression-reduced
  stiffness in those other members.
- **Footing restraint** (10.5.6): a footing giving negligible rotational
  restraint is theoretically infinite but taken as 10 for chart purposes; one
  specifically designed to prevent rotation is theoretically zero but taken
  as 1.0 unless analysis justifies less.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-column-design-basis]] — Cl 10.1/10.2 parent design procedure.
- [[concrete-column-strength-interaction]] — Cl 10.6, where the magnified
  moment from this page is ultimately checked against section capacity.
- [[concrete-elastic-analysis-methods]] — Cl 6.2.4.2 stiffness table, distinct
  from (and less conservative than) the stability-specific stiffness
  fractions used in `δs`'s frame-wide form here.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clauses 10.3–10.5 (Figures
  10.5.3(A)/(B)/(C) and Table 10.5.4 reproduced as image assets).
