---
title: Intermediate moment-resisting frame (IMRF) earthquake detailing
category: 2-concrete
tags: [earthquake, seismic, imrf, ductile-detailing, beams, columns]
standards: [AS 3600:2018 Cl 14.5]
status: draft
reviewed: 2026-09-16
---

# Intermediate moment-resisting frame (IMRF) detailing

> Scope: AS 3600 Cl 14.5 — the moderate-ductility (`μ = 3`) detailing
> requirements for IMRF beams, slabs, columns and column joints.

## Summary

`[code]` Reinforced/prestressed IMRFs are moderately ductile only if, beyond
the Standard's normal detailing, they also satisfy Cl 14.5.2–14.5.6, using
Ductility Class N steel or tendons only as flexural reinforcement (Cl
14.5.1). SFRC members need a tensile reinforcement ratio ≥0.006. In
prestressed members, tensile steel quantity must give a flexural strength
`> 1.1(Muo)min` at every section. Non-flexural elements may be incorporated
provided their action/failure doesn't impair the frame's lateral/vertical
capacity.

## Detail

### Beams — longitudinal reinforcement (Cl 14.5.2.1)

`[code]` Top and bottom faces continuously reinforced. Reinforcement/tendon
area per span such that: positive-moment strength at a support face ≥1/3 of
the negative-moment strength at that face; neither positive nor negative
moment strength anywhere along the span is less than 1/5 of the maximum
moment strength at either support face. Longitudinal reinforcement is
continuous through intermediate supports; at external columns it extends to
the far face of the confined region, anchored to develop `fsy` at the span
face. Lapped splices in a tension/reversing-stress region are confined by
≥2 closed ties at each splice.

### Beams — shear reinforcement (Cl 14.5.2.2)

`[code]` Design shear force = the **lesser** of (i) shear from reverse-
curvature bending at `φ = 1.0` nominal moment strengths at each restrained
end plus factored-gravity-load shear (Figure 14.5.2.2), or (ii) the maximum
shear from load combinations including earthquake action `E` taken at
**twice** the AS 1170.4 value. Shear reinforcement: perpendicular to the
longitudinal bars, full member length, ≥2 legs, max spacing `0.5D`;
`Asv ≥ 0.5 bv s/fsy.f`. Over ≥`2D` from a support face, closed ties (first
tie 50 mm from the face) at centres ≤ the least of `0.25d0`, `8db`, `24df`,
300 mm (`db` = smallest enclosed longitudinal bar, `df` = tie bar diameter).

![[as3600-fig-14.5.2.2-shear-gravity-reverse-curvature.png]]
*Figure 14.5.2.2 — shear from gravity loads and reverse-curvature bending:
`Wu = 1.0G + φcQ`; `Vu = (Mnl + Mnr)/ℓn + Wuℓn/2` (AS 3600:2018).*

### Slabs (Cl 14.5.3)

`[code]` Slabs follow the Cl 14.5.2.1(a)–(c) beam rules; two-way flat slabs
in a moment-resisting frame also conform with Cl 14.5.3.2: column-strip top
and bottom faces continuously reinforced both directions; support-transfer
moment reinforcement confined to the column strip (Cl 6.1.4.1); a proportion
`≥ max(1/{1 + (2/3)√[(bl+do)/(bt+do)]}, 0.5)` of that reinforcement
distributed within 1.5× the slab/drop-panel thickness beyond the column/
capital face (`bl`, `bt` = column/capital/bracket size parallel/transverse
to the span, `do` = effective depth);
column-strip negative-moment strength anywhere along the span ≥1/4 of the
maximum at either support face, with ≥1/4 of the support top steel
continuous through the span; positive-moment strength anywhere in the
column strip ≥1/3 of the maximum negative strength at either support, and
≥1/2 of the maximum span positive strength; at discontinuous edges, all
support top/bottom reinforcement must be able to develop `fsy` at the
support face.

### Columns and column joints (Cl 14.5.4–14.5.5)

`[code]` At each end of a column's clear height, longitudinal reinforcement
is restrained by closed fitments over the greater of the column's maximum
cross-section dimension or 1/6 of the least clear height to an adjacent
flexural member. Fitment spacing ≤ the smallest of: `8db` (smallest enclosed
bar); `24√(fsy.f/500)` × fitment-bar diameter; half the smallest column
cross-section dimension; 300 mm — plus the Cl 10.7.3/10.7.4 and Cl
14.5.2.2(b)–(d) shear limits. First fitment at half this spacing from the
support face. Fitment area satisfies column shear demand, not less than Cl
10.7.3/10.7.4. Where `N* > φ·0.3 Ag f'c` or `f'c > 65 MPa`, every
longitudinal bar must be individually restrained by a closed fitment.

`[code]` Column joints (Cl 14.5.5): confined by closed ties through the full
joint depth, spacing per Cl 14.5.4 — halved where slabs/beams exist on all
four sides, over the depth of the shallowest one.

### Robustness — strong column/weak beam (Cl 14.5.6)

`[code]` Where a moment-resisting frame is relied on for lateral support, the
sum of nominal column flexural strengths at a joint (with earthquake-action
axial loads, evaluated at joint faces) must exceed `1.2×` the sum of nominal
beam flexural strengths at the same joint (`ΣMnc ≥ 6/5 ΣMnb`). Columns that
cannot meet this are excluded from the lateral system but must still be
designed for drift-induced moments from frame action.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-earthquake-design-basis]] — Cl 14.1–14.4, applicability and the
  `μ`/`Sp` table this detailing route (`μ = 3`) satisfies.
- [[concrete-earthquake-structural-walls-detailing]] — Cl 14.6–14.7, the
  parallel wall-detailing route, including combined IMRF + wall systems.
- [[concrete-beam-shear-and-torsion-design]], [[concrete-beam-detailing]] —
  Sections 8.2/8.3 baseline shear design/detailing this section tightens.
- [[concrete-column-reinforcement-detailing]] — Cl 10.7, baseline column
  fitment/splicing rules referenced by Cl 14.5.4.
- [[concrete-slab-strength-in-bending]] — Cl 6.1.4.1 column-strip
  definition used by Cl 14.5.3.2.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 14.5 (Figure
  14.5.2.2 reproduced in `wiki/2-concrete/assets/`).
