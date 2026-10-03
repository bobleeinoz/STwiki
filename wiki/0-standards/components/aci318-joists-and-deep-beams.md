---
title: ACI 318M-19 one-way joist systems and deep beams
category: 0-standards
tags: [aci, joists, deep-beams, strut-and-tie]
standards: [ACI 318M-19 Cl 9.8, ACI 318M-19 Cl 9.9]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 one-way joist systems and deep beams

> Scope: ACI 318M-19 Cl 9.8 (nonprestressed one-way joist systems, with
> structural and other fillers) and Cl 9.9 (deep beams — definition,
> dimensional limit, distributed reinforcement, detailing). This is an **ACI
> 318M-19 page, kept separate from the AS 3600:2018 concept pages** elsewhere
> in `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Both are special beam types carved out of Chapter 9: a joist is a
regularly spaced rib-and-slab system that earns relaxed shear/cover rules in
exchange for geometric limits (Cl 9.8); a deep beam is a member whose behaviour
is dominated by strut-like compression between load and support and so cannot
use plane-sections flexural theory (Cl 9.9). The two-way equivalent of the joist
rules is on [[aci318-two-way-slab-reinforcement-and-shear-detailing]] (Cl 8.8).

## Detail

### Nonprestressed one-way joist systems (Cl 9.8)

`[code]` A one-way joist system is a monolithic combination of regularly spaced
ribs and a top slab spanning in one direction (Cl 9.8.1.1). It must satisfy all
of: rib width ≥ **100 mm** at every depth (Cl 9.8.1.2); overall rib depth
≤ **3.5 ×** the minimum rib width (Cl 9.8.1.3); clear spacing between ribs
≤ **750 mm** (Cl 9.8.1.4). Joist construction not meeting these limits is
designed as separate slabs and beams (Cl 9.8.1.8).

`[code]` In exchange, `V_c` may be taken as **1.1 ×** the value from Cl 22.5
(Cl 9.8.1.5), and Table 9.6.3.1 exempts joists from `A_v,min` unless
`V_u > φV_c` (see [[aci318-beam-reinforcement-limits-and-detailing]]).
`[derived]` The 10% shear bonus rests on satisfactory past performance of joist
construction at comparably high calculated shear stresses and on the potential
for redistributing local overloads to adjacent joists; the 750 mm rib-spacing
cap exists because joists also get higher allowed shear and reduced cover
(Cl R9.8.1.4, R9.8.1.5).

`[code]` For structural integrity at least one bottom bar in every joist is
continuous and anchored to develop `f_y` at the support face (Cl 9.8.1.6).
Reinforcement perpendicular to the ribs is provided in the slab as needed for
flexure (allowing for load concentrations) and at least the shrinkage/
temperature steel of Cl 24.4 (Cl 9.8.1.7).

`[code]` **Structural fillers** (burned-clay or concrete tile of unit
compressive strength ≥ the joist `f'c`): slab thickness over the filler ≥ the
greater of one-twelfth the clear rib spacing and **40 mm**; the vertical shells
of fillers touching the ribs may be included in shear and negative-moment
strength, but no other part of the filler may (Cl 9.8.2.1). **Other fillers or
removable forms**: slab thickness ≥ the greater of one-twelfth the clear rib
spacing and **50 mm** (Cl 9.8.3.1).

### Deep beams (Cl 9.9)

`[code]` **Definition** (Cl 9.9.1.1): a deep beam is loaded on one face and
supported on the opposite face so that strut-like compression elements can form
between loads and supports, **and** meets either (a) clear span ≤ **4 ×**
overall depth `h`, or (b) concentrated loads within `2h` of the support face.
Design must account for the **nonlinear strain distribution** over the depth
(Cl 9.9.1.2); the strut-and-tie method of Chapter 23 is deemed to satisfy this
(Cl 9.9.1.3, see [[aci318-strut-and-tie-method]]). `[derived]` The definition
only applies if loads are applied on top and the support is at the bottom; loads
applied through the sides or bottom call for strut-and-tie design of the
internal reinforcement regardless (Cl R9.9.1.1), and the Code gives no
detailed deep-beam flexure procedure beyond requiring the nonlinear strain
distribution (Cl R9.9.1.2).

`[code]` **Dimensional limit**, except as permitted by Cl 23.4.4: `V_u ≤
0.83 φ √f'c b_w d` (Eq. 9.9.2.1) — `[derived]` to control service cracking and
guard against diagonal compression failure (Cl R9.9.2.1).

`[code]` **Distributed reinforcement on the side faces** (Cl 9.9.3.1), required
regardless of design method: perpendicular to the beam axis `A_v ≥ 0.0025 b_w s`
(`s` = spacing of this transverse steel); parallel to the axis
`A_vh ≥ 0.0025 b_w s_2` (`s_2` = spacing of this longitudinal steel). Minimum
flexural tension steel per Cl 9.6.1 (Cl 9.9.3.2). `[derived]` Vertical shear
steel is more effective than horizontal for deep-beam shear strength (Cl
R9.9.3.1).

`[code]` **Detailing** (Cl 9.9.4): cover per Cl 20.5.1; minimum bar spacing per
Cl 25.2; spacing of the Cl 9.9.3.1 distributed steel ≤ the lesser of `d/5` and
300 mm; development must account for bar stress that is **not proportional to
bending moment** (Cl 9.9.4.4); at simple supports, positive-moment tension steel
develops `f_y` at the support face (or per Cl 23.8.2/23.8.3 if designed by
Chapter 23); at interior supports, negative-moment steel is continuous with the
adjacent spans and positive-moment steel is continuous or spliced with it
(Cl 9.9.4.5–9.9.4.6). `[derived]` High bar stresses extend to the supports in a
deep beam, so ends may need hooks, headed bars or other mechanical anchorage,
and the strut-and-tie picture shows the bottom tie must be anchored at the
support face (Cl R9.9.4.4, R9.9.4.5).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-beam-design-basis-and-strength]] — Cl 9.1–9.5.
- [[aci318-beam-reinforcement-limits-and-detailing]] — Cl 9.6–9.7.
- [[aci318-strut-and-tie-method]] — Chapter 23, the deemed-to-satisfy method for
  deep beams (see also Cl 23.2.9).
- [[aci318-two-way-slab-reinforcement-and-shear-detailing]] — the Cl 8.8
  two-way joist counterpart.
- [[as3600-non-flexural-members-and-strut-tie-models]] — the AS 3600
  equivalent treatment of deep (non-flexural) members, for structural
  comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 9 Cl 9.8–9.9 (pp. 151–153).
