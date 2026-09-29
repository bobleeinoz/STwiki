---
title: AISC/ASI Design Capacity Tables for Structural Steel — Volume 1: Open Sections (source register)
category: 1-steelwork
tags: [source-register, design-aid, section-properties, capacity-tables, open-sections, AS4100-1998]
standards: [AS 4100:1998]
status: draft
reviewed: 2026-09-29
---

# AISC/ASI Design Capacity Tables for Structural Steel — Volume 1: Open Sections

> Scope: source register for *Design Capacity Tables for Structural Steel,
> Volume 1: Open Sections*, third edition (DCT/V1/03-1999), Australian
> Institute of Steel Construction (AISC — now the Australian Steel
> Institute). A 288-page design **aid**, not a standard: it pre-computes
> AS 4100 section/member capacities for the standard range of Australian
> hot-rolled and welded open sections. No verbatim table values reproduced
> here beyond a handful of illustrative rows/figures — see `raw/` for the
> full lookup tables.

## Summary

`[practice]` This publication (DCT Vol 1) is a **design aid keyed to
AS 4100—1998** (see cover: "Limit States Edition to AS 4100-1998"), not a
standard in its own right. It tabulates section properties and pre-computed
`AS 4100` design capacities (`φM_s`, `φN_s`, `φN_c`, `φN_t`, bolt/weld
capacities, etc.) for the full range of Australian-made hot-rolled and
welded **open** sections, so a designer can look up a capacity instead of
recomputing it from first principles. Companion **Volume 2** (also in
`raw/1-steelwork/`) covers structural steel hollow sections and is a
separate source, not yet ingested.

`[practice]` Vintage flag: this is the **third edition (1999)**, keyed to
**AS 4100—1998**. The current standard in this wiki is
[[as-4100-2020-steel-structures]] (AS 4100:2020 + Amendment 1). No AISC/ASI
successor DCT Vol 1 edition keyed to AS 4100:2020 was found in `raw/`. Every
formula sampled during this ingest (moment amplification `M* = δ_b M_m*`,
`φN_s = φ k_f A_n f_y`, biaxial section/member interaction, bolt bearing
`V_b = 3.2 d_f t_p f_up`) matches the current AS 4100:2020 clause text
already on this wiki's steel pages, clause-number differences aside — no
contradiction found in the sampled material.

