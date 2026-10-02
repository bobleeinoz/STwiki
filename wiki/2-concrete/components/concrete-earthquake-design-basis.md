---
title: Earthquake design basis — ductility/performance factors and general requirements
category: 2-concrete
tags: [earthquake, seismic, ductility-factor, structural-performance-factor]
standards: [AS 3600:2018 Cl 14.1, AS 3600:2018 Cl 14.2, AS 3600:2018 Cl 14.3, AS 3600:2018 Cl 14.4]
status: draft
reviewed: 2026-09-16
---

# Earthquake design basis

> Scope: AS 3600 Section 14 general provisions — applicability (Cl 14.1),
> definitions (Cl 14.2), the structural ductility/performance factor table
> (Cl 14.3), and general earthquake design requirements (Cl 14.4: strength,
> drift, frames, walls, diaphragms, ductile-beam detailing, robustness).
> Detailing for IMRFs and structural walls is split out —
> [[concrete-earthquake-imrf-detailing]] and
> [[concrete-earthquake-structural-walls-detailing]].

## Summary

`[code]` Section 14 applies to reinforced/prestressed concrete structures and
members forming part of buildings to which AS 1170.4 applies (Cl 14.1). Plain
concrete cannot resist earthquake actions, except pedestals, footings and
pavements deemed to satisfy Cl 2.1.2 and this section. The structural
ductility factor (`μ`) chosen governs which detailing route applies: `1 < μ ≤
3` uses AS 3600 itself (this Standard and Section 14); `μ > 3` requires
NZS 1170.5/NZS 3101 design under the AS 1170.4 Hazard Map with Ductility
Class E reinforcement; Importance Level 4 structures must remain serviceable
for an Importance Level 2 design event.

## Detail

### Key definitions (Cl 14.2)

