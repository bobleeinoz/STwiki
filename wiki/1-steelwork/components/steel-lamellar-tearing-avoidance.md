---
title: Selection of materials for the avoidance of lamellar tearing
category: 1-steelwork
tags: [lamellar-tearing, through-thickness-ductility, z-quality, weld-shrinkage, ndt]
standards: [AS 4100:2020 App M]
status: draft
reviewed: 2026-09-13
---

# Selection of materials for the avoidance of lamellar tearing

> Scope: AS 4100:2020 Appendix M (informative) — the design procedure for
> checking a joint's lamellar-tearing risk and selecting through-thickness
> (Z-quality) material: the `Z_Ed ≤ Z_Rd` criterion, the `Z_Ed` scoring
> table (Table M.2, adapted with permission from EN 1993-1-10), and NDE
> guidance. The Z-quality grade suffixes and minimum reduction-in-area
> requirements themselves are on
> [[steel-materials-and-design-strengths]] (Cl 2.2.5, Table 2.2.5); the
> mandatory Cl 3.8 detailing requirement is on
> [[steel-limit-state-design-basis]].

## Summary

`[code]` Lamellar tearing is a weld-induced flaw from restrained
through-thickness shrinkage strain as weld metal cools — the main risk is
in cruciform, T- and corner joints with complete-penetration welds
(Cl M.1). Risk is minimal if:

`Z_Ed ≤ Z_Rd` — Eq M.2.1

`Z_Ed` = the required design Z-value from the magnitude of restrained-
shrinkage strain; `Z_Rd` = the material's available design Z-value per
AS/NZS 3678 (Z15, Z25 or Z35 — see [[steel-materials-and-design-strengths]]
Table 2.2.5).

## Detail

### Background (Cl M.1)

`[code]` Susceptibility is measured by through-thickness ductility per
AS/NZS 3678, expressed as quality classes identified by Z-values. Further
guidance: Weld Australia Technical Note 6.

### Procedure (Cl M.2)

`[code]` `Z_Ed = Z_a + Z_b + Z_c + Z_d + Z_e` — Eq M.2.2, summing five
scored contributions from Table M.2. Welding details should be adjusted to
minimise `Z_Ed` where practical.

`[code]` **Table M.2 — criteria affecting the target value of `Z_Ed`**
(adapted, with permission, from Table 3.2 of EN 1993-1-10; © 2005 CEN,
Belgium, www.cen.eu):

![[as4100-table-M.2-part1.png]]
![[as4100-table-M.2-part2.png]]
*Table M.2 — criteria affecting the target value of Z_Ed (AS 4100:2020, adapted from EN 1993-1-10 Table 3.2, © CEN).*

Own summary of the five contributions:

- **(a) `Z_a` — effective weld depth `S` relevant for shrinkage straining**
  (see Figure M.2 for `S`): `Z_a = 0` for `S ≤ 7 mm`, rising in steps to
  `Z_a = 15` for `S > 50 mm` (values 0, 3, 6, 9, 12, 15, 15 at the 7/10/20/
  30/40/50 mm breakpoints).
- **(b) `Z_b` — shape and position of welds** in T-/cruciform/corner
  connections: single-run fillet or partial-penetration details around
  `Z_b = −25` to `−5` (least restraint); multi-run fillet welds `Z_b = 0`;
  partial/full-penetration welds with a welding sequence chosen to reduce
  shrinkage `Z_b = 3`; ordinary partial/full-penetration welds `Z_b = 5`;
  corner joints `Z_b = 8` (or `Z_b = −10` for a particular corner-joint
  detail per the table).
- **(c) `Z_c` — effect of material thickness `t` on restraint to
  shrinkage**: `Z_c` rises from `2` (`t ≤ 10 mm`) to `15` (`t > 70 mm`) in
  10 mm steps (2, 4, 6, 8, 10, 12, 15) — **may be reduced by 50%** for
  material stressed through-thickness in **compression** under
  predominantly static loads (footnote a).
- **(d) `Z_d` — remote restraint of shrinkage** by other parts of the
  structure: `Z_d = 0` (low restraint, free shrinkage possible, e.g.
  T-joints); `Z_d = 3` (medium restraint, e.g. diaphragms in box girders);
  `Z_d = 5` (high restraint, free shrinkage not possible, e.g. stringers in
  orthotropic deck plates).
- **(e) `Z_e` — influence of preheating**: `Z_e = 0` without preheating;
  `Z_e = −8` with preheating ≥ 100 °C.

![[as4100-fig-M.2-effective-weld-depth.png]]
*Figure M.2 — effective weld depth S for shrinkage: single fillet/partial-penetration weld (left), double fillet weld (right) (AS 4100:2020).*

### Non-destructive examination (Cl M.3)

`[code]` For high-risk fabrications, fabricators may usefully ultrasonically
scan plates before welding to locate internal discontinuities (e.g.
non-metallic inclusions). Scanning sensitivity per AS 2207 (gain set so the
second back-wall echo reaches full screen height). Where reflectors give
echoes ≈ 25% of plate thickness or higher, consider relocating welds away
from those areas, or turning the plate over so critical welds are placed on
the side furthest from the indications.

`[code]` Discontinuities later found in the weld heat-affected zone are
**not** a cause for weld rejection if of parent-metal origin (AS/NZS
1554.1:2014 Cl 6.2.2). Ultrasonic examination will not typically detect the
inclusions normally associated with lamellar tearing (e.g. manganese
sulphides), and such indications are not themselves an indicator of
through-thickness ductility.

## Worked reference

`[derived]` A 40 mm cruciform full-penetration T-joint (`S ≈ 40 mm`,
tension-loaded, medium remote restraint, no preheat): `Z_a ≈ 12`
(30–40 mm band), `Z_b = 5` (ordinary full-penetration weld), `Z_c ≈ 8`
(30 < t ≤ 40 mm band, no compression reduction since in tension), `Z_d = 3`
(medium restraint), `Z_e = 0` (no preheat) → `Z_Ed ≈ 28`. Against
`Z_Rd` options of Z15/Z25/Z35, this needs **Z35** material — illustrative
only, always work through the actual joint geometry against Table M.2.

## Contradictions

None recorded.

## Related

- [[steel-materials-and-design-strengths]] — Table 2.2.5 Z-quality grade
  suffixes (Z15/Z25/Z35) and minimum reduction-in-area; Cl 2.2.5 exemption
  (`Z_Ed ≤ 10` or thickness ≤ 16 mm).
- [[steel-limit-state-design-basis]] — Cl 3.8, the mandatory design/
  detailing/material-selection requirement this appendix supports.
- [[steel-weld-design]] — weld geometry (T-, cruciform, corner joints) that
  this appendix's `Z_b` scoring addresses.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Appendix M
  (pp. 212–214). Table M.2 is adapted with permission from EN 1993-1-10
  Table 3.2 (© 2005 CEN, Belgium) — reproduced here as it appears in the
  AS 4100:2020 reprint, with that attribution retained.
