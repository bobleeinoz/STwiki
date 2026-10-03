---
title: Development length of reinforcing bars and welded mesh
category: 0-standards
tags: [development-length, anchorage, hooks-cogs, headed-bars, welded-mesh]
standards: [AS 3600:2018 Cl 13.1]
status: draft
reviewed: 2026-09-16
---

# Development length of reinforcing bars and welded mesh

> Scope: AS 3600 Cl 13.1 — development length of deformed and plain bars in
> tension and compression, headed bars, bundled bars, and welded mesh.

## Summary

`[code]` Cl 13.1.1 requires the calculated force in reinforcement to be
developed on each side of any cross-section by bond (or a mechanical
anchorage such as a hook, cog or head) over a defined development length.
This page covers the calculation routes in Cl 13.1.2–13.1.8; splicing
(lapped/welded/mechanical) is a separate topic — see
[[as3600-splicing-of-reinforcement]].

## Detail

### Basic development length in tension (Cl 13.1.2.2)

`[code]` The basic tensile development length of a deformed bar is

`Lsy.tb = (0.5 k1 k3 fsy) / (k2 √f'c) · db`, not less than `0.058 k1 fsy db`

where `k1 = 1.3` for a horizontal bar with >300 mm of concrete cast below it,
otherwise `1.0`; `k2 = (132 − db)/100`; `k3 = 1.0 − 0.15(cd − db)/db`, bounded
`0.7 ≤ k3 ≤ 1.0`, with `cd` read from Figure 13.1.2.2 (concrete cover/bar
spacing term, distinct definitions for narrow members, wide members, and
staggered bar layouts). `f'c` is capped at 65 MPa in this equation. `Lsy.tb`
is multiplied by 1.5 for epoxy-coated bars and by 1.3 where lightweight
concrete is used.

![[as3600-fig-13.1.2.2-values-of-cd.png]]
*Figure 13.1.2.2 — values of `cd`: (i) narrow members (beam webs, columns) for
straight/cogged-or-hooked/looped bars; (ii) wide members (flanges, band
beams, slabs, walls, blade columns), same three bar-end cases; (iii) planar
view of staggered development lengths of equi-spaced bars (AS 3600:2018).*

### Refined development length in tension (Cl 13.1.2.3)

`[code]` A shorter, refined length is permitted: `Lsy.t = k4 k5 Lsy.tb`, with
`k4 = 1.0 − Kλ` and `k5 = 1.0 − 0.04ρp`, each bounded `0.7–1.0`, and the
product `k3 k4 k5 ≥ 0.7`. `K` is the weighted-average effectiveness of
transverse reinforcement crossing the splitting-crack plane: `K = 0.05(1 +
nf/nbs) ≤ 0.10` (`nf`/`nbs` from Table 13.1.2.3 by member type/layout), taken
as `0` if the transverse steel is not between the longitudinal bars and the
tensile face. `λ = (ΣAtr − ΣAtr.min)/As ≥ 0` (`ΣAtr` = summed transverse-bar
area along the development/lap length, `ΣAtr.min = 0.25As` for beams/columns
or `0` for slabs/walls, `As` = area of the single bar being anchored).
`ρp` is the transverse compressive pressure (MPa) perpendicular to the
splitting plane at the ULS.

| Member type | `nf` | `nbs` | `K` |
| --- | --- | --- | --- |
| Circular column | 1 | 1 | 0.10 |
| Rectangular column | 1 | 1 | 0.05–0.10 |
| Beam | 1 | 1 | 0.05–0.10 |
| Slab or wall (with fitments) | 1 | 1 | 0.05–0.10 |
| Slab or wall (without fitments) | 0 | 1 per main-bar spacing | 0.05 |

`[code]` `nf`/`nbs` are the number of potential splitting-crack faces at the
tensile face / transverse bars per face for the arrangement shown (Table
13.1.2.3, Note 2: the resulting `K` is a weighted average across all
anchored/spliced bars at the section).

![[as3600-table-13.1.2.3-k-values-transverse-reinforcement.png]]
*Table 13.1.2.3 — values of K for typical arrangements of transverse
reinforcement for different member types, with worked `nf`/`nbs` examples
(AS 3600:2018).*

### Reduced development for partial stress, curves, hooks/cogs (Cl 13.1.2.4–13.1.2.7)

`[code]` To develop a tensile stress `σst < fsy`: `Lst = (σst/fsy)·Lsy.t`, not
less than `12db` (or the Cl 9.1.3.1(a)(ii) slab minimum). A bar is deemed
developed around a curve if the internal bend diameter is `≥10db`.

