---
title: AS 4100:2020 — Steel Structures (standard register)
category: 0-standards
tags: [standard-register, clause-map, steel]
standards: [AS 4100:2020]
status: draft
reviewed: 2026-09-13
---

# AS 4100:2020 — Steel Structures

> Scope: standard register and section-level clause map for AS 4100:2020
> (incorporating Amendment No. 1, September 2021). Which clause governs what,
> edition and amendment status. No clause text reproduced — see
> `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf` for the source.

## Summary

`[code]` AS 4100:2020 is the third edition of the Australian Standard for the
limit-states design, fabrication, erection and modification of steelwork in
buildings, structures and cranes (Cl 1.1.1). It supersedes AS 4100—1998.
Prepared by Committee BD-001; approved 31 July 2020, published 21 August 2020.

`[code]` This reprint incorporates **Amendment No. 1 (September 2021)**.
Amended text is bracketed in the source by "A1" tags — check for the tag
before relying on a clause cited from this edition.

`[code]` **NCC compliance trap** — the reprint carries a normative
**"Appendix Former Wording"** stating that the *National Construction Code
2022 edition references AS 4100:2020 but only the unamended (pre-A1)
version*; for NCC compliance under either the 2022 or a later NCC edition
still pointing at the unamended text, the **former (pre-Amendment-1)
wording** applies, read without any of the A1-added or A1-amended text.
The affected clauses are: **Cl 5.6.1.1** (α_m formula, item (a)(iii)),
**Eq 5.6.1.1(2)** (α_s formula), **Table 6.3.3(C)** (the row beginning
"20"), **Cl 6.4.1** (the V* transverse-shear equation), **Cl 8.4.5.1** and
**8.4.5.2** (biaxial bending equations, which the A1 amendment *added* — the
former wording had no equation there, only the interaction concept in
prose), **Cl 8.4.6** (single-angle eccentric-connection equation and its
lead sentence), and **Cl H.4** (the reference elastic buckling moment's `J`
formula for a hollow section — the pre-amendment text erroneously repeated
the monosymmetry constant `β_x` integral formula in place of the correct
`J ≈ 4A_e²/Σ(b/t)`; this was a correction, not a technical change, so the
current A1 wording is safe to use even where NCC nominally cites the
unamended edition, since it fixes an evident drafting error rather than
changing the design method). **Practical guidance**: the wiki pages in this
vault cite the **current, A1-amended** wording throughout (the technically
current and generally safer basis). Where a project's regulatory pathway
requires strict NCC 2022 unamended-text compliance, cross-check the listed
clauses against the source PDF's "Appendix Former Wording" before final
sign-off, and flag the discrepancy to the human — do not silently switch
formulas.

`[code]` Exclusions (Cl 1.1.2): steel < 3 mm thick (other than AS/NZS 1163
hollow sections and packers); design yield stress > 690 MPa; cold-formed
members outside AS/NZS 1163 (→ AS/NZS 4600); composite steel-concrete
members (→ AS/NZS 2327); road, rail and pedestrian bridges (→ AS 5100.1,
5100.2, AS/NZS 5100.6). Box and longitudinally stiffened girders are
pointed to AS/NZS 5100.6 (Note to Cl 1.1.1).

`[derived]` For the mining / material-handling domain of this wiki, the
crane inclusion in Cl 1.1.1 and the AS 1418 load pointer in Cl 3.2.1(b)
are the hooks for crane runway and hoist-support design; AS 4100 supplies
the member and connection capacities while the crane standard supplies the
actions.

## Detail

### Major changes from the 1998 edition

`[code]` Per the Preface, principal differences from AS 4100—1998:

- "Construction specification" introduced as a named design deliverable
  (Cl 1.3.16, 1.6.2), consistent with AS/NZS 5131.
- "Construction category" CC1–CC4 defined (Cl 1.3.15, 1.7.2) with informative
  Appendix L on selection.
- Architecturally exposed structural steelwork (AESS) defined (Cl 1.3.3, 1.7.3).
- Lamellar tearing treated explicitly (Cl 1.3.40, 3.8, Appendix M),
  consistent with AS/NZS 1554.1.
- Alignment with AS/NZS 5100.6:2017 in various clauses.
- Fabrication and erection (Sections 14, 15) now largely reference
  AS/NZS 5131:2016.
- Alignment with AS/NZS 1252.1:2016 bolting (Cl 9.1.6, 9.3, 15.2); see ASI
  Technical Note TN-001 for background.
- New geometrical tolerances aligned to AS/NZS 5131 (Cl 14.4, 15.3).
- New Appendix K statistical data (aligned with AS/NZS 5100.6).
- Shear modulus at elevated temperature (Cl 12.4.2) and slenderness at
  elevated temperature (Cl 12.4.3) added.
