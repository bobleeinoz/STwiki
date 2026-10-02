---
title: ACI 318M-19 — Building Code Requirements for Structural Concrete (standard register)
category: 0-standards
tags: [standard-register, clause-map, concrete, aci, us-code]
standards: [ACI 318M-19]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 — Building Code Requirements for Structural Concrete

> Scope: standard register and chapter-level clause map for ACI 318M-19 (the
> SI-metric edition of ACI 318-19). Which chapter governs what, edition
> status, and how this source is kept separate from the AS 3600:2018 concept
> pages elsewhere in `2-concrete`. No clause text reproduced verbatim — see
> `raw/0-standards/ACI-318M-19.pdf` for the source.

## Summary

`[code]` ACI 318M-19, *Building Code Requirements for Structural Concrete
(ACI 318-19) and Commentary (ACI 318R-19)*, is the SI-metric edition of the
American Concrete Institute's model code for structural concrete buildings
and, where applicable, nonbuilding structures. First printing October 2019;
this copy is the printing incorporating updates through June 2020. It
supersedes ACI 318M-14. Code and Commentary are printed side by side —
Commentary section numbers are prefixed `R` (e.g. Cl 4.6 is Code, R4.6 is the
matching Commentary) and are explanatory only, never binding.

`[code]` The Code has no legal status on its own — it becomes mandatory only
when adopted by reference into a jurisdiction's general building code (in the
US, typically via ASCE/SEI 7 for loads and the *International Building Code*).
It is a **US code, developed for US practice and referencing US standards
(ASTM, ASCE/SEI 7, PCI, AWS, etc.)** — not a substitute for AS 3600:2018 on an
Australian project. It is being ingested here as a comparative/reference
source (e.g. for US-client or US-codes-basis-of-design projects, or to check
an alternative design method), not as a governing code for Australian work
under the NCC.

`[derived]` Where this wiki already has an AS 3600:2018 concept page covering
the same design topic (e.g. column slenderness, punching shear), the two
codes differ enough in load-combination basis, φ-factor philosophy, and
detailing formulae that a single merged page would misrepresent both. **Per
explicit human instruction this session, ACI 318M-19 content is kept on its
own `aci-`-prefixed pages, never merged into or used to extend an existing
`concrete-*.md` (AS 3600) page.** Both sets of pages live in the `2-concrete`
category folder per CLAUDE.md's folder map (the content is still "reinforced/
prestressed concrete"), but are distinguished by filename prefix. This is a
deliberate, human-directed exception to CLAUDE.md §3's default "extend the
existing page" rule — recorded here per §5's provenance/workflow intent, and
in `log.md`.

## Detail

### Chapters not given their own concept page

`[code]` Three early chapters are reference/administrative material, not
design concepts in their own right, and are summarised here instead of on a
dedicated page (mirroring how AS 3600's own Section 1 — scope, notation,
definitions — was not made into a concept page):

- **Chapter 1 — General** (Cl 1.1–1.10, pp. 9–14): legal scope and
  applicability of the Code, interpretation rules (`shall` is always
  mandatory, specific governs over general), the roles of the "building
  official" and "licensed design professional," construction-document and
  testing/inspection obligations (detailed in Chapter 26), and the process
  for approval of a special/alternative system not covered by the Code
  (Cl 1.10.1 — referenced by several later chapters as the escape valve for
  non-conforming systems).
- **Chapter 2 — Notation and Terminology** (Cl 2.1–2.3, pp. 15–46): ~500
  notation symbols (Cl 2.2) and ~200 defined terms (Cl 2.3). Not transcribed
  as a standalone glossary page — symbols and terms are defined inline on
  each concept page as they're used, consistent with this wiki's existing
  house style for AS 3600/AS 4100.
- **Chapter 3 — Referenced Standards** (Cl 3.1–3.2, pp. 47–50): the Code's
  own reference-standard list (ASTM, AWS, ASCE/SEI, PCI, ACI companion
  documents, etc.), version-dated per Cl 3.2. Key recurring references are
  listed below rather than reproducing the full list.

`[code]` Recurring referenced standards worth registering separately:

- **ASCE/SEI 7** — loads and load combinations (Chapter 5 is written to align
  with it); also the source of Seismic Design Category (SDC) assignment.