`[code]` For a bar ending in a standard hook or cog (Cl 13.1.2.7), the
tensile development length measured from the outside of the hook/cog is
`0.5 Lsy.t` (using `σst` and `Lst` from Cl 13.1.2.4 where full yield is not
required). Where `σst > 400 MPa` the hook/cog must enclose a transverse bar
of diameter `≥ db` in contact with the bend, extending `≥4db` each side.

![[as3600-fig-13.1.2.6-hook-cog-development-length.png]]
*Figure 13.1.2.6 — development length of a deformed bar with a standard hook
(180°/135° bend + straight extension) or standard cog (90° bend), each
measured as `0.5 Lsy.t` from the outside of the bend (AS 3600:2018).*

`[code]` Standard hooks/cogs (Cl 13.1.2.7): (a) 180° bend, internal diameter
per Cl 17.2.3.3, plus a straight extension of `4db` or 70 mm (greater); (b)
135° bend, same diameter/length as (a); (c) 90° cog, internal diameter per
Cl 17.2.3.3 but `≤8db`, with the same total length as an equivalent 180°
hook.

### Plain bars and headed bars (Cl 13.1.3–13.1.4)

`[code]` Plain bars in tension: `Lsy.t` = the Cl 13.1.2.2 basic length × 1.5,
not less than 300 mm; a hooked/cogged plain bar develops `0.5 Lsy.t` (or
`0.5 Lst`) as for deformed bars.

`[code]` A head (forged, or a welded/threaded/swaged nut or plate) develops a
deformed bar in tension over `Lsy.hb` measured from the inside face of the
head, provided `Ahead ≥ 4Abar`, `db ≤ 40 mm`, clear cover `≥2db`, and clear
bar spacing `≥4db`: `Lsy.hb = 0.5 Lsy.t` at `Ahead/Abar = 4`, `Lsy.hb = 6db` at
`Ahead/Abar ≥ 10`, linearly interpolated between. Concrete-cone failure
between the head and a nearby free surface must be checked where bearing
forces are directed toward it.

### Compression, bundled bars, welded mesh (Cl 13.1.5–13.1.8)

`[code]` Deformed bar in compression — basic length `Lsy.cb = 0.22 fsy db /
√f'c` (not less than `0.0435 fsy db` or 200 mm, whichever governs); refined
length `Lsy.c = k6 Lsy.cb`, with `k6 = 0.75` where ≥3 transverse bars are
provided within `Lsy.cb` and `Atr/s ≥ As/600`, otherwise `k6 = 1.0`. Partial
stress: `Lsc = (σsc/fsy)·Lsy.c ≥ 200 mm`. Hooks/bends are **not** effective
in compression. Plain bars in compression: twice the deformed-bar `Lsy.c` or
`Lsy.cb`.

`[code]` Bundled bars: development length = that of the largest bar in the
bundle, increased 20% for a 3-bar bundle, 33% for a 4-bar bundle.

`[code]` Welded mesh in tension (Cl 13.1.8): with ≥2 cross-bars within the
development length (spaced ≥100 mm plain / ≥50 mm deformed, first ≥50 mm from
the critical section), yield is deemed developed. With one cross-bar, `Lsy.tb
= 3.25 Ab fsy /(sm √f'c)`, not less than 150 mm (plain) / 100 mm (deformed).
With no cross-bars, use the bar development rules of Cl 13.1.2/13.1.3.
Partial-stress mesh length scales by `σst/fsy` as for bars, same minima.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-splicing-of-reinforcement]] — Cl 13.2, lap/weld/mechanical
  splices built on the development lengths defined here.
- [[as3600-development-of-tendons-and-coupling]] — Cl 13.3–13.4, the
  parallel provisions for tendons.
- [[as3600-beam-detailing]] — Cl 8.3, curtailment/anchorage rules that cite
  Cl 13.1.2.7 and Cl 13.1.4 directly.
- [[as3600-column-reinforcement-detailing]] — Cl 10.7, splicing and
  restraint of column bars.
- [[as3600-earthquake-imrf-detailing]] — Section 14.5, ductile-frame
  detailing that tightens some of these anchorage requirements.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 13.1 (Figures
  13.1.2.2 and 13.1.2.6, and Table 13.1.2.3, reproduced in
  `wiki/0-standards/assets/`; the companion Figure 13.1.2.3 [K by bar
  position] is not yet reproduced).
