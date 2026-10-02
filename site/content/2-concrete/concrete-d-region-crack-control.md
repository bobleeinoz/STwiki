---
title: Crack control in D-regions and non-flexural members
category: 2-concrete
tags: [crack-control, d-regions, non-flexural-members]
standards: [AS 3600:2018 Cl 12.7]
status: draft
reviewed: 2026-09-12
---

# Crack control in D-regions and non-flexural members

> Scope: AS 3600 Cl 12.7 — the crack-control clause for non-flexural
> members/regions, referenced from [[concrete-serviceability-design]]
> Cl 2.3.3.2(d) as the home clause for D-region cracking.

## Summary

`[code]` Unlike the beam/slab crack-control clauses (Cl 8.6/9.5, see
[[concrete-beam-crack-control]] / [[concrete-slab-crack-control]]), which
offer a steel-stress-vs-bar-diameter/spacing table plus a full crack-width
calculation, this clause gives its limits **directly in the clause text** as
three named tiers — no separate data table to omit.

## Detail

### Deemed-to-satisfy stress and spacing limits (Cl 12.7)

`[code]` Requirements are deemed satisfied if the reinforcement stress under
short-term service loads (`σst`) and the maximum centre-to-centre spacing of
bonded reinforcement crossing the crack (`s`) both stay within the limits
for the chosen degree of crack control:

- **Minor degree of control**: `σst ≤ 350 MPa`, `s ≤ 350 mm`.
- **Moderate degree of control** (cracks inconsequential or hidden from
  view): `σst ≤ 250 MPa`, `s ≤ 300 mm`.
- **Strong degree of control** (appearance-critical, or cracks may reflect
  through finishes): `σst ≤ 200 MPa`, `s ≤ 200 mm`.

`[practice]` This three-tier minor/moderate/strong structure is the same
pattern used for slab and wall shrinkage/temperature reinforcement (Cl 9.5.3,
Cl 11.7.2 — see [[concrete-slab-crack-control]] and
[[concrete-wall-reinforcement-requirements]]) — worth recognising as a
recurring design-intent classification across the standard rather than a
one-off scheme.

`[code]` For prestressed concrete, the same three tiers apply to the
*change* in tendon stress after the point of decompression, rather than to
the absolute reinforcement stress used for ordinary reinforced members.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-serviceability-design]] — Cl 2.3.3.2(d), which routes D-region
  cracking to this clause.
- [[concrete-non-flexural-members-and-strut-tie-models]] — Cl 12.1.3, which
  names this clause as the serviceability companion to Section 12's strength
  design.
- [[concrete-beam-crack-control]], [[concrete-slab-crack-control]] — the
  member-specific crack-control clauses this one parallels for non-flexural
  regions.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clause 12.7.