- Table M.2 (criteria for target Z_Ed) adapted from EN 1993-1-10 Table 3.2.

Any wiki page citing an AS 4100 clause on the items above should state
whether it reflects the 1998 or 2020 provisions.

### Section-level clause map

`[code]` Own-words section scope, from the Contents. Page refs are to this
reprint (PDF page = printed page + 12) and will drift — cite clause numbers.

| Section       | Scope (own words)                                                                                                                                                                                                                                                                                             | Wiki pages                                                                                                                                                                 |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1             | Scope, exclusions, normative references, definitions, notation, alternative materials/methods, existing structures, design data and details on drawings, workmanship, construction category, AESS.                                                                                                            | [[steel-documentation-and-construction-category]]                                                                                                                          |
| 2             | Materials: design yield stress and tensile strength (Table 2.1), structural steel product standards, unidentified steel, elastic properties, through-thickness (Z) properties, fasteners, welds, studs, anchors, castings.                                                                                    | [[as4100-materials-and-design-strengths]]                                                                                                                                   |
| 3             | General design requirements: aims, loads and other actions, load combinations, notional horizontal forces, robustness, stability / strength / serviceability limit states, capacity factors (Table 3.4), load testing, brittle fracture, lamellar tearing, fatigue, fire, earthquake, reliability management. | [[as4100-limit-state-design-basis]]                                                                                                                                         |
| 4             | Methods of structural analysis: forms of construction (rigid, semi-rigid, simple), assumptions, first-order and second-order elastic analysis, moment amplification, plastic analysis, member and frame buckling analysis, effective length factors.                                                          | [[as4100-structural-analysis-methods]], [[as4100-member-effective-length-and-frame-buckling]]                                                                                |
| 5             | Members subject to bending: section moment capacity and slenderness, full lateral restraint, restraints and critical flange, member capacity without full lateral restraint (α_m, α_s, effective length), non-principal-plane bending, webs (shear, shear-bending interaction, bearing, stiffeners).          | [[as4100-beam-section-moment-capacity]], [[as4100-beam-lateral-restraint]], [[as4100-beam-member-moment-capacity]], [[as4100-web-shear-and-bearing]], [[as4100-web-stiffeners]] |
| 6             | Members subject to axial compression: form factor and effective width, member capacity α_c curves, varying sections, laced and battened members, back-to-back members, restraints.                                                                                                                            | [[as4100-compression-member-capacity]], [[as4100-built-up-compression-members]]                                                                                              |
| 7             | Members subject to axial tension: section capacity, force distribution / k_t, built-up tension members, pin-connected members.                                                                                                                                                                                | [[as4100-tension-member-capacity]]                                                                                                                                          |
| 8             | Combined actions: section capacity (uniaxial, biaxial), member in-plane capacity (elastic and plastic analysis), out-of-plane capacity, biaxial member capacity, eccentrically loaded single angles.                                                                                                          | [[as4100-combined-actions-section-capacity]], [[as4100-combined-actions-member-capacity]]                                                                                    |
| 9             | Connections: general requirements, minimum design actions, bolts (categories, shear, tension, combined, bearing, slip), bolt groups, pins, bolt detailing (pitch, edge distance, holes), welds (butt, fillet, plug/slot, compound), weld groups, packing.                                                     | [[as4100-connection-design-requirements]], [[as4100-bolt-design]], [[as4100-bolt-and-pin-detailing]], [[as4100-weld-design]]                                                   |
| 10            | Brittle fracture: notch-ductile range method, design service temperature, steel type selection (Tables 10.4.1, 10.4.4), fracture assessment.                                                                                                                                                                  | [[as4100-brittle-fracture-material-selection]]                                                                                                                              |
| 11            | Fatigue: loading, design spectrum, exemptions, detail categories (Tables 11.5.1, 11.5.2), S-N fatigue strength, constant and variable stress range assessment, punching limitation.                                                                                                                           | [[as4100-fatigue-design]]                                                                                                                                                   |
| 12            | Fire: period of structural adequacy, property variation with temperature, limiting steel temperature, time to limiting temperature for protected and unprotected members, three-sided exposure, connections and penetrations.                                                                                 | [[as4100-fire-design]]                                                                                                                                                      |
| 13            | Earthquake: design and detailing requirements by structural ductility category (μ = 2, 3, > 3), stiff and non-structural elements.                                                                                                                                                                            | [[as4100-earthquake-design-requirements]]                                                                                                                                   |
| 14            | Fabrication: material identification, procedures, hole sizes, bolting, geometrical tolerances (via AS/NZS 5131).                                                                                                                                                                                              | [[as4100-fabrication-and-erection-requirements]]                                                                                                                            |
| 15            | Erection: rejection, safety, bolt assembly and tensioning (Table 15.2.2.2 minimum bolt tension), tolerances.                                                                                                                                                                                                  | [[as4100-fabrication-and-erection-requirements]]                                                                                                                            |
| 16            | Modification of existing structures.                                                                                                                                                                                                                                                                          | [[as4100-fabrication-and-erection-requirements]]                                                                                                                            |
| 17            | Testing of structures or elements: proof testing and prototype testing, acceptance criteria, reports.                                                                                                                                                                                                         | [[as4100-load-testing]]                                                                                                                                                     |
| App A         | Not used.                                                                                                                                                                                                                                                                                                     | —                                                                                                                                                                          |
| App B (inf.)  | Suggested deflection limits.                                                                                                                                                                                                                                                                                  | [[as4100-deflection-limits]]                                                                                                                                                |
| App C (inf.)  | Selection of corrosion protection requirements.                                                                                                                                                                                                                                                               | [[as4100-corrosion-protection-selection]]                                                                                                                                   |
| App D (norm.) | Advanced structural analysis.                                                                                                                                                                                                                                                                                 | [[as4100-structural-analysis-methods]]                                                                                                                                      |
| App E (norm.) | Second-order elastic analysis.                                                                                                                                                                                                                                                                                | [[as4100-structural-analysis-methods]]                                                                                                                                      |
| App F (norm.) | Moment amplification for a sway member.                                                                                                                                                                                                                                                                       | [[as4100-structural-analysis-methods]]                                                                                                                                      |
| App G (norm.) | Braced member buckling in frames.                                                                                                                                                                                                                                                                             | [[as4100-member-effective-length-and-frame-buckling]]                                                                                                                       |
| App H (inf.)  | Elastic resistance to lateral buckling (M_o for general cases).                                                                                                                                                                                                                                               | [[as4100-beam-member-moment-capacity]]                                                                                                                                      |
| App I (inf.)  | Strength of stiffened web panels under combined actions.                                                                                                                                                                                                                                                      | [[as4100-web-stiffeners]]                                                                                                                                                   |
| App J (norm.) | Standard test for evaluation of slip factor.                                                                                                                                                                                                                                                                  | [[as4100-bolt-design]]                                                                                                                                                      |
| App K (norm.) | Statistical data (Charpy).                                                                                                                                                                                                                                                                                    | [[as4100-brittle-fracture-material-selection]]                                                                                                                              |
| App L (inf.)  | Guidance on determination of construction category.                                                                                                                                                                                                                                                           | [[steel-documentation-and-construction-category]]                                                                                                                          |
| App M (inf.)  | Selection of materials for avoidance of lamellar tearing.                                                                                                                                                                                                                                                     | [[as4100-materials-and-design-strengths]]                                                                                                                                   |

