---
title: Concrete fire resistance design — FRP method
category: 2-concrete
tags: [fire-resistance, frp, axis-distance]
standards: [AS 3600:2018 Cl 5.1-5.8]
status: draft
reviewed: 2026-09-12
---

# Concrete fire resistance design — FRP method

> Scope: how AS 3600 Section 5 establishes a fire resistance period (FRP) for
> beams, slabs, columns and walls, and how that period can be increased with
> insulating materials.

## Summary

`[code]` Section 5 sets minimum member dimensions and reinforcement/tendon
axis distances so a member achieves a required fire resistance level (FRL) —
structural adequacy, integrity and insulation periods, in that order, per the
BCA. Two routes are permitted (Cl 5.3.1): (a) read minimum dimensions/axis
distances off this section's tables/figures (no further shear/torsion/
anchorage check needed when using tabulated data, unless stated otherwise),
or (b) calculate the FRP by another method (e.g. the clause notes Eurocode 2
Part 1.2 as an accepted calculation method), in which case shear, torsion and
anchorage capacity must still be checked. Linear interpolation between
tabulated values is permitted (Cl 5.3.2) — some interpolation-only values in
the tables give covers *less* than durability/placement would otherwise
require, so don't read a table entry as a standalone minimum outside its
interpolation context.

## Detail

### Definitions and general rules (Cl 5.2–5.3)

`[code]` Key terms: **axis distance** `as` — distance from a bar/tendon
centreline to the nearest fire-exposed surface (a nominal value; no
tolerance allowance needed). **Average axis distance** `am` — an
area-weighted (or, for mixed steel strengths, strength-weighted) average
across multiple reinforcement layers (Cl 5.2.1 formula: `am = Σ(Asi·ai)/Σ(Asi)`,
extended to `Σ(Asi·fsyi·ai)/Σ(Asi·fsyi)` for mixed strengths). Reinforcement
and tendons present together (partially prestressed members) have their axis
distances assessed separately. **FRL** — the three periods (structural
adequacy, integrity, insulation) in that order. **FRP** — the tested/assessed
time to failure of the relevant criterion, per AS 1530.4 where the BCA
governs.

![[as3600-fig-5.2.1-average-axis-distance.png]]
*Figure 5.2.1 — average axis distance `am` across multiple reinforcement
layers (AS 3600:2018).*

![[as3600-fig-5.2.2-axis-distance-sections.png]]
*Figure 5.2.2 — axis distance `as` in typical beam/slab/column cross-sections
(AS 3600:2018).*

`[code]` Prestressing tendons need a larger axis distance than an equivalent
reinforcing bar would: +15 mm for strand/wire, +10 mm for bars (Cl 5.3.3),
applied on top of whatever the beam/slab/column/wall table gives for "bars".

`[code]` Dimensional limits (Cl 5.3.4): hollow-core slab/wall webs need
minimum concrete thickness around voids; ribbed slabs need rib spacing
≤ 1500 mm centre-to-centre, to be eligible for the tabulated method at all.
Joints (5.3.5) must not create a weak point below the assembly's required
FRL. Chases (5.3.6) are to be minimised; their effect on wall FRP specifically
is picked up in Cl 5.7.4.

### FRP for beams (Cl 5.4)

`[code]` Structural-adequacy FRP for beams in a roof/floor system comes from
tables/figures split by simply-supported vs. continuous, each giving
combinations of average axis distance `am` and beam width `b` at four
different width bands (own-words: a narrower beam needs a larger axis
distance for the same FRP, and vice versa — the table gives several valid
`(am, b)` combinations per period rather than one fixed pair). Applicability
requires the beam's top surface to be integral with or protected by a
conforming slab, a web of uniform or uniformly-tapering width, and
proportions within the tabulated range. A beam counts as "continuous" if it's
designed flexurally continuous at one or both ends under imposed action.
Four-sided fire exposure (rectangular beams not built into a slab) uses the
same tables but with additional proportioning rules on total depth and
cross-sectional area relative to the tabulated `b`.

