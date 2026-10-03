---
title: ACI 318M-19 two-way (punching) shear strength — critical sections, vc, vs
category: 0-standards
tags: [aci, shear, punching-shear, two-way-shear, sectional-strength]
standards: [ACI 318M-19 Cl 22.6]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 two-way (punching) shear strength

> Scope: ACI 318M-19 Cl 22.6 — two-way shear strength expressed as stress
> (`v_n = v_c + v_s`), critical section geometry (incl. openings), the
> concrete contribution `v_c` with and without shear reinforcement (both
> using the Cl 22.5.5.1.3 size-effect factor `λ_s`), and shear reinforcement
> (`v_s`) via stirrups or headed shear studs. This is an **ACI 318M-19 page,
> kept separate from the AS 3600:2018 concept pages** elsewhere in
> `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Unlike one-way shear (Cl 22.5, expressed as a force `V`), two-way
shear is expressed throughout Chapter 22.6 as a **stress** `v` — this
permits superposition of direct shear and unbalanced-moment shear transfer
(Cl R22.6). Without shear reinforcement: `v_n = v_c` (Eq. 22.6.1.2). With
shear reinforcement: `v_n = v_c + v_s` (Eq. 22.6.1.3). Shear is checked
against an assumed critical section of depth `d` and perimeter `b_o`
(Cl 22.6.1.4). `[derived]` This is ACI's punching-shear provision — the
direct counterpart to AS 3600's local (punching) shear strength of flat
slabs (see [[as3600-slab-punching-shear]]); the two codes' coefficients
and critical-perimeter conventions are not interchangeable.

## Detail

### Effective depth and material limits (Cl 22.6.2–22.6.3)

`[code]` `d` is the **average of the effective depths in the two orthogonal
directions** (Cl 22.6.2.1); for prestressed two-way members, `d` need not be
taken less than `0.8h` (Cl 22.6.2.2). `√f'c` for `v_c` is capped as if
`f'c ≤ 8.3 MPa` — there's limited test data for two-way shear in
higher-strength concrete (Cl 22.6.3.1, Cl R22.6.3.1). `f_yt` for `v_s` is
capped per Cl 20.2.2.4 (420 MPa) to control cracking (Cl 22.6.3.2).

### Critical sections (Cl 22.6.4)

`[code]` The critical section perimeter `b_o` is placed to be a **minimum**,
but never closer than `d/2` to: (a) edges/corners of columns, concentrated
loads or reaction areas, or (b) thickness changes such as drop panel/shear
cap edges (Cl 22.6.4.1). Square/rectangular columns may use straight-sided
critical sections (Cl 22.6.4.1.1); circular or regular-polygon columns may
be idealised as an equivalent-area square column (Cl 22.6.4.1.2).

`[code]` Where shear reinforcement (stirrups or headed studs) is present, a
**second, outer critical section** at `d/2` beyond the outermost peripheral
line of shear reinforcement must also be checked — shaped as the
minimum-perimeter polygon (Cl 22.6.4.2):

![[aci318-fig-r22.6.4.2a-two-way-shear-critical-section-interior-column.png]]
*Fig. R22.6.4.2a — critical sections for two-way shear in a slab with shear
reinforcement at an interior column: the inner section runs through the
first line of stirrup legs, the outer section at `d/2` beyond the last line
(ACI 318M-19).* `[derived]` The source gives matching figures for edge
(R22.6.4.2b) and corner (R22.6.4.2c) columns, not reproduced here — both
show the same two-critical-section logic with the polygon truncated at the
free edge(s).

`[code]` **Openings** within `4h` of a column/load/reaction area periphery:
the portion of `b_o` enclosed between lines from the load centroid tangent to
the opening boundary is treated as ineffective (Cl 22.6.4.3) — conservative
per Committee 326 (1962) testing, and not required at all once an opening is
more than `4d` from the column periphery (Cl R22.6.4.3).

### Vc without shear reinforcement (Cl 22.6.5)

`[code]` For nonprestressed two-way members (and prestressed members not
using the Cl 22.6.5.4 exception), `v_c` is the **least of three expressions**:

![[aci318-table-22.6.5.2-vc-two-way-no-shear-reinforcement.png]]
*Table 22.6.5.2 — `v_c` for two-way members without shear reinforcement:
expression (a) is the base punching stress, (b) penalises non-square
loaded areas (`β` = long/short side ratio), (c) penalises a large critical
perimeter relative to depth (`α_s` = 40/30/20 for interior/edge/corner
columns, Cl 22.6.5.3) (ACI 318M-19).*

`[code]` `λ_s` here is the **same** Cl 22.5.5.1.3 size-effect factor used for
one-way shear (see [[aci318-one-way-shear-strength]]) — `[derived]` its
presence in every two-way `v_c` term, with no `A_v,min` exemption, means
(unlike one-way shear) two-way `v_c` is always size-effect-reduced for
`d > 250 mm`, not just for lightly-reinforced members — Cl 22.6.6.2 below is
the only way to recover `λ_s = 1.0`.

