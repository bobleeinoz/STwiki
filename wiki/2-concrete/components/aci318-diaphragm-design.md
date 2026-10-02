---
title: ACI 318M-19 diaphragm design — in-plane forces, analysis models, moment, shear, collectors
category: 2-concrete
tags: [aci, diaphragms, collectors, in-plane-shear, lateral-load-path]
standards: [ACI 318M-19 Cl 12.1, ACI 318M-19 Cl 12.2, ACI 318M-19 Cl 12.3, ACI 318M-19 Cl 12.4, ACI 318M-19 Cl 12.5, ACI 318M-19 Cl 12.6, ACI 318M-19 Cl 12.7]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 diaphragm design

> Scope: ACI 318M-19 Chapter 12 in full — which diaphragm types it covers,
> the actions to design for, analysis/modelling options, design strength for
> moment, axial force, shear and collectors, and reinforcement limits and
> detailing. Seismic (SDC D–F) diaphragm requirements are in Cl 18.12 and are
> not covered here. This is an **ACI 318M-19 page, kept separate from the
> AS 3600:2018 concept pages** elsewhere in `2-concrete` — see
> [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Chapter 12 covers nonprestressed and prestressed diaphragms of four
kinds: (a) cast-in-place slabs; (b) cast-in-place topping on precast elements;
(c) precast elements with end strips formed by a cast-in-place topping or edge
beams; (d) interconnected precast elements without a cast-in-place topping
(Cl 12.1.1). Diaphragms in SDC D, E or F also satisfy Cl 18.12 (Cl 12.1.2). A
diaphragm acts as a horizontal (or nearly horizontal) planar element that
transfers lateral forces to the vertical lateral-force-resisting elements, ties
the building into a 3-D system and gives lateral support to its elements
(Cl R12.1.1):

![[aci318-fig-r12.1.1-typical-diaphragm-actions.png]]
*Fig. R12.1.1 — typical diaphragm actions: in-plane inertial loads, collectors
delivering force to structural walls, transfer slab/diaphragm shear transfer
(distributors), thrust from inclined columns, gravity loads and soil pressure
below grade (ACI 318M-19).* See also [[aci318-structural-system-requirements]]
(Cl 4.4.7) for the system-level diaphragm requirements.

## Detail

### General and design limits (Cl 12.2–12.3)

`[code]` Design must consider: (a) diaphragm in-plane forces from lateral load;
(b) diaphragm transfer forces; (c) connection forces between the diaphragm and
vertical framing or nonstructural elements; (d) forces from bracing of vertical
or sloped elements; (e) out-of-plane forces from gravity and other surface
loads (Cl 12.2.1). Slab openings and voids must be considered (Cl 12.2.2).
Thickness must be adequate for stability, strength and stiffness under factored
load combinations, and not less than that required for floor/roof elements
elsewhere in the Code (Cl 12.3.1).

### Required strength and analysis (Cl 12.4)

`[code]` Required strength of diaphragms, collectors and connections comes from
the Chapter 5 combinations (Cl 12.4.1.1), and for floor/roof diaphragms includes
simultaneous out-of-plane loads (Cl 12.4.1.2). The general building code's
diaphragm modelling requirements govern where applicable; otherwise modelling
satisfies Chapter 6 with **any reasonable and consistent set of stiffness
assumptions** (Cl 12.4.2.1–12.4.2.3). In-plane design moments, shears and axial
forces must be consistent with equilibrium and the boundary conditions, and may
come from (Cl 12.4.2.4): (a) a rigid diaphragm model; (b) a flexible diaphragm
model; (c) a **bounding analysis** — the envelope of two or more analyses at
upper- and lower-bound diaphragm in-plane stiffness; (d) a finite element model
including diaphragm flexibility; or (e) a strut-and-tie model per Cl 23.2 (see
[[aci318-strut-and-tie-method]]). `[derived]` The rigid model is widely used for
cast-in-place diaphragms and topped precast, unless a long span, large aspect
ratio or irregularity creates flexible behaviour (Cl R12.4.2.4).

### Design strength (Cl 12.5)

`[code]` `φS_n ≥ U` with interaction considered, φ per Cl 21.2 (Cl 12.5.1.1–
12.5.1.2). Design strengths follow whichever idealisation was used (Cl 12.5.1.3):
(a) a **deep beam** of full diaphragm depth with moment resisted by boundary
reinforcement concentrated at the edges — Cl 12.5.2–12.5.4; (b) strut-and-tie —
Cl 23.3; (c) finite element — Chapter 22, with nonuniform shear distributions
considered and collectors provided; (d) alternative methods satisfying
equilibrium with design strength ≥ required strength for every load-path
element. Precompression from prestressing may be used to resist diaphragm forces
(Cl 12.5.1.4); where bonded nonprestressed prestressing steel resists collector
force, diaphragm shear or in-plane-moment tension, steel stress is capped at the
lesser of specified yield and **420 MPa** (Cl 12.5.1.5) to control crack width
and joint opening (Cl R12.5.1.5).

`[code]` **Moment and axial force** (Cl 12.5.2): design per Cl 22.3 and 22.4
(Cl 12.5.2.1). Tension due to moment may be resisted by deformed bars, strands or
bars (prestressed or not), mechanical connectors across precast joints, or
precompression, alone or combined (Cl 12.5.2.2). Nonprestressed reinforcement and
mechanical connectors resisting that tension must lie **within h/4 of the tension
edge** (`h` = diaphragm depth in plane at that location), though reinforcement may
be developed into adjacent segments outside the `h/4` limit where depth changes
(Cl 12.5.2.3); connectors across precast joints must resist the required tension
under the anticipated joint opening (Cl 12.5.2.4):

![[aci318-fig-r12.5.2.3-diaphragm-tension-reinforcement-locations.png]]
*Fig. R12.5.2.3 — locations of nonprestressed reinforcement resisting tension
due to moment and axial force: within `h/4` of each tension edge (shaded zones),
with reinforcement for each span placed within the depth of that span's
diaphragm segment (ACI 318M-19).* `[derived]` Joint opening in an untopped
precast diaphragm responding elastically is typically on the order of 2.5 mm or
less, and may exceed that under earthquake motions beyond design level
(Cl R12.5.2.4).

`[code]` **Shear** (Cl 12.5.3): φ = **0.75** unless Cl 21.2.4 requires less
(Cl 12.5.3.2). For an entirely cast-in-place diaphragm,
`V_n = A_cv(0.17λ√f'c + ρ_t f_y)` (Eq. 12.5.3.3), where `A_cv` is the gross
concrete area bounded by diaphragm web thickness and depth (less voids),
`√f'c` ≤ √8.3 MPa and `ρ_t` is distributed steel parallel to the in-plane shear;
cross-section is limited by `V_u ≤ φ0.66√f'c A_cv` (Eq. 12.5.3.4, same `f'c`
cap) (Cl 12.5.3.3–12.5.3.4). **Cast-in-place topping on precast**: both
equations apply with `A_cv` from the topping thickness (noncomposite) or combined
thickness (composite — `f'c` then the lesser of precast and topping), and `V_n`
must not exceed the shear-friction value of Cl 22.9 using topping thickness
above the joints and the steel crossing them (Cl 12.5.3.5 — see
[[aci318-bearing-and-shear-friction]]). **Untopped precast** (and precast with
end strips): shear may be designed via (a) grouted joints with nominal strength
≤ **0.55 MPa** plus shear-friction reinforcement *in addition to* tension
reinforcement, and/or (b) mechanical connectors resisting required shear under
anticipated joint opening (Cl 12.5.3.6). `[derived]` The Code gives no untopped
diaphragm provisions for SDC D–F (Cl R12.5.3.6). Wherever shear transfers from
the diaphragm to a collector, or from diaphragm/collector to a vertical element,
either shear-friction (Cl 22.9) applies or, for mechanical connectors/dowels,
uplift and rotation of the vertical element are considered (Cl 12.5.3.7).

`[code]` **Collectors** (Cl 12.5.4): extend from the vertical elements across all
or part of the diaphragm depth as needed to transfer shear, and may stop along
lengths of vertical element where collector force transfer isn't required
(Cl 12.5.4.1). They are designed as tension and/or compression members per
Cl 22.4 (Cl 12.5.4.2):

![[aci318-fig-r12.5.4.1-collectors.png]]
*Fig. R12.5.4.1 — full-depth collector and shear-friction reinforcement
required to transfer collector force into a wall: (a) arrangement, (b) collector
tension and compression force diagram along the wall (ACI 318M-19).*
Collector steel extends along the vertical element by at least the greater of
(a) the tension development length and (b) the length needed to transmit design
force by shear-friction, mechanical connectors or other mechanism (Cl 12.5.4.3).

### Reinforcement limits and detailing (Cl 12.6–12.7)

`[code]` Shrinkage and temperature steel per Cl 24.4 (Cl 12.6.1); floor/roof
diaphragms (other than slabs-on-ground) meet the one-way (Cl 7.6) or two-way
(Cl 8.6) slab reinforcement limits (Cl 12.6.2). Steel for diaphragm **in-plane**
forces is *in addition to* steel for other load effects, except that
shrinkage/temperature steel may also resist in-plane forces (Cl 12.6.3). Cover per
Cl 20.5.1 (Chapter 18 may govern in SDC D–F, Cl 18.12.7.7); development per
Cl 25.4 unless Chapter 18 requires more; splices Cl 25.5; bundled bars Cl 25.6;
minimum spacing Cl 25.2 (Cl 12.7.1–12.7.2.1). Maximum spacing of deformed steel
is the lesser of **5×** diaphragm thickness and 450 mm (Cl 12.7.2.2). Floor/roof
diaphragms follow one-way (Cl 7.7) or two-way (Cl 8.7) detailing (Cl 12.7.3.1);
bar force at each section is developed each side (Cl 12.7.3.2); tension steel
extends at least `ℓ_d` past where no longer required, except at diaphragm edges
and expansion joints (Cl 12.7.3.3).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-structural-system-requirements]] — Cl 4.4.7, system-level diaphragm
  and collector requirements.
- [[aci318-strut-and-tie-method]], [[aci318-bearing-and-shear-friction]] —
  Chapter 23 and Cl 22.9, used for strut-and-tie modelling and shear transfer.
- [[aci318-wall-design]] — the vertical elements collectors deliver force into.
- [[concrete-diaphragm-design]] — the AS 3600 equivalent, for structural
  comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 12 Cl 12.1–12.7 (pp. 175–189),
  incl. Figs. R12.1.1, R12.5.2.3, R12.5.4.1.
