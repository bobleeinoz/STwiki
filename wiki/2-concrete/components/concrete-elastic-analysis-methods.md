---
title: Elastic analysis methods for concrete structures
category: 2-concrete
tags: [structural-analysis, elastic-analysis, stiffness, moment-redistribution]
standards: [AS 3600:2018 Cl 6.2, AS 3600:2018 Cl 6.3, AS 3600:2018 Cl 6.4]
status: draft
reviewed: 2026-09-12
---

# Elastic analysis methods for concrete structures

> Scope: linear elastic frame analysis (Cl 6.2), elastic analysis with
> secondary bending moments in sway frames (Cl 6.3), and linear elastic
> stress analysis (Cl 6.4).

## Summary

`[code]` These three clauses share one analysis philosophy — linear
elasticity — applied at three different scales: ordinary indeterminate
frame analysis, sway-frame analysis with second-order effects, and
continuum/FE stress analysis. All three feed the corresponding strength check
procedure in [[concrete-strength-check-procedures]] (Cl 2.2.2 and Cl 2.2.3).

## Detail

### Linear elastic frame analysis (Cl 6.2)

`[code]` Applies to indeterminate continuous beams/frames where secondary
geometric effects are insignificant (Cl 6.2.1).

- **Span length** (6.2.2): centre-to-centre of supports.
- **Critical section for negative moment** (6.2.3): by analysis, or at
  `0.7 × asup` from the support centreline as a default.
- **Stiffness** (6.2.4): member stiffness must represent the limit state
  being analysed, be applied consistently, and generate the worst-case
  action for the failure mode under design — not necessarily the "best
  estimate" stiffness. Haunching/section variation along a member must be
  accounted for if significant. Absent refined analysis, moment of inertia
  for lateral-system checks (drift, vibration period, action distribution)
  is either the full uncracked gross section, or a cracked-section value from
  Table 6.2.4 — own-words: beams/slabs get one fixed
  fraction of gross `I`; columns and walls get a fraction that varies with
  axial load ratio `N*/(Ag·f'c)`, interpolated linearly between stated
  points.

![[as3600-table-6.2.4-effective-section-properties.png]]
*Table 6.2.4 — effective section properties `Ieff` as a proportion of `Ig`,
by member type and axial load ratio (AS 3600:2018).*

  A section is assumed cracked unless combined flexure+axial
  tensile stress stays below the mean characteristic flexural tensile
  strength (Cl 3.1.1.3).
- **Deflections** (6.2.5): must account for cracking, tension stiffening,
  shrinkage, creep and tendon relaxation — satisfied by following Cl 8.5
  (beams) / Cl 9.3 (slabs), not yet ingested. Formwork deflection/prop
  settlement during construction must also be considered.
- **Secondary bending from prestress** (6.2.6): indeterminate-structure
  secondary moments/shears from prestressing must be included in
  serviceability design (may be found by elastic analysis of the unloaded
  uncracked structure), and in strength design with a load factor of 1.0 —
  except the permanent-action-plus-prestress-at-transfer case, which uses the
  Cl 2.5 factors instead (see [[concrete-limit-state-design-basis]]).
- **Moment redistribution** (6.2.7): elastically-determined support moments
  in statically indeterminate members may be redistributed (increased or
  decreased) provided sufficient rotation capacity is demonstrated at
  critical moment regions, accounting for actual reinforcement/tendon
  stress-strain behaviour to fracture strain, static equilibrium after
  redistribution, and concrete properties. A **deemed-to-comply** route
  (6.2.7.2) avoids a full rotation-capacity analysis provided: all main
  reinforcement is Ductility Class N or E; for SFRC members the tensile
  reinforcement ratio is ≥ 0.004; the pre-redistribution moment diagram is
  elastic; and the redistribution percentage is capped by the neutral-axis
  parameter `ku` in the peak-moment region — full redistribution allowance
  up to `ku ≤ 0.2`, a reducing allowance for `0.2 < ku ≤ 0.4`, and **no**
  redistribution permitted once `ku > 0.4`. Positive moments must be
  adjusted to preserve equilibrium after any redistribution. `[practice]`
  The clause notes extra checks on ductility and punching-shear risk are
  prudent wherever redistribution is used.

### Elastic analysis with secondary bending moments (Cl 6.3)

`[code]` Applies to unbraced frames (no shear walls/bracing, or only partial)
where relative displacement between the ends of compression members is less
than `Lu/250` under the strength design load (Cl 6.3.1). On top of the
Cl 6.2 requirements: lateral joint displacement effects must be included; for
strength design of regular rectangular frames, member stiffness follows
Cl 6.2.4.2; and for very slender members, axial-compression-induced changes
in bending stiffness must be considered.

### Linear elastic stress analysis (Cl 6.4)

`[code]` Covers numerical-methods stress analysis (including finite element
analysis) of structures or parts of structures (Cl 6.4.1), conforming with
the general basis (6.1.1) and results-interpretation (6.1.2) requirements.
Cl 6.4.3 requires a sensitivity check: results must be examined for their
sensitivity to variations in input data and modelling parameters — this is a
recurring requirement across all the numerical-analysis clauses (see also
Cl 6.5.5, 6.6.5, 6.8.2).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-structural-analysis-overview]] — parent page, method menu and
  design-strip definitions.
- [[concrete-strength-check-procedures]] — Cl 2.2.2/2.2.3 strength checks
  these methods feed.
- [[concrete-nonlinear-analysis-methods]] — the non-linear counterparts.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clauses 6.2–6.4 (Table 6.2.4
  reproduced as an image asset above).
