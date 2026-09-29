---
title: Concrete durability design — exposure classification and cover
category: 2-concrete
tags: [durability, exposure-classification, cover, corrosion]
standards: [AS 3600:2018 Cl 4.1-4.10]
status: draft
reviewed: 2026-09-12
---

# Concrete durability design — exposure classification and cover

> Scope: AS 3600's durability design method (Section 4) — exposure
> classification, concrete quality/curing by exposure, abrasion, freeze-thaw,
> aggressive/saline soils, chemical content limits, and cover to
> reinforcement/tendons.

## Summary

`[code]` Section 4 applies to a 50-year design life (±20%) as the reference
case (Cl 4.1) — more stringent requirements suit longer-life structures
(monumental), some relaxation suits shorter-life (temporary) structures. The
method (Cl 4.2) is: classify exposure (Cl 4.3) → meet the concrete
quality/curing requirement for that class (Cl 4.4/4.5) → apply any
additional checks that bite (abrasion Cl 4.6, freeze-thaw Cl 4.7, aggressive
soils Cl 4.8, alkali-aggregate reaction management) → meet chemical-content
restrictions (Cl 4.9) if reinforced/tendoned → meet cover requirements
(Cl 4.10). The clause explicitly notes conformance doesn't guarantee
durability — it's a deemed-to-satisfy minimum, not a durability guarantee.

## Detail

### Exposure classification (Cl 4.3)

`[code]` Classification (A1, A2, B1, B2, C1, C2, or U for anything outside
the table) comes from Table 4.3 — a large table by
environment: in-ground, interior, above-ground exterior by distance from
coast and climatic zone, in-water, maritime spray/tidal zones, and "other".

![[as3600-table-4.3-exposure-classifications-1.png]]
![[as3600-table-4.3-exposure-classifications-2.png]]
*Table 4.3 — exposure classifications, by surface and exposure environment
(AS 3600:2018).*

Own-words summary of the logic, not the values: severity generally increases
with proximity to coast/sea, industrial atmosphere, and exposure to
wetting/drying cycles; A1 is the mildest (e.g. damp-proofed footings,
enclosed residential interiors), C2 the most severe of the *lettered* classes
(tidal/splash zone of maritime structures), with U reserved for anything the
table doesn't cover (e.g. aggressive soils below a magnesium-sulfate
threshold, running/soft water) and requiring its own assessment. A member's
classification is the *most severe* of any of its surfaces for concrete
*quality*, but the classification of the specific surface for *cover*
purposes (Cl 4.3.1). Unreinforced members default to A1 unless the
environment is aggressive to plain concrete.

`[practice]` A one-sided exterior exposure may use a lower concrete quality
grade than Table 4.4 would otherwise require, provided cover from that face
is increased by a stated amount — a workable trade in practice when one face
is genuinely benign and the other governs.

### Concrete quality and curing (Cl 4.4–4.5)

`[code]` Classes A1–C2 require a minimum `f'c` and a minimum curing regime
(Table 4.4), or alternatively a minimum strength at
strip/de-mould.

![[as3600-table-4.4-minimum-strength-curing-requirements.png]]
*Table 4.4 — minimum strength and curing requirements for concrete, by
exposure classification (AS 3600:2018).*

B2/C1/C2 concrete must be specified as "special class" per
AS 1379, explicitly stating the exposure classification and any quality
limits. Class U has no table — quality, cover and other parameters must be
set to suit the specific aggressive environment.

### Abrasion, freezing/thawing, aggressive soils (Cl 4.6–4.8)

`[code]` Abrasion (Cl 4.6): minimum `f'c` by traffic type (footpaths through
to steel-wheeled traffic), generally increasing
with traffic severity.

![[as3600-table-4.6-strength-requirements-abrasion.png]]
*Table 4.6 — strength requirements for abrasion, by member/traffic type
(AS 3600:2018).*