`[derived]` Expression (a)'s `0.33λ_s√f'c` cap is unconservative for
elongated (high-`β`) loaded areas — test punching stress runs from
≈`0.33λ_s√f'c` at a rectangular column's corners down to `0.17λ_s√f'c` or
less along its long sides (Cl R22.6.5.2), which is why expressions (b) and
(c) exist and the least of the three governs. For a non-rectangular loaded
area, `β` is the ratio of the longest to the largest-perpendicular overall
dimension of the *effective* loaded area (the minimum-perimeter shape fully
enclosing the actual loaded area) — illustrated for an L-shaped reaction in
Fig. R22.6.5.2.

`[code]` **Prestressed exception** (Cl 22.6.5.4–22.6.5.5): if bonded
reinforcement per Cl 8.6.2.3/8.7.5.3 is provided, no column face is within
`4h` of a discontinuous edge, and effective prestress `f_pc ≥ 0.9 MPa` in
each direction, `v_c` may instead be the lesser of two prestress-specific
expressions (Eq. 22.6.5.5a/b, each including a `V_p` term for the vertical
component of effective prestress crossing the critical section) —
`[derived]` a different failure mode (diagonal tension at the Cl 22.6.4.1
critical section) from the nonprestressed punching-shear mechanism, so the
expressions are not simply a prestressed version of Table 22.6.5.2
(Cl R22.6.5.4). `f_pc` is capped at 3.5 MPa average of the two directions and
`√f'c` at √5.8 MPa for this method.

### Vc with shear reinforcement (Cl 22.6.6)

`[code]` At the **inner** critical section (Cl 22.6.4.1), `v_c` depends on
reinforcement type:

![[aci318-table-22.6.6.1-vc-two-way-with-shear-reinforcement.png]]
*Table 22.6.6.1 — `v_c` for two-way members with shear reinforcement: a flat
`0.17λ_sλ√f'c` for stirrups at every critical section; a higher,
3-expression-least value for headed shear studs at the inner (22.6.4.1)
section only, dropping to the same `0.17λ_sλ√f'c` at the outer (22.6.4.2)
section (ACI 318M-19).*

`[code]` `0.17λ_sλ√f'c` (stirrups) is exactly **half** the no-reinforcement
cap `0.33λ_sλ√f'c`, because stirrups are assumed to take all shear beyond the
inclined-cracking load, which occurs at roughly half the bare-concrete
capacity (Cl R22.6.6.1). Headed studs get a higher allowance because tests
(Elgabry and Ghali 1987) show they anchor and engage the compression zone
more effectively than stirrup legs.

`[code]` **λ_s = 1.0 override** (Cl 22.6.6.2): permitted — recovering full
two-way shear strength from the size-effect reduction — if either (a)
stirrups per Cl 8.7.6 with `A_v/s ≥ 0.17√f'c b_o/f_yt`, or (b) smooth headed
studs with shaft length ≤ 250 mm per Cl 8.7.7 with the same `A_v/s` minimum,
are provided. `[derived]` This cap on stud shaft length exists because
longer smooth studs may not fully mitigate the size effect per available
test evidence (Cl R22.6.6.2) — stacking ("piggybacking") shorter studs with
an intermediate head is the Commentary's suggested workaround for thick
slabs (Fig. R22.6.6.2).

`[code]` **Maximum v_u** (Cl 22.6.6.3) at the critical sections of Cl 22.6.4:

![[aci318-table-22.6.6.3-max-vu-two-way-with-shear-reinforcement.png]]
*Table 22.6.6.3 — maximum `v_u`: `0.5φ√f'c` for stirrups, `0.66φ√f'c` for
headed shear studs (ACI 318M-19).* This upper bound on required strength
governs the minimum effective depth, independent of how much shear
reinforcement is provided.

### Vs — stirrups and headed shear studs (Cl 22.6.7–22.6.8)

`[code]` Single-/multi-leg stirrups as two-way shear reinforcement require
`d ≥ 150 mm` **and** `d ≥ 16d_b` (stirrup bar diameter) (Cl 22.6.7.1). Both
stirrups and headed studs use the same form:

**v_s = A_v f_yt / (b_o s)**  (Eq. 22.6.7.2, Eq. 22.6.8.2)

where `A_v` is the total area of all legs/studs on one peripheral line
geometrically similar to the column perimeter, and `s` is the spacing
between peripheral lines, perpendicular to the column face. `[code]` Headed
stud reinforcement additionally requires `A_v/s ≥ 0.17√f'c b_o/f_yt`
(Cl 22.6.8.3) as its own minimum-reinforcement check, independent of the
`v_u > φv_c` trigger for one-way shear reinforcement.

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-one-way-shear-strength]] — Cl 22.5, including the `λ_s` size-effect
  factor this page's `v_c` provisions share.
- [[aci318-two-way-slab-design-basis]], [[aci318-two-way-slab-reinforcement-and-shear-detailing]]
  — Chapter 8, which invokes this page's critical sections and `v_c`/`v_s`
  throughout (factored shear stress, stirrup/headed-stud reinforcement).
- [[as3600-slab-punching-shear]] — the AS 3600 equivalent, for structural
  comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 22 Cl 22.6 (pp. 411–420), incl.
  Tables 22.6.5.2, 22.6.6.1, 22.6.6.3 and Fig. R22.6.4.2a.