- **ASTM A615M/A706M/A996M** etc. — reinforcing bar material specifications
  (Chapter 20).
- **ACI 301M** — reference specification for construction contract documents
  (distinct from this Code, which is not itself a specification).
- **ACI 216.1M** — fire-resistance guidance, cross-referenced from Cl 4.11.
- **PCI MNL 120 / MNL 126** — precast/prestressed design handbooks,
  cross-referenced for precast tolerance and hollow-core design guidance.

### Chapter-level clause map

`[code]` Own-words chapter scope, from the Table of Contents (page refs are
to this printing and will drift with future printings — cite chapter/section
numbers, not pages):

| Part | Ch  | Scope (own words)                                                                                                                                                                                                                                                            | Wiki pages                             |
| ---- | --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------- |
| 1    | 1   | General: legal scope, interpretation, building official / licensed design professional roles, approval of special systems.                                                                                                                                                   | — (folded into this page, above)       |
| 1    | 2   | Notation and terminology.                                                                                                                                                                                                                                                    | — (folded into this page, above)       |
| 1    | 3   | Referenced standards.                                                                                                                                                                                                                                                        | — (folded into this page, above)       |
| 1    | 4   | Structural system requirements: materials, design loads, load paths, seismic-force-resisting system, diaphragms, strength/serviceability/durability/sustainability philosophy, structural integrity, fire, precast/prestressed/composite/plain-concrete system requirements. | [[aci318-structural-system-requirements]] |
| 2    | 5   | Loads: load factors and combinations.                                                                                                                                                                                                                                        | [[aci318-loads-and-load-combinations]] |
| 2    | 6   | Structural analysis: modeling assumptions, live-load arrangement, simplified/linear/second-order/inelastic/FE methods.                                                                                                                                                       | [[aci318-structural-analysis-methods]] (6.1-6.5), [[aci318-column-slenderness-and-moment-magnification]] (6.2.5, 6.6.4), [[aci318-second-order-and-advanced-analysis]] (6.6.3, 6.6.5, 6.7-6.9) |
| 3    | 7   | One-way slabs.                                                                                                                                                                                                                                                               | [[aci318-one-way-slab-design]]         |
| 3    | 8   | Two-way slabs.                                                                                                                                                                                                                                                               | [[aci318-two-way-slab-design-basis]] (8.1-8.4), [[aci318-two-way-slab-reinforcement-and-shear-detailing]] (8.5-8.9) |
| 3    | 9   | Beams.                                                                                                                                                                                                                                                                       | [[aci318-beam-design-basis-and-strength]] (9.1-9.5), [[aci318-beam-reinforcement-limits-and-detailing]] (9.6-9.7), [[aci318-joists-and-deep-beams]] (9.8-9.9) |
| 3    | 10  | Columns.                                                                                                                                                                                                                                                                     | [[aci318-column-design]] (+ slenderness: [[aci318-column-slenderness-and-moment-magnification]]) |
| 3    | 11  | Walls.                                                                                                                                                                                                                                                                       | [[aci318-wall-design]] |
| 3    | 12  | Diaphragms.                                                                                                                                                                                                                                                                  | [[aci318-diaphragm-design]] |
| 3    | 13  | Foundations (shallow and deep).                                                                                                                                                                                                                                              | [[aci318-foundation-design]] |
| 3    | 14  | Plain concrete.                                                                                                                                                                                                                                                              | [[aci318-plain-concrete-design]] |
| 4    | 15  | Beam-column and slab-column joints.                                                                                                                                                                                                                                          | [[aci318-beam-column-and-slab-column-joints]] |
| 4    | 16  | Connections between members: precast connections, connections to foundations, composite horizontal shear, brackets/corbels.                                                                                                                                                  | [[aci318-connections-between-members]] |
| 4    | 17  | Anchoring to concrete: cast-in and post-installed anchors, tension/shear strength, seismic anchor design.                                                                                                                                                                    | [[aci318-anchoring-general-and-tensile-strength]] (17.1-17.6), [[aci318-anchoring-shear-interaction-seismic-and-shear-lugs]] (17.7-17.11) |
| 5    | 18  | Earthquake-resistant structures: moment frames (ordinary/intermediate/special), structural walls, diaphragms, foundations by seismic tier.                                                                                                                                   | [[aci318-earthquake-general-and-ordinary-intermediate-frames]] (18.1-18.5), [[aci318-special-moment-frames]] (18.6-18.9), [[aci318-special-structural-walls]] (18.10-18.11), [[aci318-earthquake-diaphragms-foundations-and-non-sfrs-members]] (18.12-18.14) |
| 6    | 19  | Concrete: design and durability requirements.                                                                                                                                                                                                                                | [[aci318-concrete-design-properties-and-durability]] |
| 6    | 20  | Steel reinforcement properties, durability, and embedments.                                                                                                                                                                                                                  | [[aci318-reinforcement-properties-durability-and-embedments]] |
| 7    | 21  | Strength reduction factors (φ).                                                                                                                                                                                                                                              | [[aci318-strength-reduction-factors]] |
| 7    | 22  | Sectional strength: flexure, axial, one-way shear, two-way shear, torsion, bearing, shear friction.                                                                                                                                                                          | [[aci318-sectional-strength-flexure-and-axial]] (22.2-22.4), [[aci318-one-way-shear-strength]] (22.5), [[aci318-two-way-shear-strength]] (22.6), [[aci318-torsional-strength]] (22.7), [[aci318-bearing-and-shear-friction]] (22.8-22.9) |
| 7    | 23  | Strut-and-tie method.                                                                                                                                                                                                                                                        | [[aci318-strut-and-tie-method]] |
| 7    | 24  | Serviceability: deflection, distribution of flexural reinforcement, shrinkage/temperature steel, prestressed stress limits.                                                                                                                                                  | [[aci318-serviceability-deflection-and-cracking]] |
| 8    | 25  | Reinforcement details: spacing, hooks/crossties/bend diameters, development, splices, bundled bars, transverse reinforcement, post-tensioning anchorages.                                                                                                                    | [[aci318-reinforcement-spacing-hooks-and-development]] (25.1-25.4), [[aci318-splices-bundled-bars-and-transverse-reinforcement]] (25.5-25.7), [[aci318-post-tensioning-anchorages-and-anchorage-zones]] (25.8-25.9) |
| 9    | 26  | Construction documents and inspection.                                                                                                                                                                                                                                       | [[aci318-construction-documents-concrete-materials-and-production]] (26.1-26.5), [[aci318-reinforcement-anchors-embedments-precast-and-formwork-requirements]] (26.6-26.11), [[aci318-concrete-acceptance-testing-and-inspection]] (26.12-26.13) |
| 10   | 27  | Strength evaluation of existing structures.                                                                                                                                                                                                                                  | [[aci318-strength-evaluation-of-existing-structures]] |
| App  | A   | Design verification using nonlinear response history analysis.                                                                                                                                                                                                               | [[aci318-nonlinear-response-history-analysis]] |
| App  | B   | Steel reinforcement information (reference tables).                                                                                                                                                                                                                          | [[aci318-steel-reinforcement-size-tables]] (reference tables, filed in references/) |
| App  | C   | Equivalence between SI-metric, MKS-metric and US customary units for non-homogeneous equations.                                                                                                                                                                              | [[aci318-unit-equivalence-tables]] (reference tables, filed in references/) |

## Worked reference

None yet — add a worked clause application here once a concept page below
exercises a specific clause with numbers.

## Contradictions

None recorded against AS 3600 pages — by design, this source is not compared
clause-by-clause against AS 3600 (they are two independent, non-overlapping
jurisdictional codes; see the separation note in Summary above). A genuine
disagreement between ACI 318M-19 and another **ingested ACI-family or
US-code source** would still be recorded here per CLAUDE.md §4/§5.

## Related

Concept pages compiled from this standard are listed in the chapter map
above and in [[index]]. Ingest of Chapters 4-27 and Appendices A-C is complete, chapter by chapter
per the phased plan agreed with the human — see `log.md` for phase-by-phase
status. Not ingested as pages: Chapters 1-3 (summarised above), the
References list (printed pp. 595-613) and the Index (pp. 615-623). Appendix B
and C are data tables, filed under `2-concrete/references/`.

## Sources

- `raw/0-standards/ACI-318M-19.pdf` — ACI 318M-19, *Building Code
  Requirements for Structural Concrete and Commentary*, American Concrete
  Institute, first printing October 2019 (this copy: printing incorporating
  updates through June 2020). 628 pages, Code and Commentary side by side.
