---
title: General detailing of beams (flexural, shear, torsional reinforcement)
category: 0-standards
tags: [beams, detailing, integrity-reinforcement, curtailment]
standards: [AS 3600:2018 Cl 8.3]
status: draft
reviewed: 2026-09-12
---

# General detailing of beams

> Scope: AS 3600 Cl 8.3 — detailing rules for flexural reinforcement/tendons
> (distribution, integrity reinforcement, curtailment, deemed-to-comply
> arrangements, bundled bars, tendon detailing), and for shear/torsional
> reinforcement (form, spacing, extent, anchorage).

## Summary

`[code]` This clause is where the strength calculations in
[[as3600-beam-strength-in-bending]] and
[[as3600-beam-shear-and-torsion-design]] turn into an actual bar
arrangement — curtailment lengths, minimum continuity for progressive-collapse
resistance, and fitment spacing/anchorage rules.

## Detail

### Distribution and integrity reinforcement (Cl 8.3.1.1)

`[code]` Tensile reinforcement must be well distributed in zones of maximum
concrete tension, including flange portions of T-/L-/I-beams over a support.
For in-situ beams other than perimeter beams, minimum **integrity
reinforcement** through supports: at a continuous support, at least one
Ductility Class N bottom bar (≥20 mm diameter) continuous or spliced by
tension lap/mechanical/welded splice (Cl 13.2); at a non-continuous support,
at least one equivalent bar anchored to develop `fsy` at the support face
(standard hook Cl 13.1.2.7, or headed bar Cl 13.1.4). Perimeter beams need
continuous reinforcement along the full span and over continuous supports:
at least one-sixth of the negative-moment support reinforcement (min. 2
bars) and at least one-quarter of the positive-moment midspan reinforcement
(min. 2 bars), enclosed by closed fitments anchored around a corner
longitudinal bar. Splices: top steel near midspan, bottom steel near
supports.

### Curtailment (Cl 8.3.1.2)

`[code]` At least one-third of negative-moment support reinforcement extends
a distance `D` past the point of contraflexure. At least half the
midspan positive-moment reinforcement extends past the support face by
`12dᵦ` plus a cog (or equivalent anchorage); alternatively at least a third
extends by `8dᵦ + D/2`. At a continuous/restrained support, at least a
quarter of the midspan positive-moment reinforcement continues past the near
face of the support.

### Shear strength at terminated reinforcement (Cl 8.3.1.4)

`[code]` Terminating tensile reinforcement affects local shear strength —
assess via strut-and-tie principles, or deem satisfied if: no more than a
quarter of the max tensile reinforcement terminates within any `2D`; **or**
`φVu ≥ 1.5×(V* − ψp·Pv)` at the cut-off; **or** minimum shear reinforcement
(`Asv ≥ Asv.min`) is provided for a distance `D` along the terminated bar from
the cut-off — see [[as3600-beam-shear-and-torsion-design]] for `Asv.min`.

### Deemed-to-comply arrangement (Cl 8.3.1.5)

`[practice]` For continuous reinforced beams designed by the Cl 6.10
simplified method (see [[as3600-simplified-flexural-analysis]]), a
prescribed bar-extension pattern satisfies Cl 8.3.1.2–8.3.1.4 without
individual checks: negative-moment support steel split into thirds/quarters
extending the whole span / 0.3Ln / 0.2Ln respectively past the support face
(unequal adjacent spans use the longer span for the extension length);
positive-moment midspan steel split into halves/quarters/remainder extending
into simple supports (`12dᵦ` + cog), continuous/restrained supports, or to
within `0.1Ln` of the support face; and the same quarter-in-`2D` termination
limit as Cl 8.3.1.4.

### Compression reinforcement restraint, bundled bars, tendon detailing (Cl 8.3.1.6–8.3.1.8)

`[code]` Compressive reinforcement needed for strength must be restrained by
fitments per Cl 10.7.4 (see [[as3600-column-reinforcement-detailing]]).
Bundled bars: max 4 per bundle, tied in contact, enclosed by fitments,
individual-bar termination points staggered ≥40× the largest bar diameter in
the bundle within the span; treated as a single equivalent-area bar for
design. Tendon detailing: anchorage/stress development per Cl 12.5 and
Section 13; at a pretensioned member's simple support, at least a third of
the tendons at the maximum-positive-moment section continue undebonded to
the member end; horizontally curved tendons need a bursting/splitting
capacity assessment.

### Shear and torsional reinforcement detailing (Cl 8.3.2–8.3.3)

`[code]` Shear reinforcement forms: fitments at 45°–90° to the longitudinal
bars, welded wire mesh, or (circular/oval members) helices — straight bars/
tendons permitted if fully anchored top and bottom; crack widths need
checking where fitment stress at ULS exceeds 500 MPa. **Spacing**:
longitudinal spacing capped at the lesser of `0.5D`/300 mm, relaxed to the
lesser of `0.75D`/500 mm where `V* ≤ φVu.min`; transverse spacing capped at
the lesser of 600 mm/`D`. **Extent**: shear reinforcement required at a
section is carried to the support face and continued for a further distance
`D` in the direction of decreasing shear; first fitment within 50 mm of the
support face; reinforcement extends as close to both compression and tension
faces as cover/congestion permit. **Anchorage**: hook/cog per Cl 13.1.2.7,
welding to a longitudinal bar, or lapped splice (lap length per Cl 13.1.2,
×1.3 for fitments adjacent to cover concrete) — deemed satisfied if bends
enclose a longitudinal bar of adequate diameter in contact with the bend,
spacing complies with Cl 8.3.2.2, and cogs are avoided both in the outer
reinforcement layer and within 50 mm of any concrete surface. Mesh shear
reinforcement: end-anchored per Cl 8.3.2.4 or by embedding ≥2 transverse
wires ≥25 mm into the compression zone.

`[code]` **Torsional reinforcement** (Cl 8.3.3): closed fitments (continuous
around all sides, spacing capped at the lesser of `0.12uh`/300 mm, or lapped
per Cl 13.1.2 ×1.3 near cover concrete; large members may use full-depth/
-width bars with hooked/cogged anchorage instead of a single closed loop)
plus longitudinal reinforcement placed as close as practicable to each
corner (at least one bar per corner), able to distribute torsional tension
equally to the corners of the torsion cell.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-beam-strength-in-bending]], [[as3600-beam-shear-and-torsion-design]]
  — the strength checks this detailing implements.
- [[as3600-simplified-flexural-analysis]] — Cl 6.10 method the
  deemed-to-comply arrangement pairs with.
- [[as3600-column-reinforcement-detailing]] — Cl 10.7.4 restraint rules
  reused for beam compression steel.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clause 8.3.