`[derived]` **2026-09-29 follow-up pass — full-table transcription and
cross-check for Parts 2, 3, 5 and 6.** Every numeric value in DCT Vol 1
Parts 2 (Materials), 3.1 (section properties, incl. the holed-tension-flange
Tables 3.1-14 to 3.1-17), 3.2 (fire surface-area/`k_sm` tables), 5 (maximum
UDL, section moment, and member moment capacity tables) and 6 (axial
compression member capacity tables) — roughly **12,000 individual numbers**
across ~90 tables — was transcribed from the source page images and
programmatically recomputed from AS 4100:2020's own clause formulae
(`φM_sx = 0.9 f_y Z_ex`; the Cl 5.6.1.1 elastic flexural-torsional buckling
`φM_b`; and the Cl 6.3.3 member slenderness-reduction `φN_c = α_c φN_s`
using each section's tabulated `A_g`, `r_x`, `r_y`, `I_y`, `J`, `I_w`).
**Zero discrepancies** were found against the current standard's formulae
in this recomputation, beyond one isolated source print anomaly (flagged
inline on [[asi-dct-vol1-beam-capacity-tables]], 700WB115 serviceability
load at 5.0 m span). This substantially raises confidence in the *formula*
match between DCT Vol 1 (1998-vintage) and AS 4100:2020 for these five
Parts specifically — see [[asi-dct-vol1-open-section-properties]],
[[asi-dct-vol1-fire-surface-area-tables]],
[[asi-dct-vol1-beam-capacity-tables]] and
[[asi-dct-vol1-compression-capacity-tables]] for the full transcribed
tables. **Parts 7 (tension), 8 (combined actions), 9 (connections), 10
(detailing), 11 (plates) and 13 (crane runway beams)** were not
table-transcribed in this pass — only Part-level scope and a handful of
illustrative values are recorded below; their capacity values remain a
1998-vintage cross-check only, not a substitute for a current calculation,
and should be re-verified before use on anything safety-critical.

`[practice]` Steel grades and product standards covered (Section 2.1):
Welded Beams/Columns (WB, WC) Grade 300/400 to AS/NZS 3679.2; Universal
Beams/Columns (UB, UC), Parallel Flange Channels (PFC), Taper Flange Beams
(TFB), Equal/Unequal Angles (EA, UA) Grade 300 to AS/NZS 3679.1; Tees cut
from UB/UC (BT, CT) Grade 300; round/square bars and square-edge flats
(dimensions/properties only, no capacities). The Grade 300 designation also
covers OneSteel's 300PLUS™ product.

## Detail

`[practice]` Own-words map of the 13 parts (Contents, pp. iii, 4–13 of the
PDF):

| Part | Title | Own-words scope | Wiki pages this extends |
|---|---|---|---|
| 1 | Introduction | Publication scope, how to use the tables, reference standards list. | — |
| 2 | Materials | Table T2.1 design `f_y`/`f_u` by product standard, grade and thickness; Table T2.2 elastic constants. Matches AS 4100 Table 2.1 values already on the wiki. **Full table now on [[asi-dct-vol1-open-section-properties]].** | [[steel-materials-and-design-strengths]], [[asi-dct-vol1-open-section-properties]] |
| 3 | Section Properties | Type-(A) dimensions/properties tables (`A_g`, `I_x`, `I_y`, `Z_x`, `Z_y`, `S_x`, `S_y`, `J`, `I_w`) and type-(B) AS 4100 assessment properties (compactness C/N/S, effective section modulus `Z_e`, form factor `k_f`) per section, per grade, per bending axis, incl. holed-tension-flange variants (Tables 3.1-14 to 3.1-17). Worked example (360UB44.7) shows the `Z_e`/`k_f` derivation. Fire design surface-area/mass-ratio tables (`k_sm`) for 6 exposure cases (Fig 3.1). **Full tables now on [[asi-dct-vol1-open-section-properties]] and [[asi-dct-vol1-fire-surface-area-tables]].** | [[steel-beam-section-moment-capacity]], [[steel-compression-member-capacity]], [[steel-fire-design]], [[asi-dct-vol1-open-section-properties]], [[asi-dct-vol1-fire-surface-area-tables]] |
| 4 | Methods of Structural Analysis | Guidance on first-order elastic analysis with moment amplification (`δ_b`, `δ_s`, `c_m`) as the practical method (second-order/plastic/advanced analysis flagged as out of scope for a hand-calc design aid); elastic flexural buckling load `N_om = π²EI/(k_eL)²`. | [[steel-structural-analysis-methods]], [[steel-member-effective-length-and-frame-buckling]] |
| 5 | Members Subject to Bending | Maximum UDL design tables (strength: moment- and shear-governed; serviceability: `L/250` deflection- and first-yield-governed) for simply-supported beams with full lateral restraint; design section moment/web capacity tables; design member moment capacity tables (no full lateral restraint) by segment length. **Full tables now on [[asi-dct-vol1-beam-capacity-tables]].** | [[steel-beam-section-moment-capacity]], [[steel-beam-member-moment-capacity]], [[steel-web-shear-and-bearing]], [[asi-dct-vol1-beam-capacity-tables]] |
| 6 | Members Subject to Axial Compression | `φN_s = φ k_f A_n f_y` design section capacity; `φN_c` design member capacity tables/graphs vs effective length `L_e`, split into (A) x-axis and (B) y-axis buckling series. **Full tables now on [[asi-dct-vol1-compression-capacity-tables]].** | [[steel-compression-member-capacity]], [[asi-dct-vol1-compression-capacity-tables]] |
| 7 | Members Subject to Axial Tension | `φN_t` design section capacity tables per section/grade. | [[steel-tension-member-capacity]] |
| 8 | Members Subject to Combined Actions | Section and member capacity checks for compression+uniaxial/biaxial bending and tension+uniaxial/biaxial bending; worked braced beam-column example; angles subject to bending (with/without continuous lateral restraint); eccentrically loaded single angles in trusses. | [[steel-combined-actions-section-capacity]], [[steel-combined-actions-member-capacity]] |
| 9 | Connections | Bolt types/categories (Table T9.1: 4.6/S, 8.8/S, 8.8/TF, 8.8/TB), design capacities of commonly used bolts (shear, tension, bearing incl. `V_b = 3.2 d_f t_p f_up` local bearing / `V_b = a_e t_p f_up` end-plate tearout), weld capacities (butt, fillet, plug/slot, groups), and "standardised structural connections" (rationalised standard components/parameters). | [[steel-bolt-design]], [[steel-weld-design]], [[steel-connection-design-requirements]] |
| 10 | Detailing Parameters | Rationalised fabrication dimensions (setbacks `a`, `w`, `k`, `m`) per section type, gauge lines, bolt/wrench dimensions and masses. | [[steel-connection-standard-detailing-dimensions]] |
| 11 | Plates | Floor-plate pattern/preferred-size tables; maximum design load tables for flat plates in bending (strength and serviceability limit states). | — (no dedicated wiki page yet) |
| 12 | (unused — Rails, per the outline cover page, folded into Vol 2/other AISC publications) | — | — |
| 13 | Crane Runway Beams & Monorail Beams | Table 13-1: composition, dimensions and properties of common crane runway beam built-up sections (WB/UB + PFC top-flange channel combinations). Notes AS 4100/AS 1418 give little explicit crane-runway-beam design guidance and points to Woolcock, Kitipornchai & Bradford, *Design of Portal Frame Buildings*, 3rd ed., AISC 1999, for the design method itself. | [[steel-crane-runway-beam-composition]] |

`[derived]` The cover-page "Part Twelve: Rails" tab shown in the directory
photo does not correspond to any content between Parts 11 and 13 in this
copy — Part 11 (Plates) ends and Part 13 (Crane Runway Beams) begins
immediately after. Rails content, if it exists, was not located in this
ingest pass; flagged for the human rather than assumed absent.

### Table series convention (applies through Parts 3, 5–9, 11, 13)

`[practice]` Each section-property/capacity part uses a consistent table
pairing: an (A)-series table of raw dimensions/properties, followed
immediately by a (B)-series table of AS 4100 design assessment values
(compactness, `Z_e`, `k_f`, or the design capacity itself) for the same
section set. Member-capacity-vs-length parts (6, and parts of 5) add a
graph of `φN_c` or `φM_b` vs effective/segment length directly after the
corresponding table. This pairing is the DCT's core lookup mechanic and is
why the publication functions as a look-up companion to AS 4100 rather than
a restatement of it.

## Worked reference

`[derived]` None yet on this wiki. The DCT itself carries worked examples
at 3.2.4 (`Z_e`, `k_f` for 360UB44.7), 5.1.6, 5.2.3, 5.2.4.2, 6.5, and 8.6
(braced beam-column) — useful models if a wiki worked-example page is
built from this source later.

## Contradictions

None recorded. See the vintage-flag paragraph in Summary — DCT Vol 1 is a
1998-vintage design aid; treat any apparent numeric mismatch against a
current AS 4100:2020 hand calc as a version difference to re-verify, not a
standing contradiction, until specifically checked.

## Related

- [[as-4100-2020-steel-structures]] — current standard; this DCT is a
  design aid keyed to the superseded 1998 edition.
- [[steel-materials-and-design-strengths]], [[steel-beam-section-moment-capacity]],
  [[steel-beam-member-moment-capacity]], [[steel-web-shear-and-bearing]],
  [[steel-compression-member-capacity]], [[steel-tension-member-capacity]],
  [[steel-combined-actions-section-capacity]], [[steel-combined-actions-member-capacity]],
  [[steel-bolt-design]], [[steel-weld-design]], [[steel-connection-design-requirements]],
  [[steel-connection-standard-detailing-dimensions]], [[steel-fire-design]],
  [[steel-structural-analysis-methods]], [[steel-member-effective-length-and-frame-buckling]]
  — extended with DCT cross-references this ingest.
- [[steel-crane-runway-beam-composition]] — new page, earlier ingest pass.
- [[asi-dct-vol1-open-section-properties]], [[asi-dct-vol1-fire-surface-area-tables]],
  [[asi-dct-vol1-beam-capacity-tables]], [[asi-dct-vol1-compression-capacity-tables]]
  — new full-table pages, this 2026-09-29 follow-up pass (Parts 2, 3, 5, 6).

## Sources

- `raw/1-steelwork/ASI-design-capacity-tables-volume-1-pdf.pdf` — *Design
  Capacity Tables for Structural Steel, Volume 1: Open Sections*, 3rd
  edition, DCT/V1/03-1999, Australian Institute of Steel Construction, 1999
  (ISBN 0-909945-85-3). Scanned/image PDF, no text layer — read visually
  (page renders). **2026-09-29 pass:** every page of Parts 2, 3.1, 3.2, 5
  and 6 (pp. 14–56, 76–133 of the PDF) was rendered and manually transcribed
  cell-by-cell into [[asi-dct-vol1-open-section-properties]],
  [[asi-dct-vol1-fire-surface-area-tables]],
  [[asi-dct-vol1-beam-capacity-tables]] and
  [[asi-dct-vol1-compression-capacity-tables]]. Parts 7–11 and 13 (pp.
  178–288 of the PDF) were **not** transcribed in this pass — Contents/
  outline bookmarks and a representative page sample per Part were used to
  map their scope only, per the earlier ingest pass. Companion
  `raw/1-steelwork/ASI-design-capacity-tables-volume-2.pdf` (hollow
  sections) not yet ingested.
