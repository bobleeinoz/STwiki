---
title: Crane runway beam composition, dimensions and properties
category: 1-steelwork
tags: [crane-runway-beam, monorail-beam, built-up-section, mining, material-handling]
standards: [AS 4100:1998, AS 1418]
status: draft
reviewed: 2026-09-28
---

# Crane runway beam composition, dimensions and properties

> Scope: standard crane runway beam built-up sections (Welded Beam or
> Universal Beam with a Parallel Flange Channel top-flange cap) as
> tabulated by the ASI *Design Capacity Tables for Structural Steel, Vol 1:
> Open Sections* Part 13 — composition, dimensions and section properties
> only. **No design method** is given here; AS 4100 and the crane loading
> standard AS 1418 (series) give limited explicit guidance on crane runway
> and monorail beam design, and the tabulated source itself points
> elsewhere for the method (see Detail).

## Summary

`[practice]` A crane runway beam supporting a top-running overhead travelling
crane is commonly built up as a Welded Beam (WB) or Universal Beam (UB)
with a Parallel Flange Channel (PFC) welded/bolted to the top flange, web
down ("channel cap"), to give extra lateral (y-axis) stiffness and strength
for the horizontal crane surge/lateral loads that a bare I-section is weak
against. The ASI *Design Capacity Tables for Structural Steel, Vol 1*
(DCT/V1/03-1999) Table 13-1 tabulates the composition (WB/UB + PFC pairing),
approximate mass, area, and section properties about both axes (including
a "Top F" — top-flange, i.e. channel-side — modified `I_y`, `Z_y`) for the
common combinations.

`[practice]` This is a **geometric properties reference only**. Neither
AS 4100 nor this DCT gives a full crane-runway-beam design method; the DCT
points to Woolcock, Kitipornchai & Bradford, *Design of Portal Frame
Buildings*, 3rd ed., AISC 1999, for the design criteria, worked design
capacity checks and further background. That reference is not in `raw/`
and its method has not been ingested into this wiki.

## Detail

### Table 13-1 — composition and properties

`[practice]` Two composition families are tabulated: **Welded Beams with
Parallel Flange Channels** (e.g. 1200WB249 + 380PFC) and **Universal Beams
with Parallel Flange Channels** (e.g. 610UB125 + 380PFC, down to
360UB44.7 + 300PFC). For each combination the table gives: overall depth
`d` × width `b`, mass per metre, gross area `A_g`, centroid location `y_c`,
`I_x`/`Z_x` (top and bottom, since the composite section is not symmetric
about the x-axis once the channel is added), `r_x`, `I_y`/`r_y` for the
composite section and a separate "Top F" `I_y`/`Z_y` for checks localised
to the top-flange/channel region, plus torsion (`J`) and warping (`I_w`)
constants.

`[practice]` Per the table's own notes: `I_y (Top F) = I_x` (of the channel
alone) `+ I_y` (of the Universal or Welded Beam alone) `/ 2`; `Z_y (Top F)
= I_y (Top F) / (b/2)`. These are approximations for assessing the
composite top-flange region, not full transformed-section properties.

### Design guidance gap

`[derived]` AS 4100:2020's crane hook comes from Cl 1.1.1 (scope includes
cranes) and the AS 1418 load pointer at Cl 3.2.1(b) — see
[[as-4100-2020-steel-structures]] — but the standard does not carry a
dedicated crane-runway-beam clause set (biaxial bending from vertical wheel
loads + horizontal surge, fatigue from repeated crane passes, and
lateral-torsional buckling of the asymmetric composite section are all
relevant but must be assembled from the general bending, combined-actions
and fatigue provisions already on this wiki). Until a dedicated source is
ingested, treat crane runway beam design as: geometry from this page,
loads from AS 1418, and strength/serviceability/fatigue checks assembled
from [[steel-beam-section-moment-capacity]], [[steel-beam-member-moment-capacity]],
[[steel-combined-actions-section-capacity]], [[steel-combined-actions-member-capacity]]
and [[steel-fatigue-design]] — with the asymmetric/composite section
properties above as the geometric input.

![[dct-table-13.1-crane-runway-beams.png]]
*DCT Vol 1 Table 13-1 — crane runway beams: composition, dimensions and
properties (source: DCT/V1/03-1999, p. 13-3).*

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[asi-design-capacity-tables-vol1-open-sections]] — source register
  (Part 13).
- [[as-4100-2020-steel-structures]] — AS 1418 crane-load pointer (Cl 3.2.1(b)).
- [[steel-beam-section-moment-capacity]], [[steel-beam-member-moment-capacity]]
  — bending capacity of the composite section once properties are taken
  from here.
- [[steel-combined-actions-section-capacity]], [[steel-combined-actions-member-capacity]]
  — vertical + lateral (surge) combined bending.
- [[steel-fatigue-design]] — repeated crane-load fatigue assessment.

## Sources

- `raw/1-steelwork/ASI-design-capacity-tables-volume-1-pdf.pdf`, Part 13
  (pp. 13-1 to 13-3), DCT/V1/03-1999. References Woolcock, S.T.,
  Kitipornchai, S. and Bradford, M.A., *Design of Portal Frame Buildings*,
  3rd ed., Australian Institute of Steel Construction, 1999 (not in `raw/`,
  not ingested).
