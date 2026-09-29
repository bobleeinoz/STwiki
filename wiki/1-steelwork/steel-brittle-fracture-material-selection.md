---
title: Brittle fracture — material selection by service temperature
category: 1-steelwork
tags: [brittle-fracture, notch-ductile, LODMAT, design-service-temperature, steel-type, charpy, fracture-mechanics]
standards: [AS 4100:2020 Section 10]
status: draft
reviewed: 2026-09-13
---

# Brittle fracture — material selection by service temperature

> Scope: AS 4100:2020 Section 10 — selecting steel grade/thickness against
> brittle fracture: the notch-ductile range method (design service
> temperature, LODMAT map, Table 10.4.1 permissible service temperature,
> Table 10.4.4 steel type ↔ grade, strain and post-weld heat-treatment
> modifications, non-conforming conditions), and the fracture-mechanics
> alternative.

## Summary

`[code]` Two methods (Cl 10.1): (a) **notch-ductile range** — select a
steel type/thickness whose Table 10.4.1 permissible service temperature is
**colder than** the design service temperature (Cl 10.2); or (b) a
**fracture assessment** by fracture mechanics (Cl 10.5).

`[code]` Design service temperature = lowest one-day mean ambient
temperature (LODMAT) for the site (Figure 10.3.2), possibly lowered further
for locally cold sites or artificially cooled parts (Cl 10.3).

## Detail

### Design service temperature (Cl 10.3)

`[code]` General (10.3.1): estimated lowest metal temperature in service,
erection or testing = the basic design temperature (10.3.2), as modified
by 10.3.3.

`[code]` Basic design temperature (10.3.2): the **LODMAT** isotherm value
for the site (Figure 10.3.2), except: (a) structures potentially subject to
especially low local ambient temperatures — basic temperature = LODMAT
**− 5 °C**; (b) critical structures at sites with Bureau of Meteorology
records of abnormally low local temperatures — use that lowered
temperature directly. (Metal temperatures colder than LODMAT can occur with
minimum insulation/heat capacity, radiation shielding, or frost
conditions.)

![[as4100-fig-10.3.2-lodmat-isotherms.png]]
*Figure 10.3.2 — LODMAT (lowest one-day mean ambient temperature) isotherms for Australia, °C, based on 1957–1971 Bureau of Meteorology records (AS 4100:2020).*

`[derived]` Reading the map for common mining/material-handling regions:
Pilbara / NW WA ≈ 10–15 °C; central Australia (Alice Springs area) ≈ 0–5 °C;
Bowen Basin / central QLD coal region ≈ 5–10 °C; southern NSW/VIC tablelands
and Tasmania can be 0 °C or colder (e.g. Canberra/Orange/Armidale area
≈ 0 °C, Tasmania ≈ 3–5 °C). Always confirm against the figure and the
project-specific BoM data for isolated or elevated sites rather than
reading the isotherm alone — Cl 10.3.2(a)/(b) exist precisely because
isotherms are regional averages.

`[code]` Modifications to the basic design temperature (10.3.3): parts
subject to **artificial cooling** below the basic design service
temperature (e.g. refrigerated buildings, cold storage) — design service
temperature = the minimum expected temperature for that part.

### Material selection (Cl 10.4)

`[code]` Selection of steel type (10.4.1): pick from Table 10.4.1 by
material thickness so the table's **permissible service temperature is
less (colder) than** the Cl 10.3 design service temperature, subject to
Cl 10.4.2/10.4.3.

`[code]` Table 10.4.1 — permissible service temperature (°C) by steel type
and thickness (selected rows; full table in the image):

| Steel type | ≤6mm | >6–12 | >12–20 | >20–32 | >32–70 | >70 |
|---|---|---|---|---|---|---|
| 1 | −20 | −10 | 0 | 0 | 0 | 5 |
| 2 | −30 | −20 | −10 | −10 | 0 | 0 |
| 2S | 0 | 0 | 0 | 0 | 0 | 0 |
| 3 | −40 | −30 | −20 | −15 | −15 | 10 |
| 4 | −10 | 0 | 0 | 0 | 0 | 5 |
| 5 | −30 | −20 | −10 | 0 | 0 | 0 |
| 5S | 0 | 0 | 0 | 0 | 0 | 0 |
| 6 | −40 | −30 | −20 | −15 | −15 | −10 |
| 7A | −10 | 0 | 0 | 0 | 0 | — |
| 7B | −30 | −20 | −10 | 0 | 0 | — |
| 7C | −40 | −30 | −20 | −15 | −15 | — |
| 8C | −40 | −30 | — | — | — | — |
| 8Q | −20 | −20 | −20 | −20 | −20 | −20 |
| 9Q | −20 | −20 | −20 | −20 | −20 | −20 |
| 10Q | −20 | −20 | −20 | −20 | −20 | −20 |

![[as4100-table-10.4.1-permissible-service-temperatures.png]]
*Table 10.4.1 — permissible service temperatures according to steel type and thickness (AS 4100:2020).*

For steels with an L20/L40/L50/Y20/Y40 designation, the permissible service
temperature is the **colder** of the table value and the specified impact
test temperature. Table 10.4.1 is based on statistical notch-toughness data
for steel currently made in Australia (per Appendix K); confirmation should
be sought where a different manufacturer's product is used.

