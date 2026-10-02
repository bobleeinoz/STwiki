---
title: Concrete serviceability design — deflection, cracking, vibration
category: 2-concrete
tags: [serviceability, deflection, cracking, vibration]
standards: [AS 3600:2018 Cl 2.3]
status: draft
reviewed: 2026-09-12
---

# Concrete serviceability design — deflection, cracking, vibration

> Scope: AS 3600's serviceability limit-state philosophy for deflection,
> cracking and vibration (Cl 2.3), ahead of the member-specific detail in
> Sections 8–11.

## Summary

`[code]` Cl 2.3.1 requires design checks for all relevant service conditions
so the structure performs its intended function. The note points out that the
limits in Cl 2.3.2/2.3.3 come from prior design experience for normal
structures — special situations may need other limits, with further guidance
in AS/NZS 1170.0 Appendix C.

## Detail

### Deflection (Cl 2.3.2)

`[code]` The designer chooses a deflection limit appropriate to the structure
and its use; the limit must not exceed the deflection-to-span ratio given in
Table 2.3.2 for the applicable category — the table
covers total deflection for all members, incremental deflection after
attachment of masonry partitions or other brittle finishes, deflection under
vehicular/pedestrian traffic, and deflection of transfer members, each with
tighter limits than a bare total-deflection check. Calculated or span-to-depth-controlled
deflections (per Cl 8.5 for beams, Cl 9.3 for slabs — pages not yet written)
must not exceed the chosen limit.

![[as3600-table-2.3.2-deflection-limits.png]]
*Table 2.3.2 — limits for calculated vertical deflections of beams and slabs,
by deflection type and member category (AS 3600:2018).*

`[code]` For unbraced frames and multistorey buildings under lateral load, the
inter-storey drift limit is explicitly stated in the clause text itself (not a
table): **1/500 of storey height**, checked under the design lateral
serviceability load.

### Cracking (Cl 2.3.3)

`[code]` General requirement: cracking must not compromise structural
performance, durability or appearance (Cl 2.3.3.1). Deemed-to-satisfy routes
(Cl 2.3.3.2), each delegated to member-specific clauses not yet ingested as
pages:

- Flexural cracking in beams/slabs under service conditions → Cl 8.6.1–8.6.5
  (see [[concrete-beam-crack-control]]), 9.5.1, 9.5.2, 9.5.4, 9.5.5 (see
  [[concrete-slab-crack-control]]) or 16.4.7.4 (SFRC, not yet ingested) as
  applicable.
- Shrinkage/temperature cracking in slabs → Cl 9.5.3, see
  [[concrete-slab-crack-control]].
- Cracking in D-regions under service conditions → Cl 12.7, see
  [[concrete-d-region-crack-control]].
- Cracking at openings, discontinuities and near restraints → Cl 8.6.1, 9.5.4
  or 9.5.5 — same beam/slab crack-control pages as above.
- Pre-hardening cracking → controlled by specification and construction
  measures, not a calculation clause.

`[derived]` This page is a routing map rather than a design method in itself
— the actual crack-control calculations now live in the linked beam/slab/
D-region pages (Sections 8, 9, 12 ingested); column crack control (Cl 10.9,
see [[concrete-column-floor-joint-transmission]]) simply points back to the
beam clause rather than having its own method.

### Vibration (Cl 2.3.4)

`[code]` Vibration must be controlled so serviceability and structural
performance are not adversely affected. No calculation method is given in
this clause — see Cl 8.7 (beams) and Cl 9.6 (slabs), not yet ingested.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-limit-state-design-basis]] — parent design-basis page.
- [[concrete-fatigue-design-overview]] — the fourth design check alongside
  strength/serviceability/durability/fire.
- [[concrete-beam-crack-control]], [[concrete-slab-crack-control]],
  [[concrete-d-region-crack-control]] — the pages this routing map now
  points to (Sections 8, 9, 12 ingested).

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 2.3 (Table 2.3.2
  reproduced as an image asset above).
