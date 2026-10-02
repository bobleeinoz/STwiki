---
title: Non-linear analysis methods for concrete structures
category: 2-concrete
tags: [structural-analysis, nonlinear-analysis]
standards: [AS 3600:2018 Cl 6.5, AS 3600:2018 Cl 6.6]
status: draft
reviewed: 2026-09-12
---

# Non-linear analysis methods for concrete structures

> Scope: non-linear frame analysis (Cl 6.5) and non-linear stress analysis
> (Cl 6.6), the two methods that feed the system-strength-factor strength
> checks in [[concrete-strength-check-procedures]] (Cl 2.2.5/2.2.6).

## Summary

`[code]` Both methods apply at service load, overload and collapse
(Cl 6.5.1/6.6.1), must satisfy the general analysis basis (Cl 6.1.1) and
results-interpretation requirement (Cl 6.1.2), and — for frame analysis
specifically — the design-strip definitions of Cl 6.1.4. Both require mean
(not characteristic) material properties, and both require a sensitivity
check on input data and modelling parameters, mirroring Cl 6.4.3.

## Detail

### Non-linear frame analysis (Cl 6.5)

`[code]` Must capture (6.5.2): non-linear stress-strain behaviour of
reinforcement, tendons and concrete; concrete cracking; tension stiffening
between adjacent cracks; creep and shrinkage; and tendon relaxation.
Geometric non-linearity (6.5.3): equilibrium must be considered in the
*deformed* configuration whenever joint displacement or member lateral
deflection changes action effects or overall behaviour by more than 10%.
Material values (6.5.4): mean values throughout (strength, initial elastic
moduli, yield stress/strain) — see [[concrete-properties-of-concrete]]
Cl 3.5. Additional analysis runs with other property values should be
considered to capture variability and non-proportionality effects.
Sensitivity check per 6.5.5.

### Non-linear stress analysis (Cl 6.6)

`[code]` Same numerical-methods framing as Cl 6.4 but non-linear (6.6.1–6.6.2).
Must capture the same list as frame analysis (6.6.3): material non-linearity,
cracking, tension stiffening, creep/shrinkage, tendon relaxation, **plus**
geometric non-linear effects explicitly folded into the same clause (unlike
Cl 6.5 which separates 6.5.2/6.5.3). Mean material values per 6.6.4,
sensitivity check per 6.6.5.

`[derived]` The practical difference between the two: frame analysis works
at the member/line-element level (suits the Cl 2.2.5 system-factor strength
check for framed structures), stress analysis works at the continuum/FE
level (suits Cl 2.2.6 for components or structures better modelled as
continua, e.g. deep beams, D-regions, walls with openings).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-strength-check-procedures]] — Cl 2.2.5/2.2.6 system-factor
  checks these methods feed.
- [[concrete-properties-of-concrete]] — Cl 3.5 mean-property requirement.
- [[concrete-elastic-analysis-methods]] — the linear counterparts.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clauses 6.5, 6.6.
