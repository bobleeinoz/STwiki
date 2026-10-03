---
title: Design properties of concrete (strength, elasticity, shrinkage, creep)
category: 0-standards
tags: [material-properties, concrete, shrinkage, creep]
standards: [AS 3600:2018 Cl 3.1, AS 3600:2018 Cl 3.5]
status: draft
reviewed: 2026-09-12
---

# Design properties of concrete

> Scope: how AS 3600 defines and lets you derive concrete's design strength,
> elastic modulus, density, stress-strain behaviour, thermal expansion,
> shrinkage and creep (Cl 3.1), plus the material-property basis for
> non-linear analysis (Cl 3.5).

## Summary

`[code]` For each property, AS 3600 consistently offers the same three
routes: (a) take a standard/default value, (b) test to the named AS 1012 part,
or (c) use the standard's own predictive model/table. Which route governs
depends on the property — see Detail.

## Detail

### Compressive strength (Cl 3.1.1.1–3.1.1.2)

`[code]` Characteristic cylinder compressive strength at 28 days (`f'c`) is
either the specified strength grade (if cured per the Standard and conforming
to AS 1379) or determined statistically from AS 1012.9 cylinder tests. AS 3600
recognises a set of standard strength grades spanning roughly 20 MPa to
120 MPa — `[derived]` treat any specific grade list as needing confirmation
against Cl 3.1.1.1 rather than assuming a fixed set, since the exact grade
list is given in clause text rather than a numbered table. Grout cube
strength conversion uses Table 3.1.1.1. Mean in-situ strength `f'cmi`, absent
better data, is taken as 90% of mean cylinder strength `f'cm`, or from
Table 3.1.2.

![[as3600-table-3.1.1.1-cylinder-cube-strength-relationship.png]]
*Table 3.1.1.1 — relationship between cylinder and cube strength at 28 days
(AS 3600:2018).*

### Tensile strength (Cl 3.1.1.3)

`[code]` Uniaxial tensile strength: `fct = 0.6·fct.f` or `fct = 0.9·fct.sp`,
where `fct.f` (flexural) comes from AS 1012.11 tests and `fct.sp` (indirect/
splitting) from AS 1012.10 tests. Absent test data, characteristic values
default to `fct.f ≈ 0.6√f'c` and `fct ≈ 0.36√f'c` at 28 days under standard
curing, with mean and upper-characteristic values obtained by multiplying
these by 1.4 and 1.8 respectively (Cl 3.1.1.3).

### Modulus of elasticity (Cl 3.1.2)

`[code]` Mean modulus `Ecj` is either a formula in `f'cmi` (a lower-strength
form for `f'cmi ≤ 40 MPa` and a different form above that), determined by
AS 1012.17 test, or read from Table 3.1.2 for standard grades at 28 days.
The clause flags a ±20% scatter band around the formula
value — this matters for stiffness-sensitive checks (deflection, drift,
dynamic period).

![[as3600-table-3.1.2-concrete-properties-at-28-days.png]]
*Table 3.1.2 — concrete properties at 28 days (mean/characteristic
compressive strength, tensile strength, modulus of elasticity) by standard
strength grade (AS 3600:2018).*

### Density, stress-strain shape, Poisson's ratio, thermal expansion (Cl 3.1.3–3.1.6)

`[code]` Density by test (AS 1012.12.1/.2); normal-weight concrete is
commonly taken as 2400 kg/m³ per the clause note. Stress-strain curve either
a recognised curvilinear form or from test data. Poisson's ratio taken as 0.2
or by test (AS 1012.17). Coefficient of thermal expansion taken as
10×10⁻⁶/°C (±20% scatter noted) or from test data.

### Shrinkage (Cl 3.1.7)

`[code]` Design shrinkage strain `εcs` may come from measurements on similar
local concrete, from AS 1012.13 tests (8-week drying, extrapolated), or by
calculation (Cl 3.1.7.2) as the sum of autogenous shrinkage `εcse` and drying
shrinkage `εcsd`. Both components have their own predictive sub-models keyed
to `f'c`, time since setting/drying, and an environment factor (arid /
interior / temperate inland / tropical-or-coastal — four bands, each with its
own coefficient). `[derived]` The autogenous-shrinkage exponential form and
the drying-shrinkage `k1·k4·εcsd.b` form are restated in the clause; the
environment-factor coefficient values and the 30-year typical-strain table
(Table 3.1.7.2) are data. Overall model
scatter is flagged at ±30%.

![[as3600-fig-3.1.7.2-shrinkage-k1-coefficient.png]]
*Figure 3.1.7.2 — drying-shrinkage coefficient `k1` vs. time since drying
began, by environment band (AS 3600:2018).* Practical note in the clause: uncontrolled
drying between casting and curing can produce shrinkage from suction that
exceeds all other shrinkage components combined — curing timing matters more
than the calculation precision.

![[as3600-table-3.1.7.2-design-shrinkage-strains.png]]
*Table 3.1.7.2 — typical final design shrinkage strains after 30 years, by
environment (AS 3600:2018).*

### Creep (Cl 3.1.8)

`[code]` Creep strain at time `t` under sustained stress `σo` is
`σo/Ec` scaled by a design creep coefficient `φcc(t)`, itself built from a
basic creep coefficient `φcc.b` (from local measurement, AS 1012.16 test, or
Table 3.1.8.2 by strength grade) multiplied by a chain of
factors: age-at-loading, duration, environment (same four-band split as
shrinkage), a high-strength-concrete modifier (unity below 50 MPa, a formula
above it), and a non-linearity modifier that only bites once sustained stress
exceeds 0.45×`f'cmi`. Scatter ≈ ±30%, worse above ~25°C sustained temperature.
The clause explicitly recommends permanent-effect (including prestress)
compressive stress be kept ≤ 0.45×`f'cmi`. 30-year final creep coefficients
are tabulated (Table 3.1.8.3).

![[as3600-fig-3.1.8.3-creep-k2-coefficient.png]]
*Figure 3.1.8.3 — creep coefficient `k2` vs. time since loading, by
environment band (AS 3600:2018).*

![[as3600-table-3.1.8.2-basic-creep-coefficient.png]]
*Table 3.1.8.2 — basic creep coefficient φcc.b by hypothetical thickness and
characteristic strength (AS 3600:2018).*

![[as3600-table-3.1.8.3-final-creep-coefficients.png]]
*Table 3.1.8.3 — final creep coefficients (after 30 years) for concrete first
loaded at 28 days, by environment and hypothetical thickness (AS 3600:2018).*

### Material properties for non-linear analysis (Cl 3.5)

`[code]` Where a structure is analysed by non-linear frame analysis (Cl 6.5)
or non-linear stress analysis (Cl 6.6), **mean** values of all relevant
material properties are used, expressed as full stress-strain curves rather
than characteristic design values — see
[[as3600-nonlinear-analysis-methods]].

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-properties-of-reinforcement]], [[as3600-properties-of-tendons-and-prestress-losses]]
  — companion material-property pages.
- [[as3600-nonlinear-analysis-methods]] — where the Cl 3.5 mean-property
  requirement is used.
- [[as3600-limit-state-design-basis]] — Cl 2.1.6 requires all design
  properties to trace back to this section.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clauses 3.1, 3.5 (Tables
  3.1.1.1, 3.1.2, 3.1.7.2, 3.1.8.2, 3.1.8.3, and Figures 3.1.7.2, 3.1.8.3,
  reproduced as image assets above).
