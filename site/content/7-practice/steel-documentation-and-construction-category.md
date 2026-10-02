---
title: Steel drawings, construction specification and construction category
category: 7-practice
tags: [documentation, drawings, construction-specification, construction-category, AESS, checklist]
standards: [AS 4100:2020 Cl 1.5, AS 4100:2020 Cl 1.6, AS 4100:2020 Cl 1.7, AS 4100:2020 App L, AS/NZS 5131]
status: draft
reviewed: 2026-09-13
---

# Steel drawings, construction specification and construction category

> Scope: AS 4100:2020 Cl 1.5 (alternative materials, existing structures),
> Cl 1.6 (design data and design details to show on drawings / in the
> construction specification), Cl 1.7 (workmanship, construction category
> CC1–CC4, AESS categories). Use as a deliverable checklist.

## Summary

`[code]` AS 4100:2020 names the **construction specification** as a design
deliverable alongside the drawings (Cl 1.6.2) and requires a **construction
category** (CC1–CC4) to be nominated in it; if none is nominated, CC2
applies (Cl 1.7.2). Fabrication and erection requirements for each category
are in AS/NZS 5131.

## Detail

### Design data on drawings (Cl 1.6.1) — checklist

`[code]` The drawings shall show:

- [ ] Reference number and date of issue of the design Standards used.
- [ ] Nominal loads.
- [ ] Corrosion protection, if applicable.
- [ ] Fire-resistance level, if applicable.
- [ ] Steel grades used.

### Design details on drawings and/or construction specification (Cl 1.6.2) — checklist

`[code]` As appropriate:

- [ ] Size and designation of each member.
- [ ] Number, sizes and categories of bolts in connections.
- [ ] Sizes, types, strength and categories of welds, with the level of
      visual and other NDE required.
- [ ] Sizes of connection components.
- [ ] Locations and details of planned joints, connections and splices.
- [ ] Any construction constraint assumed in design.
- [ ] Camber of any members.
- [ ] Construction category or categories required (Cl 1.7.2).
- [ ] Corrosion protection required (Cl 3.5.6).
- [ ] Any AESS requirement (Cl 1.7.3).
- [ ] Any tolerances different from AS/NZS 5131 (Cl 14.4, 15.3), including
      functional tolerance class if not Class 1.
- [ ] Any material selection requirement to avoid lamellar tearing
      (Cl 2.2.5).
- [ ] Any other fabrication, erection and operation requirements.

### Construction category (Cl 1.7.2, App L)

`[code]` Four categories CC1–CC4, strictness increasing from CC1 to CC4.
CC4 is CC3 plus project- or organisation-specific requirements for unusual
or special structures. A category applies to the whole structure, parts, or
specific details; a structure may carry several categories provided every
part is categorised, and a detail or detail group carries exactly one.
Default is CC2 if not specified. Selection depends on importance factor,
service category and fabrication category (App L).

`[code]` Appendix L (informative) determination process (Cl L.4): (a)
select the building/structure **importance level** (1–4) from the National
Construction Code (Australia) or AS/NZS 1170.0:2002 Section 3; (b) select
the **service category** (Table L.1); (c) select the **fabrication
category** (Table L.2); (d) read the construction category off the Table
L.3 risk matrix. The three inputs formalise the AS 5104 (ISO 2394)
reliability-differentiation philosophy that AS/NZS 1170.0 is built on:
importance factor (risk to life / consequence of failure), service
category (exposure to actions that reveal flaws), and fabrication category
(fabrication complexity) (Cl L.2–L.3.1).

`[code]` Table L.1 — suggested criteria for service categories:

| Category | Criteria |
|---|---|
| SC1 | (a) Predominantly quasi-static actions only — e.g. typical multi-level buildings, warehouses, storage facilities; **or** (b) low seismic demand (AS 1170.4 Earthquake Design Category I or II); **or** (c) low-level fatigue actions where assessment is not required (satisfies Cl 11.4, or cranes classified S1–S3 to AS 1418.1—2002). |
| SC2 | (d) Members/connections subject to fatigue assessment per this Standard or AS/NZS 5100.6 — e.g. road/rail bridges, cranes and their immediate supporting structure, structures susceptible to wind/crowd/machinery-induced vibration; **or** (e) medium-to-high seismic demand (Earthquake Design Category III). |

