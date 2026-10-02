---
title: Fatigue detail categories — non-welded, welded, bolted and hollow-section details
category: 1-steelwork
tags: [fatigue, detail-category, s-n-curve, weld-detail, bolt-detail, hollow-section-joint]
standards: [AS 4100:2020 Cl 11.5]
status: draft
reviewed: 2026-09-13
---

# Fatigue detail categories

> Scope: AS 4100:2020 Cl 11.5 — the detail-category classification tables
> (Tables 11.5.1(A)–(D)) that assign a numeric fatigue "detail category"
> (the S-N curve reference stress at 2×10⁶ cycles, in MPa) to specific
> constructional details, by group: 1 non-welded, 2 welded (not hollow
> sections), 3 bolts, 4 welded hollow-section details. Governing design
> theory (S-N formulae, exemptions, assessment) is on
> [[steel-fatigue-design]].

## Summary

`[code]` Every member, connection or detail subject to fatigue loading is
assigned a **detail category** — a number (e.g. 160, 125, 112, 90, 80, 71,
63, 56, 50, 45, 40, 36) equal to its fatigue strength `f_rn` at the
reference number of cycles `n_r = 2×10⁶` (Cl 11.1.2). Higher numbers = more
fatigue-resistant details. An unclassified detail takes the **lowest**
category of a similar detail, unless a higher category is proven by testing
(or analysis + testing) (Cl 11.5.1).

`[code]` Four groups (Cl 11.5.1): **Group 1** non-welded (Table 11.5.1(A));
**Group 2** welded, not in hollow sections (Table 11.5.1(B)); **Group 3**
bolts (Table 11.5.1(C)); **Group 4** welded, in hollow sections
(Table 11.5.1(D)). Shear-stress categories are a subset: descriptions 39,
40 (Table 11.5.1(B)) and 41 (Table 11.5.1(C)) (Cl 11.5.2).

`[code]` Each table row shows an isometric illustration with an arrow
indicating where, and on what plane, the stress range is calculated (normal
to the arrow, in the base material, excluding the detail's own geometric
stress concentration — Cl 11.3.1).

## Detail

### Group 1 — non-welded details (Table 11.5.1(A))

![[as4100-table-11.5.1A-detail-category-group1-nonwelded.png]]
*Table 11.5.1(A) — detail category classification, group 1 non-welded details (AS 4100:2020).*

`[code]` Own summary:

| Category | Detail |
|---|---|
| 160 | Rolled/extruded products — plates, flats, rolled sections, seamless tubes; sharp edges and rolling flaws ground out in the stress direction. |
| 140 | Bolted connections (stress on gross section for 8.8/TF, net section otherwise; avoid unsupported one-sided cover plates or account for eccentricity); material with gas-cut/sheared edges and **no draglines**, hardened material and edge discontinuities removed by machining/grinding. |
| 125 | Material with machine gas-cut edges **with draglines**, or manually gas-cut material; corners and discontinuities ground out in the stress direction. |

### Group 2 — welded details, not in hollow sections (Table 11.5.1(B))

![[as4100-table-11.5.1B-group2-welded-p151.png]]
![[as4100-table-11.5.1B-group2-welded-p152.png]]
![[as4100-table-11.5.1B-group2-welded-p153.png]]
![[as4100-table-11.5.1B-group2-welded-p154.png]]
![[as4100-table-11.5.1B-group2-welded-p155.png]]
![[as4100-table-11.5.1B-group2-welded-p156.png]]
![[as4100-table-11.5.1B-end.png]]
*Table 11.5.1(B) — detail category classification, group 2 welded details not in hollow sections, descriptions (1)–(40) (AS 4100:2020).*

`[code]` Own summary by category (governing description in brackets):

| Category | Detail |
|---|---|
| 125 | Welded plate I-section/box girder, continuous automatic longitudinal fillet or butt weld from both sides, no unrepaired stop-starts (8, 9). |
| 112 | Continuous automatic butt welds from one side with continuous backing bar, no unrepaired stop-starts (10, 11); continuous fillet/butt weld from both sides **with** stop-starts — use Cat 100 if manual (12); transverse complete-penetration butt welds with run-off tabs removed, ground flush, welded from two sides, in plates/flats/rolled sections/plate girders without cope hole, taper ≤ 1:4 (16, 17, 18). |
| 100 | Continuous manual longitudinal fillet/butt weld from both sides with stop-starts (per Note to (12)); bolts in shear, 8.8/TB category only, stress on minor-diameter area (41 — Table C). |
| 90 | Longitudinal welds from one side only, with/without stop-starts (13); transverse butt welds as above but Cat 90 variant, taper ≤1:4 (19, 20, 21); welded attachments non-load-carrying, `l ≤ 50 mm` fillet or `r/b` ratio criteria (32, 33); welds loaded in shear — fillet welds transmitting shear (throat-area stress), stud shear connectors failing in the weld (39, 40); transverse fillet welds `t ≤ 12 mm`, end ≥10 mm from plate edge (35). |
| 80 | Intermittent longitudinal welds (14); transverse butt welds with taper 1:4–1:2.5 (22); welded attachments `50 < l ≤ 100 mm` or intermediate r/b (33); shear connectors on base material, failure in base metal (34). |
| 71 | Zones with cope holes in longitudinally welded T-joints, cope hole not weld-filled (15); transverse butt welds on a backing bar, backing-strip fillet weld end > 10 mm from stressed-plate edges, with/without taper < 1:2.5 (23, 24); cruciform joints with load-carrying full-penetration welds, NDT-inspected, plate misalignment < 0.15× intermediate plate thickness (26); welded attachments `50 < l ≤ 100 mm` with `1/6 ≤ r/b < l/3` (33); vertical stiffeners welded to beam/plate-girder flange or web, `t > 12 mm` — combined bending+shear webs use principal-stress range (36); diaphragms of box girders welded to flange/web (37). |
| 63 | Overlapped welded joints — fillet-welded lap joint, welds + overlapping elements stronger than main plate, taper ≤ 1:2 (29). |
| 56 | Cruciform joints, partial penetration or fillet welds, stress on plate area (27); fillet-welded lap joint, `b < 8t`, welds + main plate stronger than overlapping elements (30). |
| 50 | Transverse butt welds as (23) but fillet weld ends **closer than 10 mm** to plate edge (25); cover plates in beams/plate girders, `t_f, t_p ≤ 25 mm`, end zones of single/multiple welded cover plates (38). |
| 45 | Fillet-welded lap joint, main plate + overlapping elements both stronger than the weld (31); welded attachments with `r/b < 1/6` (33). |
| 36 | Cruciform joints, partial penetration/fillet welds, stress on weld throat area (28); cover plates, `t_f, t_p > 25 mm` (38). |