Freeze-thaw (Cl 4.7): minimum `f'c` banded by
cycle frequency (occasional vs. frequent, a numeric annual-cycle threshold in
the clause text itself), plus an air-entrainment percentage range by
aggregate size. Aggressive soils (Cl 4.8): sulfate/acid-sulfate soils get
their own exposure-classification table (4.8.1) keyed to sulfate
concentration and pH, split by soil permeability; saline soils get a
separate strength-and-cover table (4.8.2) keyed to soil electrical
conductivity. `[practice]` Where more than one aggressive chemical is
present (e.g. sulfate + magnesium, or sulfate + chloride), the clause notes
combined effects can be more or less severe than either alone — treat
Table 4.8.1 as a simplified starting point, not a full chemistry assessment,
per its own notes.

![[as3600-table-4.8.1-exposure-classification-sulfate-soils-1.png]]
![[as3600-table-4.8.1-exposure-classification-sulfate-soils-2.png]]
*Table 4.8.1 — exposure classification for concrete in sulfate/acid-sulfate
soils, by sulfate concentration, pH and soil permeability (AS 3600:2018).*

![[as3600-table-4.8.2-strength-cover-saline-soils.png]]
*Table 4.8.2 — strength and cover requirements for concrete in salt-rich
soils and areas affected by salinity (AS 3600:2018).*

### Chemical content restrictions (Cl 4.9)

`[code]` Chemical admixtures must conform to AS 1478.1; chemical content in
the hardened concrete must conform to AS 1379 — relevant because chlorides
and similar constituents are deleterious to durability.

### Cover to reinforcement and tendons (Cl 4.10)

`[code]` Required cover is the **greatest** of: the Cl 4.8 aggressive-soil
requirement (if applicable), the Cl 4.10.2 placement/compaction requirement,
and the Cl 4.10.3 corrosion-protection requirement — unless Section 5 fire
resistance demands more (see [[concrete-fire-resistance-design]]).

- **Placement cover** (4.10.2): governed by member size/shape, reinforcement/
  tendon/duct configuration, aggregate size and placement direction — a cover
  at least equal to bar/tendon nominal size or maximum aggregate size
  (whichever governs) is deemed sufficient for this check alone.
- **Corrosion-protection cover** (4.10.3): standard formwork + compaction
  (4.10.3.2), repetitive/intense-compaction rigid formwork (4.10.3.3), and
  self-compacting concrete (4.10.3.4) each get their own required-cover table
  by exposure class and `f'c` (Tables 4.10.3.2/4.10.3.3 —
  own-words: required cover increases with exposure severity and decreases
  with higher `f'c`, with a documented concession for higher-strength
  concrete used at a class boundary).

![[as3600-table-4.10.3.2-cover-standard-formwork-compaction.png]]
*Table 4.10.3.2 — required cover where standard formwork and compaction are
used, by exposure classification and `f'c` (AS 3600:2018).*

![[as3600-table-4.10.3.3-cover-intense-compaction.png]]
*Table 4.10.3.3 — required cover where repetitive procedures and intense
compaction, or self-compacting concrete, are used in rigid formwork
(AS 3600:2018).*

  Cast-against-ground surfaces
  (4.10.3.5) add a fixed increment to the standard-formwork cover, larger if
  there's no damp-proof membrane. Spun/rolled members (4.10.3.6) use
  whatever cover the relevant product Standard specifies for an equivalent
  exposure class. Non-corrosion-resistant embedded items (4.10.3.7) need the
  same cover as reinforcement; aluminium must never be embedded unless
  effectively isolated from concrete and from steel (galvanic risk).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-fire-resistance-design]] — cover can be governed by fire
  resistance instead of durability; Section 4 cover is a floor, not a
  ceiling, when Section 5 demands more.
- [[concrete-documentation-requirements]] — exposure classification and cover
  are both required drawing/spec items (Cl 1.4).
- [[concrete-properties-of-concrete]] — `f'c` grade selection this section
  drives.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clauses 4.1–4.10 (Tables
  4.3, 4.4, 4.6, 4.8.1, 4.8.2, 4.10.3.2, 4.10.3.3 reproduced as image assets
  above).