`[code]` Limitations (10.4.2): Table 10.4.1 applies **without
modification** only to members/components fabricated and erected per
Sections 14–15 and AS/NZS 5131, welded per AS/NZS 1554.1 or 1554.4, and
**not** subject to more than **1.0 % outer bend fibre strain** during
fabrication (e.g. cold-formed/cold-bent details). Greater strain needs
Cl 10.4.3.

`[code]` Modification for certain applications (10.4.3):
- **1.0–10.0 % strain** (10.4.3.1): raise the Table 10.4.1 permissible
  temperature by **≥ 20 °C** (local strain from weld distortion is
  disregarded).
- **≥ 10.0 % strain** (10.4.3.2): raise it by ≥ 20 °C **plus 1 °C for every
  1.0 % of strain above 10.0 %**.
- **Post-weld heat treatment** (10.4.3.3): PWHT between 500 °C and 620 °C
  does **not** require modification of Table 10.4.1 (guidance: AS 4458).
- **Non-conforming conditions** (10.4.3.4): where the permissible service
  temperature is unknown, or is warmer than the design service temperature,
  the steel must not be used **unless** all of: (a) a mock-up of the joint/
  member is fabricated from the actual grade with similar dimensions and
  strain; (b) three Charpy specimens are taken from the area of maximum
  strain and tested at the design service temperature; (c) impact
  properties meet the minimum specified for that grade; (d) where the
  product Standard specifies no minimum, average absorbed energy for three
  10×10 mm specimens ≥ 27 J, none below 20 J; (e) where plate thickness
  prevents a 10×10 mm specimen, use the nearest standard test thickness
  with proportionally reduced energy requirements.

### Steel type ↔ grade cross-reference (Cl 10.4.4, Table 10.4.4)

`[code]` Table 10.4.4 maps each notional "steel type" (1, 2, 2S, 3, 4, 5,
5S, 6, 7A, 7B, 7C, 8C, 8Q, 9Q, 10Q) to the specific product grades under
AS/NZS 1163, AS/NZS 1594, AS/NZS 3678/3679.2, AS/NZS 3679.1 and AS 3597
that qualify as that type. Selected examples:

| Steel type | AS/NZS 1163 | AS/NZS 1594 | AS/NZS 3678 / 3679.2 | AS/NZS 3679.1 | AS 3597 |
|---|---|---|---|---|---|
| 1 | C250 | HA200/250/300, HU250/300 | 200, 250, 300 | 300 | — |
| 4 | C350 | HA350, HA400, WR350 | 350, WR350, 400 | 350 | — |
| 7A | C450 | — | 450 | — | — |
| 8Q | — | — | — | — | 500 |
| 9Q | — | — | — | — | 600 |
| 10Q | — | — | — | — | 700 |

Types 8Q/9Q/10Q are quenched-and-tempered steels (formerly "steel types
8/9/10" in AS/NZS 1554.4).

![[as4100-table-10.4.4-steel-type-to-grade-part1.png]]
![[as4100-table-10.4.4-steel-type-to-grade.png]]
*Table 10.4.4 — steel type relationship to steel grade (AS 4100:2020), full table in two parts.*

`[derived]` Types 2, 2S, 3, 5, 5S, 6, 7B, 7C are the impact-tested /
low-temperature sub-grades (L0, L15, L20, L40, Y20, Y40, S0 suffixes) of the
base grades in types 1, 4, 7A — i.e. selecting a colder Table 10.4.1
permissible temperature usually means specifying an impact-tested variant
of the same nominal grade (e.g. Grade 300L15 instead of plain Grade 300),
not a different `f_y`.

### Fracture assessment (Cl 10.5)

`[code]` Alternative to Cl 10.2: a fracture-mechanics analysis combined
with fracture-toughness measurements of the selected steel, weld metal and
heat-affected zones, and NDE of welds and HAZs. See BS 7910 and WTIA
Technical Note 10 for methods.

## Worked reference

`[derived]` A gantry in the Pilbara (LODMAT ≈ 10–15 °C on the map, no
special local-cold-spot or refrigeration factors) has a very mild design
service temperature by Australian standards — ordinary Grade 300/350 plate
(Type 1/4) up to significant thickness satisfies Table 10.4.1 with margin.
A structure in the NSW/ACT tablelands or Tasmania (LODMAT near or below
0 °C) is far more likely to need an impact-tested (Ln/Yn suffix) grade,
especially in thicker material — check the actual site LODMAT and the
thickness band, not just the region name.

## Contradictions

None recorded.

## Related

- [[as-4100-2020-steel-structures]] — standard register.
- [[steel-materials-and-design-strengths]] — base product grades and
  design strengths (Table 2.1); Z-quality / lamellar tearing (a related but
  distinct through-thickness durability requirement, not brittle fracture).
- [[steel-limit-state-design-basis]] — Cl 3.7 routing to this Section.
- [[steel-fatigue-design]] — Section 11, a related but separate mode of
  failure that can compound with low-temperature notch sensitivity.
- [[steel-brittle-fracture-statistical-data]] — Appendix K test regime for
  qualifying a product not already covered by Table 10.4.1.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Section 10
  (pp. 139–144). Figure 10.3.2, Tables 10.4.1 and 10.4.4 reproduced in
  `wiki/1-steelwork/assets/`.