### Referenced standards that recur across categories

`[code]` Cross-references worth registering separately:

- AS/NZS 1170.0 / 1170.1 / 1170.2 / 1170.3, AS 1170.4 — actions and combinations (Cl 3.2).
- AS 1418 series — crane loads (Cl 3.2.1(b)). AS 1657 — platforms, walkways, stairways, ladders (Cl 3.2.1(c)).
- AS/NZS 1163, 1594, 3678, 3679.1, 3679.2, AS 3597 — steel products (Cl 2.2.1, Table 2.1).
- AS/NZS 1252.1 — high-strength structural bolting; AS 1110, 1111, 1112, 1237.1 — commercial bolts, nuts, washers (Cl 2.3.1).
- AS/NZS 5131 — fabrication and erection, welding, surface treatment, tolerances (Cl 2.3.3, 14, 15).
- AS/NZS 1554 series — welding (via AS/NZS 5131); AS/NZS 1554.2 — welded studs.
- AS 5216 — mechanical and chemical anchors (Cl 2.3.7). AS 2074 — steel castings (Cl 2.4).
- AS 2312.1 / AS/NZS 2312.2 / AS/NZS 4680 — corrosion protection and galvanizing (Cl 3.5.6 notes).
- AS 5104 (ISO 2394) — reliability / design by testing (Cl 1.5.2, 3.13).
- AS/NZS 5100.6 — box girders, weathering steel, bridge steelwork (pointers throughout).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

Concept pages compiled from this standard are listed in the clause map above
and in [[index]].

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf` — AS 4100:2020 incorporating
  Amendment No. 1 (September 2021). Text layer of this PDF is unreliable
  (clause numbers, formulae and many lines are vector outlines); all pages
  were read visually during ingest.