![[as3600-fig-5.4.1a-frp-beams-simply-supported.png]]
*Figure 5.4.1(A) — beam cross-section geometry for the simply supported FRP
table, average axis distance `am` and width `b` (AS 3600:2018).*

![[as3600-table-5.4.1a-frp-simply-supported-beams.png]]
*Table 5.4.1(A) — FRPs for structural adequacy for simply supported beams,
combinations of average axis distance `am` and width `b` (AS 3600:2018).*

![[as3600-fig-5.4.1b-frp-beams-continuous.png]]
*Figure 5.4.1(B) — beam cross-section geometry for the continuous-beam FRP
table (AS 3600:2018).*

![[as3600-table-5.4.1b-frp-continuous-beams.png]]
*Table 5.4.1(B) — FRPs for structural adequacy for continuous beams, same
style as Table 5.4.1(A) (AS 3600:2018).*

### FRP for slabs (Cl 5.5)

`[code]` **Insulation** FRP depends only on effective thickness (Table 5.5.1)
— actual thickness for solid slabs, net area ÷ width for
hollow-core, solid thickness between webs for ribbed.

![[as3600-table-5.5.1-frp-insulation-slabs.png]]
*Table 5.5.1 — FRPs for insulation for slabs, by effective thickness
(AS 3600:2018).*

