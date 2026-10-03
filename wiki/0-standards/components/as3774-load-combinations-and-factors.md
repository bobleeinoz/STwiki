---
title: AS 3774 load groups, combinations and load factors
category: 0-standards
tags: [as3774, silo, bin, load-combinations, load-factors]
standards: [AS 3774:1996 Section 4, AS 3774:1996 Section 5, AS 3774:1996 App A]
status: draft
reviewed: 2026-10-02
---

# AS 3774 load groups, combinations and load factors

> Scope: AS 3774:1996 Sections 4-5 and Appendix A — load groups A-D, the three
> load combinations of Table 4.1, load factors of Table 4.2, fatigue,
> construction tolerances, wear allowance, permanent loads, and the data sheet.
> Register: [[as-3774-1996-loads-on-bulk-solids-containers]].

## Summary

`[code]` Loads are split into Group A permanent, B normal service, C
environmental and D accidental, subdivided into load types (Cl 4.1). Loads are
combined to give the most adverse effect on the member, considering
simultaneous action of several loads at upper characteristic values where
reasonably expected (Cl 4.2). Loads are determined at **characteristic**
values per Sections 5-6 and then factored for limit-state design (Cl 4.3).

## Detail

### Combinations (Cl 4.2, Table 4.1)

`[code]` Instantaneous *minimum* values of Group C and D loads are not assumed
to occur simultaneously; instantaneous *maximum* values of C and D are
combined individually with Groups A and B (Cl 4.2(a),(b)). Lower-bound values
must be checked where they are adverse, e.g. cylindrical walls in axial
buckling where the restraint of the stored solid is relied on.

![[as3774-table-4.1-load-classification-and-combination.png]]
*Table 4.1 — classification and combination of loads. A.1 and B.1, B.4-B.7 are in all combinations; B.2 initial loads in combination 1 only; B.3 flow loads in combination 2 only; combination 3 adds B.8, B.9 and one of the (X) Group C/D loads at a time (with the most adverse of them adopted).*

`[code]` Notes to Table 4.1 (deemed requirements): upper and lower estimates of
A.1 are both used with all combinations, plant on the roof or hung from the
hopper at upper bound for strength and lower bound for stability; conveyor/
feeder forces use the most adverse operating condition, including a zero value
where that is less favourable (Note 3); lateral restraint forces by rational
analysis (Note 4); loads from attached conveyor galleries are included
(Note 5); vehicle impact by rational dynamic analysis unless prevented by
positive measures (Note 6).

### Load factors (Cl 4.3, Table 4.2)

![[as3774-table-4.2-load-factors.png]]
*Table 4.2 — load factors, strength / serviceability: A 1.4 / 1.0; B.1 1.25 / 1.0; B.2 & B.3 on container walls 1.5 / 1.1; B.2 & B.3 on the support structure 1.5 / 1.0; B.4-B.9 1.8 / 1.1; C 1.5 / 0.9; D 1.25 / 0.8.*

`[derived]` The factors are tied to the load types, not to a code-wide set such
as AS/NZS 1170.0. They should not be mixed with AS/NZS 1170.0 factors on the
same member without an explicit decision (the Standard is a loading standard
that predates AS/NZS 1170 for this purpose).

### Other Section 4-5 requirements

`[code]` Containers subject to high-cycle filling/emptying shall be verified
for **fatigue** (Cl 4.4). Cylindrical (non-corrugated) walls: maximum
deviation 0.5 % grade (plumb of walls and centre-line). Corrugated walls:
straightness of trough/crest envelope d_c/100 over 1000 mm, abrupt joint
misalignment 3t, (d_c,max − d_c,min)/d_c ≤ 0.01, plumb 0.5 % (Cl 4.5.2).
Specified pressures assume these imperfection levels (Cl 4.5.1). An
appropriate allowance shall be made for **wear and corrosion** (Cl 4.6).
`[code]` Self-weight A.1 includes the structure, fixed plant and any permanent
infill over the container bottom or dead zone (Cl 5.1); dead and live loads and
wind on structures supported by the container are accurately assessed (Cl 5.2).

### Appendix A — data sheet (informative)

![[as3774-appendix-A-specification-data-sheet.png]]
*Appendix A — bulk solids container specification data sheet (bulk solid, properties min/avg/max, filling/discharge rates, capacity, geometry, discharge method, eccentricity, pressures, roof loads, wind, environment, earthquake zone, foundation).*

`[derived]` The data sheet is a useful project-intake checklist for any
silo/bin job; it could be adopted as a `[practice]` item by the human.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as-3774-1996-loads-on-bulk-solids-containers]]
- [[as3774-silo-wall-pressures-initial-and-flow]], [[as3774-hopper-pressures-and-feeder-loads]], [[as3774-eccentric-filling-and-discharge-loads]], [[as3774-special-service-loads]], [[as3774-environmental-and-accidental-loads]] — supply the load types combined here.
- [[as3774-container-classification-and-bulk-solid-properties]]

## Sources

- `raw/0-standards/AS 3774-reprint.pdf` — AS 3774—1996 incl. Amdt 1, 2 (1998), Sections 4-5, App A.
