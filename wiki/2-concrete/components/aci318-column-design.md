---
title: ACI 318M-19 column design — dimensional limits, strength, reinforcement limits, splices, ties and spirals
category: 2-concrete
tags: [aci, columns, reinforcement-detailing, splices, ties, spirals]
standards: [ACI 318M-19 Cl 10.1, ACI 318M-19 Cl 10.2, ACI 318M-19 Cl 10.3, ACI 318M-19 Cl 10.4, ACI 318M-19 Cl 10.5, ACI 318M-19 Cl 10.6, ACI 318M-19 Cl 10.7]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 column design

> Scope: ACI 318M-19 Chapter 10 in full — scope and general requirements,
> dimensional limits and the reduced effective area allowance, required and
> design strength, longitudinal/shear reinforcement limits, and detailing
> (bar count, offset bends, splices, ties, hoops, spirals). Slenderness is on
> [[aci318-column-slenderness-and-moment-magnification]]; the axial/flexural
> strength calculation itself is on [[aci318-sectional-strength-flexure-and-axial]].
> This is an **ACI 318M-19 page, kept separate from the AS 3600:2018 concept
> pages** elsewhere in `2-concrete` — see [[aci-318m-19-building-code-concrete]]
> for why.

## Summary

`[code]` Chapter 10 covers nonprestressed and prestressed columns, including
reinforced concrete pedestals; plain concrete pedestals go to Chapter 14
(Cl 10.1). Composite steel–concrete columns (encased sections or concrete-filled
tubes) are not covered — AISC 360 governs them (Cl R10.1.1). Like Chapter 9 it
is mostly a hub of limits and checklists that delegates calculations to
Chapter 22 and details to Chapter 25.

## Detail

### General and dimensional limits (Cl 10.2–10.3)

`[code]` Concrete per Chapter 19, reinforcement Chapter 20, embedments Cl 20.6;
cast-in-place joints satisfy Chapter 15, precast connections Cl 16.2, and
column-to-foundation connections Cl 16.3 (Cl 10.2).

`[code]` **Effective section** (Cl 10.3.1): for square, octagonal or other
shaped columns, gross area, required steel and design strength may be based on a
circular section of diameter equal to the **least lateral dimension**
(Cl 10.3.1.1). For a column larger than loading requires, these may be based on
a reduced effective area, **not less than one-half the total area** — *not*
allowed for special moment frame columns or columns outside the seismic system
that must meet Chapter 18 (Cl 10.3.1.2); the effective section of a column built
monolithically with a wall extends no more than **40 mm** outside the transverse
steel (Cl 10.3.1.3); for interlocking spirals it extends the minimum cover
outside the spirals (Cl 10.3.1.4). Analysis/design of other parts of the
structure interacting with the column uses the **actual** section
(Cl 10.3.1.5). `[derived]` With a reduced effective area the minimum steel is
computed from the *required* area but never below 0.5% of the actual section
(Cl R10.3.1.2).

### Required and design strength (Cl 10.4–10.5)

`[code]` Required strength follows Chapters 5 and 6 (Cl 10.4.1); every
applicable combination of `P_u` and `M_u` occurring **simultaneously** must be
checked (Cl 10.4.2.1):

![[aci318-fig-r10.4.2.1-critical-load-combinations-columns.png]]
*Fig. R10.4.2.1 — critical column load combinations: checking only the
maximum-axial-force combination (LC1) and the maximum-moment combination (LC2)
does not guarantee a compliant design for other combinations such as LC3 that
fall outside the `φM_n`–`φP_n` envelope (ACI 318M-19).*

`[code]` Design strength at all sections must satisfy `φP_n ≥ P_u`,
`φM_n ≥ M_u`, `φV_n ≥ V_u`, `φT_n ≥ T_u`, with interaction considered and φ per
Cl 21.2 (Cl 10.5.1). `P_n` and `M_n` come from Cl 22.4, `V_n` from Cl 22.5; if
`T_u ≥ φT_th` torsion is designed per Chapter 9 (Cl 10.5.2–10.5.4 — see
[[aci318-torsional-strength]]).

### Reinforcement limits (Cl 10.6)

`[code]` **Longitudinal steel** in nonprestressed columns (and prestressed
columns with average `f_pe < 1.6 MPa`): at least **0.01 A_g** and not more than
**0.08 A_g** (Cl 10.6.1.1). **Minimum shear reinforcement** `A_v,min` is needed
wherever `V_u > 0.5φV_c` (Cl 10.6.2.1), and where shear steel is required
`A_v,min/s` is the greater of `0.062√f'c b_w/f_yt` and `0.35 b_w/f_yt`
(Cl 10.6.2.2). `[derived]` Same rationale as for beams: restrain inclined
cracking and avoid sudden failure (Cl R10.6.2.1; see
[[aci318-beam-reinforcement-limits-and-detailing]]).

### Reinforcement detailing (Cl 10.7)

`[code]` Cover per Cl 20.5.1; development per Cl 25.4; minimum spacing per
Cl 25.2; bundled bars per Cl 25.6 (Cl 10.7.1–10.7.2). Along development and lap
lengths of longitudinal bars with `f_y ≥ 550 MPa`, transverse steel must give
`K_tr ≥ 0.5d_b` (Cl 10.7.1.3).

`[code]` **Minimum number of longitudinal bars** (nonprestressed, or prestressed
with `f_pe < 1.6 MPa`) (Cl 10.7.3.1): **three** within triangular ties, **four**
within rectangular or circular ties, **six** enclosed by spirals (or by circular
hoops for special moment frame columns). `[derived]` For other tie shapes,
provide a bar at each corner/apex with proper transverse steel (Cl R10.7.3.1).