**Structural adequacy**
FRP is deemed satisfied by axis-distance tables split by slab type: solid/
hollow-core slabs on beams or walls (5.5.2(B), by one-way/two-way and support
condition), flat slabs/plates (5.5.2(A), with an added restriction near
column faces where depth can't be reduced by calculation), one-way ribbed
slabs (borrows beam rules for the rib itself, plus its own axis distance for
the flange), and two-way ribbed slabs, simply-supported (5.5.2(C)) or
continuous (5.5.2(D)), each needing rib width/axis-distance combinations plus
a separate flange thickness/axis-distance check.

![[as3600-table-5.5.2a-frp-flat-slabs.png]]
*Table 5.5.2(A) — FRPs for structural adequacy for flat slabs including flat
plates, slab thickness and axis distance (AS 3600:2018).*

![[as3600-table-5.5.2b-frp-solid-hollow-core-one-way-ribbed-slabs.png]]
*Table 5.5.2(B) — FRPs for structural adequacy for solid/hollow-core slabs
supported on beams or walls, and for one-way ribbed slabs, by span
condition and `ly/lx` (AS 3600:2018).*

![[as3600-table-5.5.2c-frp-two-way-simply-supported-ribbed-slabs.png]]
*Table 5.5.2(C) — FRPs for structural adequacy for two-way simply supported
ribbed slabs, axis distance/rib-width combinations plus flange thickness
(AS 3600:2018).*

![[as3600-table-5.5.2d-frp-two-way-continuous-ribbed-slabs.png]]
*Table 5.5.2(D) — FRPs for structural adequacy for two-way continuous ribbed
slabs, same style as Table 5.5.2(C) (AS 3600:2018).*

### FRP for columns (Cl 5.6)

`[code]` Insulation/integrity FRPs only matter for columns forming part of a
fire-separating wall (then use the wall rules, Cl 5.7.1). Structural adequacy
for **braced** columns uses one of two tabular methods:

- **Restricted tabular method** (5.6.3): valid within stated limits on load
  level `N*f/(φ·Nu)` (default 0.7 if not calculated), reinforcement
  distribution once `As/Ag` and FRP exceed thresholds, effective length under
  fire (<3 m), eccentricity (≤0.15b), and a longitudinal reinforcement ratio
  cap. Within those limits, Table 5.6.3 gives axis distance/dimension
  combinations by exposure condition (one-sided vs. multi-sided, at several
  load-level bands). Outside the table's numeric range but within stated
  variable bounds, a direct formula (Eq. 5.6.3(2)) is offered instead,
  combining axis-distance, effective-length, dimension and reinforcement-ratio
  terms — `[derived]` restate the formula's structure only; its specific
  coefficients are code-calibrated constants best read directly from the
  clause if used in a real calc.

![[as3600-table-5.6.3-frp-columns-restricted-method-1.png]]
![[as3600-table-5.6.3-frp-columns-restricted-method-2.png]]
*Table 5.6.3 — FRPs for structural adequacy of columns, restricted tabular
method, axis distance/dimension by exposure condition and load level
(AS 3600:2018).*

- **General tabular method** (5.6.4): valid within its own limits on
  eccentricity ratio, slenderness (≤30) and reinforcement distribution;
  Table 5.6.4 gives axis distance/dimension combinations keyed to a
  mechanical reinforcement ratio (`1.3·As·fsy/(Ag·f'c)`) at several bands, by
  FRP and load ratio.

![[as3600-table-5.6.4-frp-braced-columns-general-method-1.png]]
![[as3600-table-5.6.4-frp-braced-columns-general-method-2.png]]
*Table 5.6.4 — FRPs for structural adequacy of braced columns, general
tabular method, axis distance/dimension by mechanical reinforcement ratio
(AS 3600:2018).*

![[as3600-fig-5.6.4-columns-general-method-1.png]]
![[as3600-fig-5.6.4-columns-general-method-2.png]]
*Figure 5.6.4 — column cross-section geometry for the general tabular
method, axis distance and dimension parameters (AS 3600:2018).*

Columns outside either method's limits, or with a long/short side ratio
≥ 4:1, are directed to be treated as walls (Cl 5.7) or via a full performance
solution (Cl 5.3.1(b), BCA route).

### FRP for walls (Cl 5.7)

`[code]` Insulation FRP by effective thickness (Table 5.7.1, same style as
slabs).

![[as3600-table-5.7.1-frp-walls-insulation.png]]
*Table 5.7.1 — FRPs for walls for insulation, by effective thickness
(AS 3600:2018).*

Structural adequacy FRP by axis distance/thickness combinations
(Table 5.7.2), split by load ratio and one-sided vs. two-sided exposure.

![[as3600-table-5.7.2-frp-walls-structural-adequacy.png]]
*Table 5.7.2 — FRPs for structural adequacy for walls, axis distance/wall
thickness by load ratio and exposure (AS 3600:2018).*
Effective-height-to-thickness ratio is capped at 40 for any wall required to
carry an FRL (Cl 5.7.3), unless its top lateral support itself carries no
FRL requirement. Chases and recesses (Cl 5.7.4) are deemed to have no effect
on FRP below stated size/area thresholds; above those thresholds, the wall's
effective thickness for FRP purposes is reduced by the recess/chase depth
before re-checking against the same tables.

### Increasing FRP with insulating materials (Cl 5.8)

`[code]` FRP for insulation and/or structural adequacy can be increased by
adding an insulating material to the surface — acceptable forms include
gypsum-vermiculite/gypsum-perlite plaster (a stated mix ratio) or any other
material demonstrated equivalent by a standard fire test. Required thickness
is either determined by AS 1530.4 test, or — for the named plaster types only
— by a stated fraction (0.75) of the shortfall between the required and
actual cover/effective thickness, rounded up to the nearest 5 mm. Sprayed/
trowelled insulation thicker than 10 mm must itself be reinforced against
detachment in fire. Slab insulation periods specifically can also be
increased by a topping, with required topping thickness given by a formula
(`tnom = k·td + 10`) where `k` depends on topping material (plain concrete,
lightweight aggregate concrete, or gypsum) and `td` is the effective-thickness
shortfall against Table 5.5.1.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-durability-and-cover]] — cover is the *greater* of the Section 4
  and Section 5 requirements; this page only covers the Section 5 side.
- [[concrete-documentation-requirements]] — FRL is a required drawing/spec
  item (Cl 1.4).

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clauses 5.1–5.8 (numbered
  tables and Figures 5.2.1, 5.2.2, 5.4.1(A)/(B), 5.6.4 reproduced as image
  assets above).
