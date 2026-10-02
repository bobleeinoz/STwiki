---
title: Structural steel materials and design strengths
category: 1-steelwork
tags: [materials, yield-stress, tensile-strength, steel-grades, fasteners, lamellar-tearing]
standards: [AS 4100:2020 Section 2, AS 4100:2020 Cl 3.8, AS 4100:2020 App M]
status: draft
reviewed: 2026-09-13
---

# Structural steel materials and design strengths

> Scope: AS 4100:2020 Section 2 — design yield stress and tensile strength by
> product standard, grade and thickness (Table 2.1); elastic constants;
> unidentified steel; through-thickness (Z-quality) properties and lamellar
> tearing (Cl 2.2.5, 3.8, App M); fastener, weld, stud and anchor material
> standards.

## Summary

`[code]` The yield stress `f_y` and tensile strength `f_u` used in design
must not exceed the values in Table 2.1 for the product standard, grade and
thickness of the element (Cl 2.1.1, 2.1.2). `f_y` reduces with thickness for
plate and section grades — the tabulated value, not the grade name, is the
design value.

`[code]` Elastic constants for all grades (Cl 2.2.4): `E = 200 × 10³ MPa`,
`G = 80 × 10³ MPa`, `ν = 0.25`, `α_T = 11.7 × 10⁻⁶ /°C`.

`[code]` Unidentified steel (Cl 2.2.3): unless fully tested to AS 1391, design
with `f_y ≤ 170 MPa` and `f_u ≤ 300 MPa`, and only where surface condition
and weldability do not compromise the structure.

## Detail

### Cross-check against ASI Design Capacity Tables Vol 1 (1999, AS 4100-1998 vintage)

`[practice]` The AISC/ASI *Design Capacity Tables for Structural Steel,
Vol 1: Open Sections* (DCT/V1/03-1999) Table T2.1 tabulates the same
yield stress / tensile strength values for AS/NZS 3679.1 hot-rolled
sections used in this page's table (t < 11: 320/440; 11 ≤ t ≤ 17: 300/440;
t > 17: 280/440 MPa) — no discrepancy found against the current AS 4100:2020
Table 2.1 values above for the sections sampled. See
[[asi-design-capacity-tables-vol1-open-sections]] for the source register
and vintage caveat (this DCT predates AS 4100:2020 and is not re-verified
clause-by-clause against it).

![[dct-table-t2.1-yield-stress-tensile-strength.png]]
*DCT Vol 1 Table T2.1 — yield stress and tensile strength by steel standard,
form, grade and thickness (source: DCT/V1/03-1999, p. 2-3).*

### Table 2.1 — design strengths by product, grade and thickness

`[code]` Values below are transcribed from Table 2.1 (AS 4100:2020). `t` is
thickness of material in mm; `f_y`, `f_u` in MPa. Welded I-sections to
AS/NZS 3679.2 are made from AS/NZS 3678 plate, so use the AS/NZS 3678 rows
for them. Impact-tested sub-grades (e.g. L0, L15, Y20) share the strengths
of their parent grade.

**AS/NZS 1163 — cold-formed hollow sections**

| Grade | t | f_y | f_u |
|---|---|---|---|
| C450 | all | 450 | 500 |
| C350 | all | 350 | 430 |
| C250 | all | 250 | 320 |

**AS/NZS 1594 — hot-rolled plate, strip, sheet floorplate**

| Grade | t | f_y | f_u |
|---|---|---|---|
| HA400 | all | 380 | 460 |
| HW350 | all | 340 | 450 |
| HA350 | all | 350 | 430 |
| HA300/1, HU300/1 | all | 300 | 430 |
| HA300, HU300 | all | 300 | 400 |
| HA250, HU250 | all | 250 | 350 |
| HA200 | all | 200 | 300 |
| XF500 (plate and strip) | ≤ 8 | 480 | 570 |
| XF400 (plate and strip) | ≤ 8 | 380 | 460 |
| XF300 (plate and strip) | all | 300 | 440 |

**AS/NZS 3678 — hot-rolled plate and floorplate** (also governs AS/NZS 3679.2 welded I-sections)