`[code]` Selected definitions (AS 1170.4 definitions apply generally; where
they differ, Section 14's own apply): **IMRF** — a moment-resisting frame
detailed to this section for moderate ductility; **OMRF** — a moment-
resisting frame with no special earthquake detailing except columns (Cl
14.4); **structural wall** — a loadbearing or non-loadbearing wall connected
to floor/roof diaphragms that attracts horizontal earthquake/wind actions,
classified Non-Ductile / Limited Ductile / Moderately Ductile, with short or
squat walls (Cl 14.4.4.4) always treated as non-ductile; `μ` — numerical
assessment of a structure's ability to sustain inelastic cyclic
displacement; `Sp` — numerical assessment of the whole building's additional
survival capacity.

### Structural ductility and performance factors (Cl 14.3, Table 14.3)

`[code]` `μ` and `Sp` are read from Table 14.3 by structural system; where a
combined system mixes ductilities, the governing (least-ductile) element's
factors apply to the whole system, and Section 2.2 plus the relevant Section
14 clauses govern each element type. Systems not covered require rational
analysis to derive `μ` and `Sp`.

![[as3600-table-14.3-structural-ductility-and-performance-factors.png]]
*Table 14.3 — structural ductility factor (μ) and structural performance
factor (Sp), by structural system description (AS 3600:2018).*

| Structural system | `μ` | `Sp` | `Sp/μ` |
| --- | --- | --- | --- |
| Special moment-resisting frames (fully ductile), NZS 1170.5/NZS 3101, AS 1170.4 Hazard Map | 4 | 0.67 | 0.17 |
| Ductile structural walls, NZS 1170.5/NZS 3101, Hazard Map | 4 | 0.67 | 0.17 |
| Ductile partially/fully coupled walls, NZS 1170.5/NZS 3101, Hazard Map | 4 | 0.67 | 0.17 |
| IMRFs — Cl 2.2 + Cl 14.4/14.5 | 3 | 0.67 | 0.22 |
| Combined IMRF + moderately ductile walls — Cl 2.2 + Cl 14.4/14.5/14.7 | 3 | 0.67 | 0.22 |
| Moderately ductile structural walls — Cl 2.2 + Cl 14.4/14.7 | 3 | 0.67 | 0.22 |
| OMRFs — Cl 2.2 + Cl 14.4 | 2 | 0.77 | 0.38 |
| OMRFs + limited ductile shear walls — Cl 2.2 + Cl 14.4/14.6 | 2 | 0.77 | 0.38 |
| Limited ductile structural walls — Cl 2.2 + Cl 14.4/14.6 | 2 | 0.77 | 0.38 |
| Non-ductile structural walls — Cl 2.2 + Cl 14.4 | 1 | 0.77 | 0.77 |

### General earthquake design requirements (Cl 14.4)

`[code]` **Strength & drift** (Cl 14.4.1–14.4.2): all members designed for
AS 1170.4 earthquake loads per Cl 2.2; vertical load-bearing elements
designed for the calculated inter-storey drift; prefabricated/non-structural
attachments must accommodate relative floor movement (joints allow the
movement; connections have ductility/rotation capacity to avoid non-ductile
failure).

`[code]` **Moment-resisting frames** (Cl 14.4.3): OMRF beams need ≥2
continuous longitudinal bars top and bottom, fully developed at support
faces; SFRC members need a tensile reinforcement ratio (steel + tendons)
≥0.004 (interim requirement, low-conventional-reinforcement SFRC). Any OMRF
column in the lateral system with unsupported length `Lu ≤ 5D` must be
detailed per Cl 14.5.4–14.5.5 (see
[[concrete-earthquake-imrf-detailing]]).

`[code]` **Structural walls** (Cl 14.4.4): designed per Section 10 or 11 as
appropriate, except the Cl 11.5 simplified vertical-compression method is
restricted to non-ductile walls; limited/moderately ductile walls also
conform with Cl 14.6/14.7 respectively (see
[[concrete-earthquake-structural-walls-detailing]]). Interconnected wall
groups distribute in-plane load by linear-elastic analysis in proportion to
gross-section stiffness, with vertical shear designed at interconnected
edges. Axial load limit for `μ = 1` elements: `N*/Ag < 0.2 f'c` (`N*` = sum
of AS 1170.4 Cl 6.2.2 seismic weights). Short/squat walls (aspect ratio <2)
are designed as non-ductile via the Section 12 strut-and-tie method.

`[code]` **Diaphragms** (Cl 14.4.5): always non-ductile, designed to Section
15 (see [[concrete-diaphragm-design]]); inertia forces from equivalent
static analysis per AS 1170.4 with `μ = 1.0`, `Sp = 0.77`; lower-floor forces
incorporate higher-mode effects (or use the maximum seismic distribution
factor at any floor); mass assumed evenly distributed over the diaphragm.

`[code]` **Ductile beam/band-beam detailing** (Cl 14.4.6, for `μ > 1.25` and
`μ ≤ 3`): in potential plastic-hinge zones (excluding a cast-in-place T-/L-
beam flange in compression), compression-face reinforcement ≥1/3 of the
tension-face ultimate capacity, and neutral-axis depth `ku0 ≤ 0.25`.

`[code]` **Robustness** (Cl 14.4.7): checked per Cl 2.1.3; stairs and ramps
must remain serviceable under maximum design earthquake actions.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-earthquake-imrf-detailing]] — Cl 14.5, IMRF beam/slab/column/
  joint detailing for `μ = 3`.
- [[concrete-earthquake-structural-walls-detailing]] — Cl 14.6–14.7, limited
  and moderately ductile wall detailing.
- [[concrete-diaphragm-design]] — Section 15, diaphragm design actions.
- [[concrete-wall-design-basis-and-classification]] — Section 11 wall
  routing that Cl 14.4.4 overlays.
- [[concrete-non-flexural-members-and-strut-tie-models]] — Section 12,
  strut-and-tie method for short/squat non-ductile walls.
- [[concrete-limit-state-design-basis]] — Cl 2.1.2/2.1.3/2.1.5, general
  applicability and robustness/fatigue framework this section plugs into.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clauses 14.1–14.4.
