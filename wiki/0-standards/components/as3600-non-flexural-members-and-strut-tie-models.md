---
title: Non-flexural members — scope, strength/serviceability basis, strut-and-tie model types
category: 0-standards
tags: [non-flexural-members, deep-beams, strut-and-tie, d-regions]
standards: [AS 3600:2018 Cl 12.1, AS 3600:2018 Cl 12.2]
status: draft
reviewed: 2026-09-12
---

# Non-flexural members — scope and strut-and-tie model types

> Scope: AS 3600 Cl 12.1 (which members/regions this section governs, and
> the three permitted strength-design routes) and Cl 12.2 (the three
> classes of strut-and-tie model for deep beams and similar non-flexural
> members).

## Summary

`[code]` Section 12 governs members that are geometrically too short/deep
for the plane-sections beam theory in Section 8 to hold, plus regions where
plane-sections theory breaks down locally regardless of the member's overall
proportions (Cl 12.1.1): **non-flexural members** — deep beams, footings,
pile caps — identified by a clear-span(or projection)-to-depth ratio below a
threshold that varies by end condition (1.5 for cantilevers, 3 for simply
supported, 4 for continuous members); and **non-flexural regions** —
corbels, continuous nibs, prestressed end zones, and surfaces where
concentrated forces act, regardless of the overall member's slenderness.

## Detail

### Design for strength and serviceability (Cl 12.1.2–12.1.3)

`[code]` Strength design uses one of three routes, each paired with its
matching Cl 2.2 strength-check procedure (see
[[as3600-strength-check-procedures]]): linear elastic stress analysis
(Cl 2.2.3), strut-and-tie analysis (Cl 2.2.4), or non-linear stress analysis
(Cl 2.2.6) — `φ` comes from Table 2.2.2 for whichever route is used.
Serviceability design follows Cl 2.3 generally (see
[[as3600-serviceability-design]]) plus this section's own crack-control
clause, Cl 12.7 — see [[as3600-d-region-crack-control]].

### Strut-and-tie model types for deep beams (Cl 12.2.1)

`[code]` Three model types, distinguished by how load reaches the supports
(Fig 12.2.1, reproduced below and also described in words):

![[as3600-fig-12.2.1-strut-tie-model-types.png]]
*Figure 12.2.1 — strut-and-tie model types for deep beams: Type I (major
struts only), Type II (major + minor struts, hanger reinforcement) and
Type III (minor struts only, hanger reinforcement) (AS 3600:2018).*

- **Type I** — load carried directly to supports by major (primary) struts
  only. The simplest, most direct load path.
- **Type II** — load reaches supports via a mix of primary and secondary
  (minor) struts. Because the secondary struts develop vertical force
  components that need to be carried back up to the top of the member,
  **adequately anchored hanger reinforcement** is required for that purpose.
- **Type III** — load reaches supports entirely via a series of minor struts,
  again requiring hanger reinforcement to return the struts' vertical force
  components to the top of the member.

`[code]` Hanger reinforcement (fitments) is anchored per Cl 8.3.2.4 (see
[[as3600-beam-detailing]]). For Type II models specifically, the force
carried by the secondary struts (`Tw`) is bounded: `0 ≤ Tw ≤ F`, where `F` is
the total vertical component of the external load carried through the shear
span — i.e. the secondary-strut/hanger system can carry anywhere from none
to all of the shear-span load, but not more than the load itself. Strut
bursting reinforcement (where struts are bottle-shaped) follows Cl 7.2.4 —
see [[as3600-strut-and-tie-modelling]].

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-strut-and-tie-modelling]] — Section 7's general strut/tie/node
  design-strength rules, which every model type here must still satisfy.
- [[as3600-beam-shear-and-torsion-design]] — Cl 8.2.3.2 routes
  near-support/deep-shear-span members into this section instead of ordinary
  sectional shear design.
- [[as3600-corbels-nibs-and-stepped-joints]] — Cl 12.3/12.4, additional
  requirements for two specific non-flexural details.
- [[as3600-wall-design-basis-and-classification]] — routes low-aspect-ratio
  walls in net tension (`H/L ≤ 2`) to this section's strut-and-tie method.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clauses 12.1, 12.2 (Figure
  12.2.1 reproduced as an image asset above).
