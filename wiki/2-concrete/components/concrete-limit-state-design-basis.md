---
title: Concrete design basis — limit states, actions and combinations
category: 2-concrete
tags: [design-basis, limit-states, actions, loads, prestress]
standards: [AS 3600:2018 Cl 2.1, AS 3600:2018 Cl 2.5]
status: draft
reviewed: 2026-09-12
---

# Concrete design basis — limit states, actions and combinations

> Scope: the overall procedural basis AS 3600 requires for designing a
> concrete structure — which limit states must be checked, how actions and
> combinations feed the checks, and the cross-references to durability, fire,
> earthquake, robustness and fatigue.

## Summary

`[code]` AS 3600 Cl 2.1.1 requires concrete structures to be designed for
ultimate strength and serviceability limit states following the general
procedures of AS/NZS 1170.0, supplemented by AS 3600's own strength (Cl 2.2)
and serviceability (Cl 2.3) requirements. Strength/serviceability may
alternatively be demonstrated by testing a structure or component to
Appendix B.

`[code]` Where AS 1170.4 requires earthquake design, the structure must
conform with AS 1170.4, AS 3600 generally, and specifically Section 14;
reinforcement must be detailed to deliver the ductility assumed in design.

`[code]` Robustness and structural integrity are designed to AS/NZS 1170.0
Section 6 or BCA Cl BV2 (whichever applies). Detailing must effectively tie
members together — cast-in-place requirements sit in Sections 8, 9, 10, 11;
prefabricated concrete requirements sit in Section 17.

`[code]` Durability (Section 4) and fire resistance (Section 5) are mandatory
companion checks alongside strength/serviceability, not optional add-ons.

`[code]` Fatigue (Cl 2.1.5) need not be considered where the foreseen number
of stress cycles is less than 10 000. Where it must be considered, design
actions follow Cl 6.1.3's analysis methods, but moment redistribution (elastic
per Cl 6.2.7, plastic per Cl 6.7) is **not permitted** for fatigue load cases.
Non-linear analysis is allowed provided sections don't undergo large plastic
deformation under fatigue combinations. Note (own-words): the standard's
guidance is to model in cracked linear-elastic terms with a modular ratio
Es/Ec = 10 in the absence of better data.

`[code]` All material properties used in design trace to Section 3, and must
account for age, rate of loading and expected variability — see
[[concrete-properties-of-concrete]], [[concrete-properties-of-reinforcement]],
[[concrete-properties-of-tendons-and-prestress-losses]].

## Detail

### Actions and combinations (Cl 2.5)

`[code]` The base actions/loads and their load-factor combinations come from
AS/NZS 1170.0 — that standard is not yet in `raw/`, so its specific
combinations are not restated here. Ingest AS/NZS 1170.0 to give
`4-loads-mechanics-maths` its own combinations page; this page only covers
what AS 3600 adds on top.

`[code]` **Prestressed members at transfer** (Cl 2.5.2.2): stress resultants
from prestress carry a load factor of unity in both ULS and SLS combinations
unless stated otherwise. For the specific case of permanent action plus
prestress force at transfer, the more severe of two combinations governs:
one that increases the permanent-action factor above unity, and one that
reduces it below unity — bounding the case from both sides rather than
assuming dead load and prestress always act favourably together. See
Cl 2.5.2.2 for the exact factors; also cross-check against Cl 6.2.6 and
Cl 8.2.1.3.

`[code]` **Fatigue combinations** (Cl 2.5.2.3): pair a permanent-action +
prestress + short-term-service-action combination with the fatigue action
`Qfat`. The load factor applied to this combination is generally taken as a
fixed value, reducible if the stress analysis is shown to be accurate or
conservative and verified by in-situ observation.

![[as3600-table-2.5.2.3a-fatigue-load-combinations.png]]
*Table 2.5.2.3(A) — fatigue load combinations for maximum steel stress range
and maximum/minimum concrete compressive/tensile stress (AS 3600:2018).*

`[code]` A separate
representative-value factor applies to prestress specifically for fatigue
combinations, and varies by tendon type (pre-tensioned/unbonded vs.
post-tensioned bonded, with or without direct force measurement) — see
Table 2.5.2.3(B).

![[as3600-table-2.5.2.3b-prestress-representative-value-factor.png]]
*Table 2.5.2.3(B) — representative value factor for prestress (φp) in fatigue
load combinations, by tendon type (AS 3600:2018).*

`[code]` **Construction effects** (Cl 2.5.3): the critical design condition
for strength and serviceability must account for construction sequence, the
formwork-stripping schedule, and the back-propping method and its effect on
loads applied during construction.

`[code]` **Pattern loading** (Cl 2.5.4): for continuous beams, 2D and 3D
framed structures and floor systems, alternative arrangements of vertical
imposed action must be checked to find the critical combination — at minimum:
factored dead load with no pattern variation, factored imposed action on
alternate spans, on any two adjacent spans, and on all spans; 3D systems add
chequerboard arrangements. **Exception:** for beams/slabs at ULS where imposed
action Q is less than three-quarters of dead load G, the factored imposed
action on all spans governs and separate pattern checks are not required.
`[practice]` Deflection- or vibration-sensitive structures and slender floor
systems may need load arrangements beyond this minimum — the clause flags this
as a note, not a rule, so treat any extra patterns as engineering judgement.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[wiki/0-standards/as-3600-2018-concrete-structures]]
- [[concrete-strength-check-procedures]] — Cl 2.2, the strength-side check
  this design basis feeds into.
- [[concrete-serviceability-design]] — Cl 2.3.
- [[concrete-fatigue-design-overview]] — Cl 2.4, and the Section 18 detail
  still to be ingested.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clauses 2.1, 2.5.
