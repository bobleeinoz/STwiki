---
title: Beam vibration, T-/L-beam flange width, and slenderness limits
category: 2-concrete
tags: [beams, vibration, t-beams, l-beams, slenderness]
standards: [AS 3600:2018 Cl 8.7-8.9]
status: draft
reviewed: 2026-09-12
---

# Beam vibration, T-/L-beam flange width, and slenderness limits

> Scope: three short, largely independent beam clauses grouped on one page —
> vibration serviceability (Cl 8.7), effective flange width for T-/L-beams
> (Cl 8.8), and lateral slenderness limits (Cl 8.9).

## Summary

`[code]` None of these three clauses is large enough to warrant its own page,
but each is a distinct concept: vibration is a serviceability check with no
prescribed method; flange width is a section-property definition feeding
every other beam clause; slenderness is a lateral-torsional-buckling
detailing limit, not a strength calculation.

## Detail

### Vibration of beams (Cl 8.7)

`[code]` Vibration from machinery, vehicular or pedestrian traffic must be
considered and mitigated where it would adversely affect serviceability — no
calculation method is prescribed, unlike deflection or crack control.

### T-beams and L-beams (Cl 8.8)

`[code]` Where a slab forms the flange, flange-web longitudinal shear
capacity is checked per Cl 8.4 (see
[[concrete-beam-longitudinal-shear-composite]]); isolated T-/L-beams also
need the flange's own shear strength checked per Cl 8.2 on vertical sections
parallel to the beam. **Effective flange width** `bef`, absent a more
accurate determination: `bef = bw + 0.2a` (T-beams) or `bw + 0.1a` (L-beams),
where `a` is the distance between points of zero bending moment (taken as
`0.7L` for continuous beams). The overhanging flange considered effective is
capped at half the clear distance to the next member, and `bef` may be taken
as constant over the whole span once determined this way.

### Slenderness limits (Cl 8.9)

`[code]` **Simply supported/continuous beams**: distance between lateral
restraints `Ll` limited by `Ll/bef ≤` the lesser of `180·bef/D` and 60.
**Cantilevers** (restrained only at the support): clear projection `Ln`
limited by `Ln/bef ≤` the lesser of `100·bef/D` and 25. **Slender prestressed
beams** exceeding either ratio's threshold (`Ll/bef > 30`, or `Ln/bef > 12`
for a cantilever) need additional reinforcement: stirrups providing
`Asv.min` per Cl 8.2.1.7, plus corner longitudinal bars at the compression
face sized against a fraction of the tendon breaking-load capacity
(`Asc ≥ 0.35·Apt·fpb/fsy`) — own-words: this is a lateral-buckling safeguard
for long, slender prestressed members, distinct from the ordinary shear/
flexure reinforcement already provided.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-beam-longitudinal-shear-composite]] — Cl 8.4, referenced by the
  T-/L-beam flange-web shear check.
- [[concrete-beam-shear-and-torsion-design]] — Cl 8.2, referenced by both the
  isolated-flange shear check and the slenderness stirrup requirement.
- [[concrete-properties-of-tendons-and-prestress-losses]] — `fpb` used in the
  slender prestressed beam reinforcement formula.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clauses 8.7–8.9.
