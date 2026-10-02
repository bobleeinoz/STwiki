---
title: ACI 318M-19 foundation design — shallow foundations, deep foundations, pile caps, retaining walls
category: 2-concrete
tags: [aci, foundations, footings, piles, pile-caps, retaining-walls]
standards: [ACI 318M-19 Cl 13.1, ACI 318M-19 Cl 13.2, ACI 318M-19 Cl 13.3, ACI 318M-19 Cl 13.4]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 foundation design

> Scope: ACI 318M-19 Chapter 13 in full — foundation types covered, general
> design criteria and critical sections, shallow foundations (one-way,
> two-way isolated, combined/mat, grade-beam walls, retaining-wall stems) and
> deep foundations (allowable-strength and strength design of piles/piers/
> caissons, precast pile detailing, pile caps). Soil/rock capacity itself is
> **outside** this Code — it comes from the general building code and
> geotechnical principles. This is an **ACI 318M-19 page, kept separate from
> the AS 3600:2018 concept pages** elsewhere in `2-concrete` — see
> [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Chapter 13 applies to nonprestressed and prestressed shallow
foundations (strip, isolated, combined, mat, grade beams, pile caps), deep
foundations (piles, drilled piers, caissons) and retaining walls (cantilever,
counterfort/buttressed) (Cl 13.1.1; excluded foundations per Cl 1.4.7,
Cl 13.1.2):

![[aci318-fig-r13.1.1-types-of-foundations.png]]
*Fig. R13.1.1 — types of foundations covered: strip, isolated, stepped,
combined and mat footings; a pile cap on piles (deep foundation system); and
cantilever and counterfort/buttressed retaining walls (stem, toe, heel, optional
key) (ACI 318M-19).*

## Detail

### General requirements (Cl 13.2)

`[code]` Materials per Chapters 19–20 and Cl 20.6 (Cl 13.2.1); column, pedestal
and wall connections to foundations per Cl 16.3 (Cl 13.2.2.1). **Earthquake**:
members below the structure base that transmit earthquake forces to the
foundation follow Cl 18.2.2.3; for SDC C–F, foundations resisting or
transferring earthquake forces follow Cl 18.13 (Cl 13.2.3). Slabs-on-ground that
transmit vertical or lateral forces from other parts of the structure follow the
applicable Code provisions (Cl 13.2.4.1; seismic-system ones per Cl 18.13,
Cl 13.2.4.2). Plain concrete foundations: Chapter 14 (Cl 13.2.5.1).

`[code]` **Design criteria** (Cl 13.2.6): foundations are proportioned for
bearing, and for overturning and sliding stability at the soil–foundation
interface, per the general building code (Cl 13.2.6.1). For one-way shallow
foundations, two-way isolated footings, and two-way combined footings and mat
foundations, the **size-effect factor `λ_s`** of Cl 22.5 (one-way) and Cl 22.6
(two-way) may be **neglected** (Cl 13.2.6.2) — `[derived]` a footing-specific
relaxation of the shear size effect in
[[aci318-one-way-shear-strength]] / [[aci318-two-way-shear-strength]].
Foundation members are designed for factored loads and induced reactions except
as permitted for allowable-strength design of deep foundations (Cl 13.2.6.3);
any procedure satisfying equilibrium and geometric compatibility is permitted
(Cl 13.2.6.4), as is strut-and-tie (Cl 13.2.6.5 — see
[[aci318-strut-and-tie-method]]). External moment on any section of a strip
footing, isolated footing or pile cap is found by passing a vertical plane
through the member and taking the forces over the whole area on one side
(Cl 13.2.6.6). `[derived]` For a concentrically loaded spread footing, factored
soil pressure is simply factored load over base area; the base area itself is
sized with *unfactored* loads against permissible bearing (Cl R13.2.6.1,
R13.2.6.3).

`[code]` **Critical sections** (Cl 13.2.7): `M_u` at the supported member may be
taken at: face of column or pedestal; **halfway between column face and steel
base plate edge**; face of concrete wall; or **halfway between centre and face of
a masonry wall** (Table 13.2.7.1). The critical sections for one-way and two-way
shear are measured from those same `M_u` locations (Cl 13.2.7.2); circular or
regular-polygon columns/pedestals may be treated as square members of equivalent
area for moment, shear and development (Cl 13.2.7.3). **Development** follows
Chapter 25, with each section's bar force developed on both sides, critical
sections at the `M_u` locations and wherever section or reinforcement changes
occur, plus adequate anchorage where bar stress isn't proportional to moment
(sloped/stepped/tapered footings, or tension steel not parallel to the
compression face) (Cl 13.2.8).

### Shallow foundations (Cl 13.3)

`[code]` **General** (Cl 13.3.1): minimum base area is proportioned so permissible
bearing pressure (from soil/rock mechanics per the general building code) is not
exceeded under the applied forces and moments; overall depth is selected so the
effective depth of **bottom reinforcement is at least 150 mm**; in sloped,
stepped or tapered foundations depth, step locations or slope angle must satisfy
the design requirements at every section.

`[code]` **One-way** foundations (strip footings, combined footings, grade beams):
design per this section and Chapters 7 and 9, with reinforcement distributed
**uniformly across the full width** (Cl 13.3.2). **Two-way isolated footings**:
Chapters 7 and 8 apply; in square footings reinforcement is uniform across the
full width in both directions; in rectangular footings the long-direction steel
is uniform across the full width, and in the short direction a portion
`γ_s A_s` lies uniformly over a **central band** equal in width to the short side,
centred on the column, with the rest `(1 − γ_s)A_s` outside it, where
**γ_s = 2/(β + 1)**, `β` = long/short side ratio (Cl 13.3.3.3, Eq. 13.3.3.3).
`[derived]` A common construction simplification is to increase short-direction
steel by `2β/(β+1)` and space it uniformly along the long side (Cl R13.3.3.3).

`[code]` **Two-way combined footings and mat foundations**: Chapter 8 applies;
the **direct design method may not be used**; bearing pressure distribution must
be consistent with soil/rock properties and the structure; minimum reinforcement
in nonprestressed mats follows Cl 8.6.1.1 (Cl 13.3.4 — see
[[aci318-two-way-slab-reinforcement-and-shear-detailing]]). `[derived]`
Continuous steel near both faces in each direction is advisable for thermal
gradients and to intercept punching cracks (Cl R13.3.4.4).

`[code]` **Walls as grade beams**: Chapter 9 applies; a grade-beam wall that
counts as a deep beam per Cl 9.9.1.1 satisfies Cl 9.9; minimum wall
reinforcement of Cl 11.6 applies (Cl 13.3.5 — see
[[aci318-joists-and-deep-beams]], [[aci318-wall-design]]). **Retaining-wall
stems**: a cantilever retaining wall stem is designed as a **one-way slab**
(Chapter 7); a counterfort/buttressed stem as a **two-way slab** (Chapter 8)
(Cl 13.3.6.1–13.3.6.2). For uniform-thickness stems the critical section for
shear and flexure is at the **stem–footing interface**; tapered/varied stems are
checked throughout the height (Cl 13.3.6.3).

### Deep foundations (Cl 13.4)

`[code]` **General**: the number and arrangement of piles/piers/caissons is set so
forces and moments don't exceed permissible deep-foundation strength determined
per soil/rock mechanics and the general building code; members are designed by
the allowable-strength route (Cl 13.4.2) or strength design (Cl 13.4.3)
(Cl 13.4.1).

`[code]` **Allowable axial strength** (Cl 13.4.2): permitted using ASCE/SEI 7
Section 2.4 allowable-stress combinations and the maximum allowable compressive
strengths of Table 13.4.2.1, if the member is laterally supported for its full
height **and** applied forces cause bending less than that from an accidental
eccentricity of 5% of the diameter or width (Cl 13.4.2.1):

![[aci318-table-13.4.2.1-max-allowable-compressive-strength-deep-foundation.png]]
*Table 13.4.2.1 — maximum allowable compressive strength `P_a` by member type:
uncased drilled/augered cast-in-place `0.3f'cA_g + 0.4f_yA_s`; cast-in-place in
rock or in non-confining casing `0.33f'cA_g + 0.4f_yA_s`; confined metal-cased
`0.4f'cA_g`; precast nonprestressed `0.33f'cA_g + 0.4f_yA_s`; precast prestressed
`(0.33f'c − 0.27f_pc)A_g` (ACI 318M-19).* If either condition fails the member
is designed by strength design (Cl 13.4.2.2). A metal-cased cast-in-place member
counts as **confined** only if (Cl 13.4.2.3): the casing carries none of the
axial load; has a sealed tip and is mandrel-driven; is at least **1.7 mm**
thick; is seamless or has full-strength seams giving confinement; has casing
`f_y/f'c ≥ 6` and `f_y ≥ 210 MPa`; and nominal diameter ≤ **400 mm**. Higher
allowable strengths are permitted if the building official accepts them with
load-test justification (Cl 13.4.2.4).

`[code]` **Strength design** (Cl 13.4.3): permitted for all deep foundation
members, per Cl 10.5 with the compression φ of Table 13.4.3.2 for **axial load
without moment**, and Table 21.2.1 φ for tension, shear and combined axial force
and moment; Cl 22.4.2.4–22.4.2.5 tie/spiral provisions don't apply
(Cl 13.4.3.1–13.4.3.2):

![[aci318-table-13.4.3.2-phi-deep-foundation-members.png]]
*Table 13.4.3.2 — compressive strength reduction factors φ: uncased drilled/
augered 0.55; cast-in-place in rock or non-confining casing 0.60;
cast-in-place concrete-filled steel pipe 0.70; confined metal-cased 0.65;
precast nonprestressed and prestressed 0.65 (ACI 318M-19).* `[derived]` The
0.55 factor is an upper bound for well-understood soil conditions and quality
workmanship — a lower value may be appropriate for poorer soil knowledge or
quality control (Table 13.4.3.2 note 1).

`[code]` **Cast-in-place deep foundations** that are subject to uplift, or where
`M_u > 0.4M_cr`, must be reinforced unless enclosed by a structural steel pipe or
tube (Cl 13.4.4.1); portions in air, water or soil unable to restrain lateral
buckling are designed as columns per Chapter 10 (Cl 13.4.4.2 — see
[[aci318-column-design]]).

`[code]` **Precast piles supporting SDC A/B buildings** (Cl 13.4.5): symmetric
longitudinal steel; nonprestressed piles at least **4 bars** and `0.008A_g`;
prestressed piles with effective prestress giving minimum average compression of
**2.8 MPa** (length ≤ 10 m), **3.8 MPa** (10–15 m) or **4.8 MPa** (> 15 m),
computed with an assumed total loss of 210 MPa; transverse steel not smaller than
MW25/MD25 (`h ≤ 400 mm`), MW30/MD30 (`400 < h < 500`), MW35 (`h ≥ 500`) — or No. 10
bars throughout — at centre-to-centre spacing ≤ **25 mm** for the first five
ties/spirals at each end, **100 mm** within 600 mm of each end, **150 mm** over the
remainder (Tables 13.4.5.4, 13.4.5.6(a)/(b), Cl 13.4.5.1–13.4.5.6).

`[code]` **Pile caps** (Cl 13.4.6): overall depth such that the effective depth of
bottom steel is at least **300 mm**; factored moments and shears may take each pile
reaction concentrated at the pile centroid; unless strut-and-tie is used, the cap
satisfies `φV_n ≥ V_u` (one-way, Cl 22.5) and, for two-way foundations,
`φv_n ≥ v_u` (Cl 22.6). If designed by strut-and-tie, strut effective strength
uses `β_s = 0.60λ` (Cl 13.4.6.4) — `[derived]` because confining reinforcement
per Cl 23.5 is rarely practical in a pile cap, the lower of the available `β_s`
values is used (Cl R13.4.6.4). Shear on any section: a pile with centre `d_pile/2`
or more **outside** the section contributes its full reaction; `d_pile/2` or more
**inside** contributes none; intermediate positions interpolate linearly
(Cl 13.4.6.5).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-one-way-slab-design]], [[aci318-two-way-slab-design-basis]],
  [[aci318-two-way-slab-reinforcement-and-shear-detailing]] — Chapters 7–8,
  invoked for footings and mats.
- [[aci318-one-way-shear-strength]], [[aci318-two-way-shear-strength]] —
  Cl 22.5/22.6 shear strength used for footings and pile caps.
- [[aci318-strut-and-tie-method]] — permitted route for footings and pile caps.
- [[aci318-column-design]], [[aci318-wall-design]],
  [[aci318-joists-and-deep-beams]] — Chapters 10, 11, 9 invoked here.
- [[aci318-plain-concrete-design]] — plain concrete footings and pedestals.
- [[concrete-slab-on-ground-pavements-and-footings]] — the AS 3600 equivalent
  (footings/slabs-on-ground), for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 13 Cl 13.1–13.4 (pp. 191–202),
  incl. Tables 13.2.7.1, 13.4.2.1, 13.4.3.2, 13.4.5.4, 13.4.5.6 and
  Fig. R13.1.1.
