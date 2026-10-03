---
title: Strut-and-tie modelling (struts, ties, nodes)
category: 0-standards
tags: [strut-and-tie, non-flexural-members, d-regions]
standards: [AS 3600:2018 Cl 7.1-7.6]
status: draft
reviewed: 2026-09-12
---

# Strut-and-tie modelling

> Scope: how AS 3600 Section 7 defines a valid strut-and-tie model and sets
> the design strength of its struts, ties and nodes. Used to represent
> non-flexural members/regions at overload and failure, both for strength
> design and strength evaluation.

## Summary

`[code]` A strut-and-tie model is a load-resisting system of axially-loaded
compression elements (struts) and tension elements (ties) meeting at nodes.
Cl 7.1 sets seven modelling rules: loads apply only at nodes; struts/ties
carry axial force only; the model must provide a complete load path to
supports/adjacent regions; it must be in equilibrium with applied loads and
reactions; strut/tie/nodal-zone dimensions factor into the model geometry;
ties may cross struts but struts may only cross/intersect at nodes; and the
strut–tie angle at any node must be ≥30° for reinforced members or ≥20° for
prestressed members where a tendon acts as the tie reinforcement.

## Detail

### Concrete struts (Cl 7.2)

`[code]` Struts take one of three shapes — prismatic, fan, or bottle
(Fig 7.2.1) — chosen by the compression-field geometry; prismatic struts are
used only where the compressive stress field cannot diverge.

![[as3600-fig-7.2.1-strut-types.png]]
*Figure 7.2.1 — strut types: prismatic, fan and bottle-shaped compression
fields (AS 3600:2018).*

An **efficiency
factor** `βs` scales the effective strength: `βs = 1.0` for prismatic struts;
for unconfined fan/bottle-shaped fields, `βs` reduces as a function of the
strut–tie angle at the node (`βs = 1/(1.0 + 0.66·cot²θ)`, bounded
`0.3 ≤ βs ≤ 1.0`), using the smallest relevant angle where more than one tie
meets the node or angles differ at each end of the strut.

![[as3600-fig-7.2.2-strut-tie-angle.png]]
*Figure 7.2.2 — strut–tie angle `θ` at a node, used in the `βs` efficiency
factor (AS 3600:2018).*

`[code]` **Design strength**: `φst·βs·0.9·f'c·Ac`, where `Ac` is the strut's
smallest cross-sectional area normal to its axis, and `φst` comes from
Table 2.2.4 (see [[as3600-strength-check-procedures]]). Longitudinal
reinforcement used to boost a strut's strength must run parallel to and sit
within the strut, be enclosed in ties/spirals per Cl 10.7, and be properly
anchored — such a strut is then designed as a prismatic pin-ended short
column of equivalent geometry.

`[code]` **Bursting reinforcement in bottle-shaped struts** (7.2.4): the
design bursting force is found from an equilibrium model of the bottle
shape, using a minimum divergence angle (`tanθ = 1/2` for serviceability,
`1/5` for strength). Bursting force at cracking:
`Tb.cr = 0.7·b·lb·f'ct`. Where the calculated bursting force exceeds half of
`Tb.cr`, transverse reinforcement is required — either in two orthogonal
directions or one direction at ≥40° to the strut axis — sized so the
reinforcement's tensile capacity (at the appropriate serviceability stress
per Cl 12.7 — see [[as3600-d-region-crack-control]] — or at yield for
strength) meets or exceeds the governing
bursting force, distributed evenly through the bursting-zone length
`lb = √(z² + a²) − dc` (own-words: `a`, `b`, `z`, `dc` are shear span, member
width, and geometric projections of the idealized strut — see Fig 7.2.4(A)).

![[as3600-fig-7.2.4a-bottle-strut-bursting-model.png]]
*Figure 7.2.4(A) — idealized bottle-shaped strut, bursting-zone geometry
(`a`, `b`, `z`, `dc`, `lb`) (AS 3600:2018).*

![[as3600-fig-7.2.4b-bursting-reinforcement.png]]
*Figure 7.2.4(B) — bursting reinforcement layout in a bottle-shaped strut
(AS 3600:2018).*

### Ties (Cl 7.3)

`[code]` Ties consist of reinforcement and/or tendons, evenly distributed
across the nodal regions at each end so the resultant tensile force lines up
with the tie axis (7.3.1). **Design strength**:
`φst·[Ast·fsy + Ap·(σp.ef + Δσp)]`, capped by tendon yield `fpy`, with `φst`
from Table 2.2.4 (7.3.2). **Anchorage** (7.3.3): reinforcement/tendon must
extend beyond the node far enough to develop the tie's design strength at
the node, per Cl 13.1, with at least 50% of the development length beyond
the nodal zone — or, alternatively, a welded/mechanical anchorage located
entirely beyond the nodal zone.

### Nodes (Cl 7.4)

`[code]` Three node types by the struts/ties meeting there: **CCC** (struts
only), **CCT** (two-plus struts + one tension tie), **CTT** (two-plus
tension ties). Where the nodal region is **unconfined**, design strength is
capped by principal compressive stress on any nodal face:
`φst·βn·0.9·f'c`, where `βn = 1.0` (CCC), `0.8` (CCT) or `0.6` (CTT) — node
type alone sets the strength penalty, reflecting how much tension crosses
the compression field at that node. Where the nodal region **is** confined,
design strength may be assessed by test or calculation accounting for that
confinement, capped at `φst·1.8·f'c` principal compressive stress.

### Analysis and design basis (Cl 7.5–7.6)

`[code]` Model analysis must satisfy the general basis (Cl 6.1.1), results
interpretation (Cl 6.1.2) and the strut-and-tie-specific sensitivity check
(Cl 6.8.2 — see
[[as3600-plastic-and-strut-tie-analysis-methods]]). Strength design using
strut-and-tie modelling must satisfy the Cl 2.2.4 strength check procedure
(see [[as3600-strength-check-procedures]]); serviceability is **not**
covered by the strut-and-tie strength check and must be verified separately
(7.6.2).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-strength-check-procedures]] — Cl 2.2.4 strength check and
  `φst` (Table 2.2.4) this section's design strengths use.
- [[as3600-non-flexural-members-and-strut-tie-models]] — Section 12,
  which applies these Section 7 rules to deep beams and similar members.
- [[as3600-d-region-crack-control]] — Cl 12.7 serviceability stress used
  in bursting-reinforcement sizing (Cl 7.2.4).
- [[as3600-plastic-and-strut-tie-analysis-methods]] — Cl 6.8 analysis-menu
  entry pointing here.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clauses 7.1–7.6 (Figures 7.2.1,
  7.2.2, 7.2.4(A)/(B) reproduced as image assets above).