`[derived]` The repeated pattern — the **same physical joint drops one or
two categories when the material is thicker** (e.g. cover plates 50→36 at
the 25 mm threshold; hollow-section joints below) — reflects the
well-established fatigue thickness effect (Cl 11.1.6, `β_tf`) baked
directly into some tables as a discrete step rather than the continuous
`β_tf` formula.

### Group 3 — bolts (Table 11.5.1(C))

![[as4100-table-11.5.1C-bolts.png]]
*Table 11.5.1(C) — detail category classification, group 3 bolts (AS 4100:2020).*

`[code]`

| Category | Detail |
|---|---|
| 100 | Bolts in shear, **8.8/TB bolting category only** — shear stress range on the minor diameter area `A_c` of the bolt (41). If the joint shear is insufficient to cause slip (Cl 9.2.3), bolt shear need not be considered in fatigue (Note 1). |
| 36 | Bolts and threaded rods in tension — tensile stress on the tensile stress area `A_s` (42); prying-action forces included; for tensioned bolts (8.8/TF, 8.8/TB) the stress range depends on connection geometry (Note 2: Standards Australia does not recommend a method for calculating the stress range in tensioned bolts — the applied-force change is often greater than the resulting bolt-force change, but this is connection-geometry-dependent). |

### Group 4 — welded details in hollow sections (Table 11.5.1(D))

![[as4100-table-11.5.1D-hollow-p1.png]]
![[as4100-table-11.5.1D-hollow-p2.png]]
*Table 11.5.1(D) — detail category classification, group 4 welded details in hollow sections, descriptions (43)–(50) (AS 4100:2020).*

`[code]`

| Category | Detail |
|---|---|
| 140 | Continuous automatic longitudinal welds, no stop-starts, or as manufactured (43). |
| 90 (t≥8) / 71 (t<8) | Transverse butt welds, circular hollow sections end-to-end (44). |
| 71 (t≥8) / 56 (t<8) | Transverse butt welds, rectangular hollow sections end-to-end (45); welded attachments (non-load-carrying) — CHS/RHS fillet-welded to another section, section width parallel to stress ≤ 100 mm — this row is a flat 71 regardless of `t` (48). |
| 56 (t≥8) / 50 (t<8) | Circular hollow sections, end-to-end **butt** welded with an intermediate plate (46). |
| 50 (t≥8) / 41 (t<8) | Rectangular hollow sections, end-to-end **butt** welded with an intermediate plate (47). |
| 45 (t≥8) / 40 (t<8) | Circular hollow sections, end-to-end **fillet** welded with an intermediate plate (49). |
| 40 (t≥8) / 36 (t<8) | Rectangular hollow sections, end-to-end **fillet** welded with an intermediate plate (50). |

`t` is the wall thickness of the hollow section. See Cl 11.3.1 for the
separate stress-range **multiplying factors** (Tables 11.3.1(A)/(B)) applied
to K/N-type gap/overlap truss connections in hollow sections, which are
independent of — and applied on top of — the detail category chosen here
(the connection itself is typically detail category 90 or similar under
Table 11.5.1(D) description (48), with the truss secondary-moment/
connection-stiffness effect captured by the multiplying factor instead of
a special detail category).

## Worked reference

`[derived]` A conveyor gantry chord splice made as a full-penetration
transverse butt weld between two equal rolled sections, weld cap ground
flush, welded from both sides, 100 % NDT, no cope hole → Table 11.5.1(B)
description (17)/(19) → **Category 112** (if taper ≤ 1:4 is not applicable,
plain splice) or per the applicable taper band. A field splice made instead
with a backing bar left in place → description (23)/(24) → **Category 71**
— a significant fatigue-life penalty purely from the fabrication detail,
independent of section size.

## Contradictions

None recorded.

## Related

- [[steel-fatigue-design]] — S-N formulae (`f_f`, `f_3`, `f_5`), exemption
  limits, constant/variable amplitude assessment, thickness correction
  `β_tf`, that consume the detail category assigned here.
- [[steel-weld-design]] — weld category (SP/GP) and geometry rules that
  some detail categories require (Cl 11.1.4).
- [[steel-bolt-design]] — 8.8/TB, 8.8/TF bolting categories referenced in
  Table 11.5.1(C).

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Cl 11.5 (pp. 149–158).
  Tables 11.5.1(A)–(D) reproduced in full as page images in
  `wiki/1-steelwork/assets/` (dense illustrated reference tables — the
  images are the primary source; the prose above is a navigational index,
  not a substitute).
