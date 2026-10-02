---
title: Crack control of beams
category: 2-concrete
tags: [beams, crack-control, crack-width]
standards: [AS 3600:2018 Cl 8.6]
status: draft
reviewed: 2026-09-12
---

# Crack control of beams

> Scope: AS 3600 Cl 8.6 — deemed-to-satisfy detailing, steel-stress limits,
> and direct crack-width calculation for reinforced and prestressed beams.

## Summary

`[code]` Cracking is normal and acceptable in reinforced concrete; the
question is limiting it to a chosen characteristic maximum crack width
`wmax` appropriate to the surface's function/exposure (Cl 8.6.1). For beams
fully enclosed in a building (bar weather exposure during construction) where
cracking won't impair function, only two deemed-to-satisfy detailing rules
apply; otherwise, add a steel-stress limit or a direct crack-width
calculation.

## Detail

### Baseline detailing (Cl 8.6.1)

`[code]` (a) minimum tensile reinforcement per Cl 8.1.6.1 (see
[[concrete-beam-strength-in-bending]]); (b) distance from beam side/soffit to
the nearest longitudinal bar centre ≤100 mm (ignoring bars smaller than half
the largest bar's diameter), and centre-to-centre bar spacing near a tension
face ≤300 mm — for T-/L-beams, flange reinforcement distributed across the
effective width. Under direct (axial) loading, calculated tensile steel
stress `σscr.1 ≤ 0.8fsy` regardless of which route below is used.

### Crack control without direct calculation (Cl 8.6.2.2)

`[code]` Split by whether the section is primarily in **tension** (whole
section in tension) or primarily in **flexure** (triangular tensile stress
distribution, cracking, part of section in compression):

- Tension: calculated steel stress `σscr` must not exceed the Table
  8.6.2.2(A) limit for the largest bar diameter in the section.
- Flexure: `σscr` must not exceed the *larger* of the Table 8.6.2.2(A) limit
  (by bar diameter) and the Table 8.6.2.2(B) limit (by bar spacing) — i.e.
  either a fine/close bar arrangement or a coarser/wider one can satisfy this,
  whichever the designer prefers.

`[derived]` Both tables are steel-stress-vs-crack-width grids (finer bars or
tighter spacing tolerate higher stress for the same crack width) — see below
for the actual stress limits at a chosen `wmax` (0.2/0.3/0.4 mm columns).

![[as3600-table-8.6.2.2a-max-steel-stress-beams-bar-diameter.png]]
*Table 8.6.2.2(A) — maximum steel stress for tension or flexure in reinforced
beams, by nominal bar diameter and `wmax` (AS 3600:2018).*

![[as3600-table-8.6.2.2b-max-steel-stress-beams-spacing.png]]
*Table 8.6.2.2(B) — maximum steel stress for flexure in reinforced beams, by
centre-to-centre bar spacing and `wmax` (AS 3600:2018).*

### Crack control by direct crack-width calculation (Cl 8.6.2.3)

`[code]` `w = sr,max·(εsm − εcm) ≤ wmax`, where `sr,max` is maximum crack
spacing and `(εsm − εcm)` is the difference between mean reinforcement strain
and mean concrete strain between cracks — itself a function of the cracked-
section steel stress `σscr`, the concrete's mean tensile strength, an
effective modular ratio `(1+φcc)·Es/Ec`, an effective tension-reinforcement
ratio `ρeff` (steel area over an effective tension-concrete area `Ac,eff`
bounded by a depth taken as the least of three geometric limits), and the
long-term shrinkage strain `εcs`. Maximum crack spacing, for reasonably
closely-spaced bonded reinforcement, is built from clear cover, an
equivalent bar diameter (area-weighted, for mixed bar sizes), `ρeff`, and two
empirical coefficients — one for bond quality (deformed vs. plain bars) and
one for the strain gradient (pure tension vs. bending vs. combined,
the combined case interpolating between the two boundary-strain values).

### Crack control for prestressed beams (Cl 8.6.3)

`[code]` Deemed controlled if maximum tensile stress under short-term
service loads stays within `0.25√f'c`; if exceeded, add reinforcement/bonded
tendons near the tensile face (spacing ≤300 mm) and satisfy **one** of:
limiting max flexural tensile stress to `0.6√f'c`; limiting the steel-stress
*increment* (from zero-tension-fibre load level up to short-term service
load) per Table 8.6.3; or a direct crack-width calculation
per Cl 8.6.2.3.

![[as3600-table-8.6.3-max-stress-increment-prestressed-beams.png]]
*Table 8.6.3 — maximum increment of steel stress for flexure in prestressed
beams, by nominal bar diameter and `wmax` (AS 3600:2018).*

### Side-face and opening/discontinuity crack control (Cl 8.6.4–8.6.5)

`[code]` Beams over 750 mm deep need side-face longitudinal reinforcement —
12 mm bars at 200 mm centres, or 16 mm bars at 300 mm centres, in each side
face (a skin-reinforcement requirement independent of the main flexural
steel). Openings and discontinuities need their own crack-control
reinforcement, without a prescribed formula — an engineering-judgement
clause.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-serviceability-design]] — Cl 2.3.3 parent cracking-control
  requirement this clause satisfies.
- [[concrete-beam-strength-in-bending]] — Cl 8.1.6.1 minimum reinforcement
  baseline.
- [[concrete-slab-crack-control]] — the equivalent slab clause (Cl 9.5),
  which reuses this clause's crack-width formula directly.
- [[concrete-properties-of-concrete]] — `εcs`, `φcc` inputs to the crack-width
  calculation.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 8.6 (Tables
  8.6.2.2(A), 8.6.2.2(B), 8.6.3 reproduced as image assets above).