| Grade | t (mm) | f_y | f_u |
|---|---|---|---|
| 450 | ≤ 20 | 450 | 520 |
| 450 | 20 < t ≤ 32 | 420 | 500 |
| 450 | 32 < t ≤ 50 | 400 | 500 |
| 400 | ≤ 12 | 400 | 480 |
| 400 | 12 < t ≤ 20 | 380 | 480 |
| 400 | 20 < t ≤ 80 | 360 | 480 |
| 350 | ≤ 12 | 360 | 450 |
| 350 | 12 < t ≤ 20 | 350 | 450 |
| 350 | 20 < t ≤ 80 | 340 | 450 |
| 350 | 80 < t ≤ 150 | 330 | 450 |
| WR350 | ≤ 50 | 340 | 450 |
| 300 | ≤ 8 | 320 | 430 |
| 300 | 8 < t ≤ 12 | 310 | 430 |
| 300 | 12 < t ≤ 20 | 300 | 430 |
| 300 | 20 < t ≤ 50 | 280 | 430 |
| 300 | 50 < t ≤ 80 | 270 | 430 |
| 300 | 80 < t ≤ 150 | 260 | 430 |
| 250 | ≤ 8 | 280 | 410 |
| 250 | 8 < t ≤ 12 | 260 | 410 |
| 250 | 12 < t ≤ 50 | 250 | 410 |
| 250 | 50 < t ≤ 80 | 240 | 410 |
| 250 | 80 < t ≤ 150 | 230 | 410 |
| 200 | ≤ 12 | 200 | 300 |

**AS/NZS 3679.1 — hot-rolled bars and sections**

| Form | Grade | t (mm) | f_y | f_u |
|---|---|---|---|---|
| Flats and sections | 350 | < 11 | 360 | 480 |
| Flats and sections | 350 | 11 ≤ t < 40 | 340 | 480 |
| Flats and sections | 350 | ≥ 40 | 330 | 480 |
| Flats and sections | 300 | < 11 | 320 | 440 |
| Flats and sections | 300 | 11 ≤ t ≤ 17 | 300 | 440 |
| Flats and sections | 300 | > 17 | 280 | 440 |
| Hexagons, rounds, squares | 350 | ≤ 50 | 340 | 480 |
| Hexagons, rounds, squares | 350 | 50 < t < 100 | 330 | 480 |
| Hexagons, rounds, squares | 350 | ≥ 100 | 320 | 480 |
| Hexagons, rounds, squares | 300 | ≤ 50 | 300 | 440 |
| Hexagons, rounds, squares | 300 | 50 < t < 100 | 290 | 440 |
| Hexagons, rounds, squares | 300 | ≥ 100 | 280 | 440 |

`[derived]` For AS/NZS 3679.1 sections the governing `t` is the flange
thickness for flange-controlled checks; the standard tabulates by "thickness
of material", and common practice is to take the thickest element of the
section (flange) for `f_y` of the whole section, though a web-specific `f_y`
is permissible where the web is thinner. Confirm against Cl 5.2 / 6.2
notation (`f_y` of the element) before relying on the higher web value.

**AS 3597 — quenched and tempered plate**

| Grade | t (mm) | f_y | f_u |
|---|---|---|---|
| 500 | 5 ≤ t ≤ 110 | 500 | 590 |
| 600 | 5 ≤ t ≤ 110 | 600 | 690 |
| 700 | ≤ 5 | 650 | 750 |
| 700 | 5 < t ≤ 65 | 690 | 790 |
| 700 | 65 < t ≤ 110 | 620 | 720 |

`[code]` The AS 4100 scope cap is `f_y ≤ 690 MPa` (Cl 1.1.2(b)), so Grade 700
plate at the 690 MPa band is the upper limit of the Standard.

### Product standards and acceptance (Cl 2.2.1–2.2.2)

`[code]` Structural steel must conform, before fabrication, to AS 3597,
AS/NZS 1163, AS/NZS 1594, AS/NZS 3678, AS/NZS 3679.1 or AS/NZS 3679.2 as
appropriate. Conforming test reports or certificates are sufficient evidence
of conformance.

### Through-thickness properties and lamellar tearing (Cl 2.2.5, 3.8, App M)