`[code]` **Offset bent bars** (Cl 10.7.4): inclined portion slope relative to the
column axis ≤ **1 in 6**, with portions above and below parallel to the axis; if
the column face is offset **75 mm or more**, bars are not offset-bent and
separate lap-spliced dowels are provided instead. Horizontal support at offsets
(ties, hoops, spirals or floor construction) resists **1.5 ×** the horizontal
component of the force in the inclined bar portion, and any such transverse
steel lies within **150 mm** of the bend points (Cl 10.7.6.4).

`[code]` **Splices** (Cl 10.7.5): lap, mechanical, butt-welded and end-bearing
splices are permitted, must satisfy all factored load combinations, and splices
of deformed bars follow Cl 25.5 (Cl 10.7.5.1). `[derived]` The basic gravity
combination often governs the column, but a wind/earthquake combination may
impose greater bar tension, so each splice is designed for the maximum
calculated bar tension (Cl R10.7.5.1.2).

- **Compression lap splices** may be shortened — to not less than 300 mm — by
  ×0.83 for tied columns whose ties throughout the splice have effective area
  ≥ `0.0015 h s` in both directions (tie legs perpendicular to `h` counted), or by
  ×0.75 for spiral columns whose spirals satisfy Cl 25.7.3 (Cl 10.7.5.2.1).

![[aci318-fig-r10.7.5.2.1-effective-tie-legs-lap-splice.png]]
*Fig. R10.7.5.2.1 — example of the Cl 10.7.5.2.1(a) tie-area check: four effective
legs in direction 1 (`4A_b ≥ 0.0015h_1 s`) and two in direction 2
(`2A_b ≥ 0.0015h_2 s`), `A_b` = tie bar area (ACI 318M-19).*

- **Tension lap splices** (bar force tensile under factored loads) are Class A if
  ≤ 50% of bars are spliced at any section, adjacent-bar laps are staggered by at
  least `ℓ_d`, **and** tensile bar stress ≤ `0.5f_y`; otherwise Class B; always
  Class B if stress `> 0.5f_y` (Table 10.7.5.2.2, Cl 10.7.5.2.2).
- **End-bearing splices** (compressive bars only) require staggering or extra
  bars, with the continuing bars on each face having tensile strength ≥
  `0.25f_y ×` the vertical steel area on that face (Cl 10.7.5.3.1; details in
  Cl 25.5.6).

`[code]` **Transverse reinforcement** (Cl 10.7.6): satisfies the most
restrictive spacing rule and the details of Cl 25.7.2 (ties), 25.7.3 (spirals)
or 25.7.4 (hoops) (Cl 10.7.6.1.1–10.7.6.1.2); prestressed columns with average
`f_pe ≥ 1.6 MPa` need not meet the `16d_b` tie-spacing limit (Cl 10.7.6.1.3).
Longitudinal bars must be laterally supported by ties/hoops (Cl 10.7.6.2) or
spirals (Cl 10.7.6.3) unless tests and analyses show adequate strength and
constructability (Cl 10.7.6.1.4). Anchor bolts in the top of a column or pedestal
must be enclosed by transverse steel surrounding at least four longitudinal bars,
distributed within **125 mm** of the top, of at least two No. 13 or three No. 10
ties/hoops (Cl 10.7.6.1.5); the same applies to mechanical couplers or extended
bars for precast connections at column ends (Cl 10.7.6.1.6). `[derived]` The
confinement helps load transfer from bolts and couplers where concrete may crack
from unanticipated temperature, shrinkage or impact forces (Cl R10.7.6.1.5).

`[code]` **Ties/hoops, vertical placement** (Cl 10.7.6.2): the bottom tie is no
more than half a tie spacing above the footing/slab top; the top tie is no more
than half a tie spacing below the lowest horizontal steel in the slab, drop
panel or shear cap — or, if beams/brackets frame into all sides, no more than
75 mm below the lowest horizontal steel of the shallowest beam/bracket.
**Spirals** (Cl 10.7.6.3): bottom at the top of footing or slab; top per Table
10.7.6.3.2 — extend to the lowest horizontal steel of supported members if beams
or brackets frame into all sides; if not, extend likewise **and** add ties above
the spiral termination up to the bottom of the slab/drop panel/shear cap; for
columns with capitals, extend to the level where the capital diameter or width is
twice the column's.

`[code]` **Shear reinforcement** (Cl 10.7.6.5): ties, hoops or spirals;
maximum spacing per:

![[aci318-table-10.7.6.5.2-max-spacing-shear-reinforcement-columns.png]]
*Table 10.7.6.5.2 — maximum spacing of shear reinforcement: for
`V_s ≤ 0.33√f'c b_w d`, the lesser of `d/2` (nonprestressed) or `3h/4`
(prestressed) and 600 mm; for `V_s > 0.33√f'c b_w d`, the lesser of `d/4` or
`3h/8` and 300 mm (ACI 318M-19).*

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-column-slenderness-and-moment-magnification]] — Cl 6.2.5/6.6.4,
  slenderness effects.
- [[aci318-sectional-strength-flexure-and-axial]] — Cl 22.4, `P_n,max` and the
  axial/flexural strength assumptions.
- [[aci318-beam-reinforcement-limits-and-detailing]] — the Chapter 9
  counterpart whose shear-steel basis Cl 10.6.2 reuses.
- [[concrete-column-design-basis]], [[concrete-column-reinforcement-detailing]]
  — the AS 3600 equivalents, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 10 Cl 10.1–10.7 (pp. 155–163),
  incl. Tables 10.7.5.2.2, 10.7.6.3.2, 10.7.6.5.2 and Figs. R10.4.2.1,
  R10.7.5.2.1.