`[code]` Table L.2 — suggested criteria for fabrication categories:

| Category | Criteria |
|---|---|
| FC1 | (a) Non-welded components, any steel grade; (b) welded components from steel grade ≤ 450. |
| FC2 | (c) Welded components from steel grade above 450; (e) site-welded components essential for structural integrity; (f) components receiving thermic treatment during manufacture; (g) CHS truss components requiring end profile cuts. |

A structure or part of a structure may contain components under different
service categories and/or fabrication categories.

![[as4100-table-L.3-risk-matrix.png]]
*Table L.3 — risk matrix for determination of the construction category (AS 4100:2020).*

`[code]` Table L.3 (transcribed):

| Importance level | 1 | | 2 | | 3 | | 4 | |
|---|---|---|---|---|---|---|---|---|
| Service category | SC1 | SC2 | SC1 | SC2 | SC1 | SC2 | SC1 | SC2 |
| FC1 | CC1 | CC3 | CC2 | CC3 | CC2/CC3ᵃ | CC3 | CC3 | CC3 |
| FC2 | CC2 | CC3 | CC2 | CC3 | CC3 | CC3 | CC3 | CC4 |

ᵃ The CC2-vs-CC3 assessment for that cell is by engineering judgement,
based on the relative simplicity of fabrication and erection.

Determining the construction category is the **designer's** responsibility,
considering national provisions, industry-association guidance and the
applicable WHS regulations/codes of practice (Note 1). CC4 requirements are
additional to CC3 and **not fully defined** in AS 4100 — for unusual/
special structures, expect project-specific or organisation-specific CC4
requirements (Note 2).

`[derived]` Mining and material-handling structures with dynamic machinery
(crushers, screens, stacker/reclaimer booms, crane runways) typically sit
in **SC2** (fatigue assessment applies) — pushing even Importance Level 1–2
structures to at least CC2/CC3, and FC2 fabrication (thick or high-grade
welded members, site-critical welds) at IL3+ reaches CC3 outright, CC4 at
IL4. Confirm the actual importance level from the NCC/AS 1170.0 before
reading the matrix — do not assume IL2 by default for an industrial
structure with a process-safety or life-safety consequence of failure.

### Architecturally exposed structural steelwork (Cl 1.7.3)

`[code]` Any AESS requirement must be designated in the construction
specification. AS/NZS 5131 defines five categories:

| Category | Own-words description |
|---|---|
| AESS 1 | Basic elements requiring enhanced workmanship. |
| AESS 2 | Feature elements viewed from > 6 m: good fabrication practice, enhanced weld, connection, detail and gap/cope tolerance treatment. |
| AESS 3 | Feature elements viewed from < 6 m: welds generally smooth but visible, some grind marks acceptable, tighter tolerances. |
| AESS 4 | Showcase elements: ground/filled weld edges smooth and true, all surfaces sanded and filled smooth, most stringent tolerances. |
| AESS C | Custom elements. |

### Alternative materials and existing structures (Cl 1.5)

`[code]` Materials or methods not covered are permitted provided Section 3
is satisfied (Cl 1.5.1). For existing structures the Standard's general
principles may be applied using the **actual** material properties
(Cl 1.5.2); AS 5104 (ISO 2394) covers design by testing and AS 5100.7/5100.8
cover assessment and rehabilitation.

### Workmanship (Cl 1.7.1, 1.7.4)

`[code]` All structures designed to AS 4100 must be constructed so that all
requirements in the drawings and construction specification are met;
fabrication and erection requirements are a function of the nominated
construction category.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as-4100-2020-steel-structures]] — standard register.
- [[steel-limit-state-design-basis]] — Cl 3.13 reliability management.
- [[steel-fabrication-and-erection-requirements]] — Sections 14–16.
- [[steel-materials-and-design-strengths]] — Z-quality / lamellar tearing.
- [[concrete-documentation-requirements]] — AS 3600 counterpart checklist.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Cl 1.5–1.7 (pp. 24–26),
  Appendix L (pp. 209–211). Table L.3 reproduced in
  `wiki/1-steelwork/assets/`.