`[code]` Where a joint transmits stress normal to the plate surface —
especially where the branch member thickness or required weld size is
≥ 20 mm — design, material selection and detailing must minimise
through-thickness stress intensity, and weld sizes larger than necessary must
not be specified (Cl 3.8). Material suitability is judged on the AS/NZS 3678
through-thickness ductility quality classes (Z-values). The full Appendix M
selection procedure (the `Z_Ed ≤ Z_Rd` check and its five-factor scoring
table) is on [[steel-lamellar-tearing-avoidance]].

`[code]` Table 2.2.5 — minimum reduction in area by grade suffix:

| Grade suffix | Min. reduction in area (%) | Range of Z_Ed |
|---|---|---|
| Z15 | 15 | 11 ≤ Z_Ed ≤ 20 |
| Z25 | 25 | 21 ≤ Z_Ed ≤ 30 |
| Z35 | 35 | > 30 |

`[code]` Z-quality steel is not required where `Z_Ed ≤ 10` or where the steel
thickness is 16 mm or less (Note 2 to Table 2.2.5; Note 1 to Cl 3.8).

### Fasteners, welds, studs, anchors, castings (Cl 2.3, 2.4)

`[code]`
- Bolts, nuts, washers: AS 1110, AS 1111, AS 1112, AS 1237.1, AS/NZS 1252.1
  (high-strength structural), AS/NZS 1559 (galvanized tower bolts — written
  for towers, may not suit all structures). Acceptable bolts and bolting
  categories are in Table 9.2.1 — see [[steel-bolt-design]].
- Test laboratories must meet AS ISO/IEC 17025 where the product standard
  is silent.
- Equivalent high-strength fasteners (Cl 2.3.2) are permitted with evidence
  of equivalence: same chemistry and mechanical properties as AS/NZS 1252.1,
  body diameter and bearing areas not less than the AS/NZS 1252.1 bolt of the
  same nominal size, and a checkable tensioning method achieving at least
  the Table 15.2.2.2 minimum bolt tension.
- Welding: AS/NZS 5131 (Cl 2.3.3). Welded studs: AS/NZS 1554.2, collars to
  ISO 13918 for non-prequalified applications (Cl 2.3.4).
- Explosive fasteners: AS/NZS 1873 (Cl 2.3.5).
- Anchor bolts: bolt standards of Cl 2.3.1, or rod to the Cl 2.2.1 steel
  standards with threads to AS 1275 (Cl 2.3.6).
- Mechanical and chemical anchors: designed and specified to AS 5216
  (Cl 2.3.7).
- Steel castings: AS 2074 (Cl 2.4).

## Worked reference

`[derived]` Example of the thickness effect: a 310UC158 (AS/NZS 3679.1
Grade 300, flange 25 mm) takes `f_y = 280 MPa` (t > 17), whereas a 310UC97
(flange 15.4 mm) takes `f_y = 300 MPa` and a 150UC23 (flange 6.8 mm) takes
`f_y = 320 MPa`. Section tables from the mills already reflect this; check
the table's `f_y` column rather than assuming 300.

## Contradictions

None recorded.

## Related

- [[as-4100-2020-steel-structures]] — standard register.
- [[asi-design-capacity-tables-vol1-open-sections]] — 1999 design-aid
  cross-check of Table 2.1 values (Table T2.1).
- [[asi-dct-vol1-open-section-properties]] — full transcription of Table
  T2.1 (design `f_y`/`f_u` by product standard, grade, thickness) and
  T2.2 (elastic constants).
- [[steel-limit-state-design-basis]] — how `f_y`, `f_u` enter the capacity
  checks; lamellar tearing and brittle fracture pointers (Cl 3.7, 3.8).
- [[steel-brittle-fracture-material-selection]] — steel type / impact grade
  selection by service temperature (Section 10).
- [[steel-lamellar-tearing-avoidance]] — full Appendix M selection
  procedure for Z-quality material against a joint's shrinkage-strain risk.
- [[steel-bolt-design]] — bolting categories (Table 9.2.1).
- [[steel-fabrication-and-erection-requirements]] — minimum bolt tension
  (Table 15.2.2.2), material identification.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Section 2 (pp. 27–31),
  Cl 3.8, Appendix M.
