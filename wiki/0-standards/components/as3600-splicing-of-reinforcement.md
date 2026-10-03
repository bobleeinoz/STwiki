---
title: Splicing of reinforcement — lapped, welded and mechanical splices
category: 0-standards
tags: [splicing, lap-length, mesh, bundled-bars, mechanical-splices]
standards: [AS 3600:2018 Cl 13.2]
status: draft
reviewed: 2026-09-16
---

# Splicing of reinforcement

> Scope: AS 3600 Cl 13.2 — general splicing rules, tensile and compressive
> lap lengths, mesh laps, bundled-bar laps, and welded/mechanical splices.

## Summary

`[code]` Cl 13.2.1 sets general rules: splices only where shown/permitted on
drawings; made by welding, mechanical means, end-bearing or lapping; tension
splices in tension-tie members restricted to welding or mechanical means;
lapped splices barred for bars >40 mm diameter in tension or compression;
welding kept ≥3db from a bent-and-restraightened region of a bar.

## Detail

### Lapped splices for bars in tension (Cl 13.2.2)

`[code]` In **wide** elements/members (flanges, band beams, slabs, walls,
blade columns) with bars lapped in the plane of the member, the tensile lap
length is `Lsy.t.lap = k7 Lsy.t ≥ 0.058 fsy k1 db`, where `Lsy.t` is the Cl
13.1.2.1 development length (the `0.058 fsy k1` floor in Eq 13.1.2.2 is
suspended for this use), and `k7 = 1.25` unless the area of steel provided is
at least twice that required **and** no more than half the reinforcement at
the section is spliced, in which case `k7 = 1.0`.

`[code]` In **narrow** elements/members (beam webs, columns), `Lsy.t.lap` is
not less than the largest of `0.058 fsy k1 db`, `k7 Lsy.t`, and `Lsy.t +
1.5sb`, where `sb` is the clear distance between the lapped bars (Figure
13.2.2) — taken as zero if `sb ≤ 3db`.

![[as3600-fig-13.2.2-cd-lapped-splices.png]]
*Figure 13.2.2 — value of `cd` for lapped splices: (i) 100% of bars spliced,
no stagger, `cd = min(a/2, c)`; (ii) 50% staggered splices, adjacent splice
starts offset by ≥`0.3 Lsy.t.lap` (AS 3600:2018).*

### Lapped splices for mesh in tension (Cl 13.2.3)

`[code]` A mesh lap must place the two outermost cross-bars of the lapped
sheet beyond the two outermost cross-bars of the sheet being lapped, spaced
≥100 mm (plain) / ≥50 mm (deformed) apart, with a minimum 100 mm overlap.
Mesh with no cross-bars inside the splice length is spliced per Cl 13.2.2
instead.

![[as3600-fig-13.2.3-lapped-splices-mesh.png]]
*Figure 13.2.3 — lapped splices for welded mesh: (a) equal cross-bar spacing
`s1 = s2`; (b) unequal spacing `s1 < s2` (AS 3600:2018).*

### Lapped splices for bars in compression (Cl 13.2.4)

`[code]` Minimum lap length = the Cl 13.1.5 compression development length,
not less than 300 mm, taken as:
(a) `Lsy.c` per Cl 13.1.5, not less than `40db`;
(b) in fitmented compression members with ≥3 fitment sets over the lap and
`Atr/s ≥ Ab/1000` — 0.8× (a);
(c) in helically-tied members with ≥3 helix turns over the lap and `Atr/s ≥
n·Ab/6000` (`n` = bars around the helix) — 0.8× (a).
`Ab` here is the area of the bar being spliced.

### Bundled bars and welded/mechanical splices (Cl 13.2.5–13.2.6)

`[code]` Bundled-bar laps use the largest bar's lap length, increased 20%
(3-bar bundle) or 33% (4-bar bundle); individual bar splices within a bundle
must not overlap each other.

`[code]` Welded or mechanical splices between Ductility Class N bars must not
fail prematurely (in tension or compression) ahead of the bars themselves,
unless the member's strength/ductility is shown to meet design requirements
regardless. Where crack control or vertical deflection governs, excessive
longitudinal slip in a proprietary mechanical connector must be assessed if
tests show slip could exceed 0.1 mm at 300 MPa tensile stress — slip is the
gauge-length (`12db`) deformation of the spliced pair, less the equivalent
unspliced elongation.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-development-length-of-reinforcement]] — Cl 13.1, the
  development lengths this section's `k7`-factored laps build on.
- [[as3600-earthquake-structural-walls-detailing]] — Section 14.6.7/14.7.3,
  staggered-lap arrangement referencing Figure 13.2.2 for ductile walls.
- [[as3600-diaphragm-design]] — Cl 15.4.4, collector splicing limited to
  full-yield-strength splice lengths from this section.
- [[as3600-column-reinforcement-detailing]] — Cl 10.7, column bar splicing
  context.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 13.2 (Figures
  13.2.2 and 13.2.3 reproduced in `wiki/0-standards/assets/`).
