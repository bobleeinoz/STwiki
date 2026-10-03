---
title: Concrete strength check procedures (Rd ≥ Ed by analysis method)
category: 0-standards
tags: [strength-design, capacity-factors, phi-factor, limit-states]
standards: [AS 3600:2018 Cl 2.2]
status: draft
reviewed: 2026-09-12
---

# Concrete strength check procedures

> Scope: the five strength check procedures AS 3600 Cl 2.2 defines, one per
> method of analysis used to get the design action effect.

## Summary

`[code]` The universal strength check is `Rd ≥ Ed`: design capacity not less
than design action effect (Cl 2.2.2, restated identically in Cl 2.2.5 and
Cl 2.2.6 for the non-linear cases). What changes between methods is how `Rd`
and `Ed` are each obtained. Cl 2.2.1 permits mixing procedures across
different members of the same structure, provided equilibrium and
compatibility are maintained for the structure as a whole.

`[practice]` Read this page together with
[[as3600-elastic-analysis-methods]], [[as3600-nonlinear-analysis-methods]]
and [[as3600-strut-and-tie-modelling]] — this page is the strength-check
layer that sits on top of whichever analysis method produced the action
effects.

## Detail

### (a) Linear elastic analysis / simplified analysis / statically determinate structures — Cl 2.2.2

`[code]` `Rd = Ru`, obtained from the ultimate strength `Ru` (calculated per
the relevant member-design section using characteristic material strengths)
times a capacity reduction factor `φ`. `Ed` comes from the critical factored
combination (AS/NZS 1170.0 + Cl 2.5) analysed by: linear elastic analysis
(Cl 6.2), linear elastic analysis with secondary bending moments (Cl 6.3), a
simplified method (Cl 6.9 or 6.10), or equilibrium analysis of a determinate
structure.

`[code]` `φ` varies by action type and reinforcement Ductility Class — axial
tension/compression, bending alone, bending with axial tension, bending with
axial compression, shear and torsion, bearing, plain concrete, fixings, and
singly-reinforced walls in a primary lateral system each have their own value
or formula in Table 2.2.2.

![[as3600-table-2.2.2-capacity-reduction-factors.png]]
*Table 2.2.2 — capacity reduction factors (φ) by action type and reinforcement
ductility class (AS 3600:2018).*

### (b) Linear elastic stress analysis — Cl 2.2.3

`[code]` Structure/member analysed uncracked under the critical factored
combination via linear stress analysis (Cl 6.4). Principal compressive
stresses are checked against a stress-reduction-factor–scaled effective
concrete strength; the effective-strength multiplier depends on whether
confining reinforcement is present and, if not, on whether the principal
tensile stress exceeds the concrete's tensile strength. Reinforcement and
tendons carry the tensile forces, checked against stress limits scaled by the
same stress reduction factor (Table 2.2.3). Steel areas
may be found by averaging peak stresses over an appropriate tributary area.
Development of reinforcement/tendons still follows Cl 13.1/13.3.

![[as3600-table-2.2.3-stress-reduction-factors.png]]
*Table 2.2.3 — stress reduction factor (φs) for concrete in compression, steel
in tension (Class N/L) and tendons, used with linear elastic stress analysis
(AS 3600:2018).*

### (c) Strut-and-tie analysis — Cl 2.2.4

`[code]` Forces in struts, ties and nodes come from an analysis of the
strut-and-tie model (Section 7) under the critical factored combination. Each
element's force is checked against its design strength from Section 7
(Cl 7.2.3 struts, Cl 7.3.2 ties, Cl 7.4.2 nodes), using a strength reduction
factor `φst` from Table 2.2.4. Tie reinforcement must
be Class N bar/mesh or tendons — Class L is excluded here. See
[[as3600-strut-and-tie-modelling]] for the model-building rules themselves.

![[as3600-table-2.2.4-strength-reduction-factors-strut-and-tie.png]]
*Table 2.2.4 — strength reduction factor (φst) for concrete struts, steel
ties and fibres in tension under strut-and-tie analysis (AS 3600:2018).*

### (d) Non-linear frame analysis at collapse — Cl 2.2.5

`[code]` `Rd = φsys·Ru.sys`: a **system** strength reduction factor applied to
the structure's mean capacity (not a per-member φ), where `Ru.sys` comes from
non-linear frame analysis (Cl 6.5) using mean material properties under the
same action combination used for `Ed`. `φsys` (Table 2.2.5) depends
qualitatively on failure ductility: systems that deflect
well beyond service levels and yield well before peak load get a higher
factor than systems without that warning — the note allows an even higher
factor if adequate warning of impending collapse can be demonstrated.

![[as3600-table-2.2.5-system-strength-reduction-factors.png]]
*Table 2.2.5 — system strength reduction factor (φsys) by failure ductility,
for non-linear frame/stress analysis at collapse (AS 3600:2018).*

### (e) Non-linear stress analysis at collapse — Cl 2.2.6

`[code]` Same system-factor logic as (d), but `Ru.sys` comes from non-linear
stress analysis (Cl 6.6) instead of frame analysis. Applies to a structure or
an individual component.

## Worked reference

None yet — add one once a specific member page (e.g. beam bending) exercises
a φ value with an actual number, at which point the human should supply the
Table 2.2.2 value being used.

## Contradictions

None recorded.

## Related

- [[as3600-limit-state-design-basis]] — where `Ed`'s load combinations come
  from.
- [[as3600-elastic-analysis-methods]], [[as3600-nonlinear-analysis-methods]],
  [[as3600-plastic-and-strut-tie-analysis-methods]] — the analysis methods
  feeding each procedure above.
- [[as3600-strut-and-tie-modelling]] — Section 7 detail for procedure (c).

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 2.2 (Tables 2.2.2–2.2.5
  reproduced as image assets above).
