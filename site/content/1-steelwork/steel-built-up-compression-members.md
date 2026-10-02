---
title: Laced, battened and back-to-back compression members
category: 1-steelwork
tags: [compression, built-up-members, laced, battened, back-to-back, double-angle, tie-plates]
standards: [AS 4100:2020 Cl 6.4, AS 4100:2020 Cl 6.5]
status: draft
reviewed: 2026-09-13
---

# Laced, battened and back-to-back compression members

> Scope: AS 4100:2020 Cl 6.4 (design transverse shear for built-up members,
> laced members, battened members) and Cl 6.5 (two angles / channels / tees
> back to back, separated or in contact). The main-member capacity itself is
> per [[steel-compression-member-capacity]].

## Summary

`[code]` A compression member made of two or more parallel main components
acting as one must have its components and their connections proportioned
for a design transverse shear `V*` applied anywhere along the member in the
most unfavourable direction (Cl 6.4.1, A1):

`V* = π (N_s/N_c − 1) N* / λ_n ≥ 0.01 N*`

with `N_s` (Cl 6.2.1), `N_c` (Cl 6.3.3), `N*` the design axial force and
`λ_n` the modified member slenderness (for battened members from
Cl 6.4.3.2 and 6.3.3).

## Detail

### Laced compression members (Cl 6.4.2)

`[code]`
- Main component slenderness `(l_e/r)_c` (minimum `r`, length between
  lacing points) ≤ lesser of 50 and 0.6 × the whole-member slenderness
  (6.4.2.1).
- Whole-member slenderness assumes integral action but ≥ `1.4(l_e/r)_c`
  (6.4.2.2).
- Lacing angle to the member axis: 50°–70° single lacing; 40°–50° double
  lacing (6.4.2.3).
- Lacing element effective length: distance between inner welds/fasteners
  (single); 0.7 × that for double lacing connected at intersections
  (6.4.2.4). Lacing slenderness ≤ 140 (6.4.2.5).
- Mutually opposed single lacing on opposite faces is not permitted without
  allowing for torsion; double or mutually opposed lacing must not be
  combined with perpendicular members/diaphragms other than tie plates
  unless deformation actions are calculated (6.4.2.6).
- Tie plates (6.4.2.7): at lacing ends, interruptions and connections; end
  tie plate width (along the member) ≥ the perpendicular distance between
  the connection centroids to the main components, intermediate ≥ 3/4 of
  it; designed as battens (Cl 6.4.3); thickness ≥ 0.02 × distance between
  innermost weld/fastener lines unless free edges are stiffened
  (stiffener slenderness < 170).

### Battened compression members (Cl 6.4.3)

`[code]`
- Main component slenderness ≤ lesser of 50 and 0.6 × whole-member
  slenderness per 6.4.3.2 (6.4.3.1).
- About the axis **normal** to the batten plane:
  `(l_e/r)_bn = sqrt[(l_e/r)_m² + (l_e/r)_c²]`, with `(l_e/r)_m` the whole
  member acting integrally and `(l_e/r)_c` the main component maximum.
  About the axis **parallel** to the batten plane: `(l_e/r)_bp ≥ 1.4(l_e/r)_c`
  (6.4.3.2).
- Batten effective length: end batten = perpendicular distance between
  main component centroids; intermediate = 0.7 × that (6.4.3.3). Batten
  slenderness ≤ 180 (6.4.3.4).
- Batten width: end ≥ greater of the centroid distance and 2 × the narrower
  component width; intermediate ≥ greater of half the centroid distance and
  2 × narrower component width (6.4.3.5).
- Batten thickness ≥ 0.02 × minimum distance between innermost weld/
  fastener lines unless free edges stiffened (stiffener slenderness ≤ 170,
  `r` about the axis parallel to the member) (6.4.3.6).
- Loads on battens (6.4.3.7): simultaneously a longitudinal shear
  `V*_l = V* s_b / (n_b d_b)` and a bending moment `M* = V* s_b / (2n_b)`,
  where `s_b` = batten spacing, `n_b` = number of parallel batten planes,
  `d_b` = lateral distance between weld/fastener centroids.

### Back-to-back members (Cl 6.5)

`[code]` **Components separated** (6.5.1) — two angles, channels or tees
separated back to back by no more than the end-gusset thickness, designed as
one member: similar sections arranged symmetrically with rectangular axes
aligned; slenderness about the axis parallel to the connected surfaces per
Cl 6.4.3.2; interconnected by fasteners as a battened member (Cl 6.4.3) with
at least three approximately equal bays and ≥ 2 fasteners per line at each
end (or equivalent welds); interconnection design longitudinal shear per
connection `V*_l = 0.25 V* (l_e/r)_c`, `(l_e/r)_c` = main component
slenderness between interconnections.

`[code]` **Components in contact or with continuous packing** (6.5.2): same
configuration and slenderness rules; connected at intervals into ≥ 3
approximately equal bays with ≥ 2 fasteners per line at the ends (or
equivalent welds); connection design forces per 6.5.1.5.

`[derived]` Practical consequence for double-angle bracing (common in
conveyor gantry and transfer tower bracing): with three bays the component
slenderness between stitch bolts is `l/3` over the angle's minimum `r_v`,
and the "y-y" (parallel to gusset) slenderness of the pair is
`sqrt[(l_e/r_y)² + (l_e/(3 r_v))²]`. Sizing the pair on its integral `r_y`
alone overstates capacity.

## Worked reference

None yet.

## Contradictions

None recorded. **Flag**: the Cl 6.4.1 design transverse shear force `V*`
equation is Amendment-No.-1-amended (the source's "Appendix Former
Wording" gives a former equation of near-identical visible form — the
precise wording delta was not resolved from the source scan); the NCC's
current reference edition of AS 4100:2020 is unamended. Confirm the exact
former-vs-current difference against the source PDF's Appendix Former
Wording before relying on this clause for strict NCC-unamended compliance.
See [[as-4100-2020-steel-structures]] "NCC compliance trap".

## Related

- [[steel-compression-member-capacity]] — `N_s`, `N_c`, `λ_n`, `α_c`.
- [[steel-tension-member-capacity]] — Cl 7.4 built-up tension members
  (same batten/tie-plate and bay rules referenced).
- [[steel-bolt-design]] — stitch bolt design for `V*_l`.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Cl 6.4–6.5 (pp. 93–98).
  The `V*` equation in Cl 6.4.1 carries an A1 amendment tag.
