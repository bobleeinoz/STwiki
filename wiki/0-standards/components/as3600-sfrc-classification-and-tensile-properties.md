---
title: SFRC — scope, classification and tensile/compressive properties
category: 0-standards
tags: [sfrc, steel-fibre-reinforced-concrete, residual-tensile-strength, testing]
standards: [AS 3600:2018 Cl 16.1, AS 3600:2018 Cl 16.2, AS 3600:2018 Cl 16.3]
status: draft
reviewed: 2026-09-16
---

# SFRC — scope, classification and properties

> Scope: AS 3600 Section 16 general/definitions/properties (Cl 16.1–16.3) —
> what SFRC design in this Standard covers, softening-vs-hardening
> classification, and how compressive and residual tensile strength are
> determined and graded. Member design is
> [[as3600-sfrc-member-design]]; durability/fire/production is
> [[as3600-sfrc-durability-fire-and-production]].

## Summary

`[code]` Section 16 sets minimum requirements for steel fibres conforming to
ISO 13270 or EN 14889 in building structures/members (Cl 16.1). It excludes
slabs on grade, temporary sprayed linings, and applications aimed at plastic-
shrinkage/abrasion/impact resistance. Design (ULS and SLS) is based on
stress–COD (crack-opening-displacement) relationships for SFRC in tension,
determined by testing per Cl 16.3.3. Steel fibres may supplement
conventional reinforcement/tendons, including in statically indeterminate
systems where cracking won't cause sudden collapse; redistribution/plastic
analysis (Cl 2.2.2) is permitted where high-moment regions have sufficient
moment-rotation capacity. Fibres are never relied on at construction joints.
Only **softening**-classification SFRC is covered — hardening SFRC and
synthetic fibres are out of scope (Cl 16.1, Note: hardening = tensile
strength ≥1.1× the fibre-free matrix strength at COD ≥0.3 mm).

`[derived]` Note 1 to Cl 16.1 flags a durability caveat for brittle,
high-bond fibres in high-strength concrete: fibre fracture (rather than
pullout) can erode member ductility as bond strength gains with time — worth
checking against manufacturer data for high-`f'c` mixes.

## Detail

### Classification (Cl 16.2–16.3.1, Figure 16.3.3.1)

`[code]` Key definitions (Cl 16.2): **CMOD** — crack mouth opening
displacement in an EN 14651 flexural test; **COD** — crack opening
displacement, averaged over 4 sides, in an Appendix C direct tensile
dog-bone test; **target dosage** — specified fibre mass per m³ (kg/m³).

`[code]` SFRC is classified by both `f'c` (Cl 16.3.2, per Cl 3.1.1.1; mean
in-situ strength `fcmi` may be taken as `0.9 fcm` absent better data) and
characteristic residual tensile strength `f'1.5` (Cl 16.3.3.3). Tensile
behaviour is classified softening or hardening per Figure 16.3.3.1 —
hardening SFRC is out of scope for this section.

![[as3600-fig-16.3.3.1-classification-of-sfrc.png]]
*Figure 16.3.3.1 — classification of SFRC: (a) strain-softening SFRC, stress
drops from `fct` at crack formation to `f0.5`/`f1.5` at 0.5/1.5 mm COD; (b)
strain-hardening SFRC, stress rises past crack formation (`fctm`) to crack
localisation (`fct ≥ 1.1 fctm`) at COD ≥0.3 mm before softening
(AS 3600:2018).*

### Residual tensile strength (Cl 16.3.3.2–16.3.3.6)

`[code]` Matrix tensile strength `fct` (Cl 16.3.3.2) comes from direct/
indirect testing per Cl 3.1.1.3, or is calculated from `f'c` alone via the
same clause. Standard characteristic residual tensile strength grades
(`f'1.5`): 0.4, 0.6, 0.8, 1.2, 1.6, 2.0 MPa (Cl 16.3.3.3), determined
statistically per Cl 16.3.3.4 (direct) or 16.3.3.5 (indirect); higher grades
need direct testing. Similar mixes (fibre type/content, w/cm ratio, max
aggregate size, aggregate geology, `f'c` all matching) with fibre-content
differences ≤20 kg/m³ may be linearly interpolated (Cl 16.3.3.3 Note 1).

`[code]` **Direct testing** (Cl 16.3.3.4): `f'0.5`, `f'1.5` from Appendix C
or an independently verified method, multiplied by the 3D orientation
factor `k3Dt = 1/(0.94 + 0.6·lf/b) ≤ 1`; or, via matched direct/indirect
testing (Cl 16.3.3.6), `f'0.5 = kR,2 fR,2`, `f'1.5 = kR,4 fR,4`. Statistical
basis for all characteristic values here and in Cl 16.3.3.7: normal
distribution, ISO 12491, 75% confidence level (95% of population exceeds the
characteristic value), COV floor of 0.25, minimum 6 specimens. Interpolation/
extrapolation between/beyond `f'0.5` and `f'1.5` is capped `0 ≤ · ≤ f'0.5`.
`f'1.5` is capped at `0.9 f'0.5`.

`[code]` **Indirect testing** (Cl 16.3.3.5): `f'0.5 = k3Db·min(−0.04fR,4 +
0.37fR,2, 0.36√f'c)`; `f'1.5 = k3Db·min(0.4fR,4 − 0.07fR,2, 0.36√f'c)`, with
`k3Db = 1/(1 + 0.19·lf/b) ≤ 1` (`b` = prism sectional width; conservatively
`k3Db = 0.92` for fibres ≤70 mm). Same `f'1.5 ≤ 0.9f'0.5` cap and
interpolation/extrapolation rule as direct testing.

`[code]` **Residual flexural tensile strength `fR,j`** (Cl 16.3.3.7): from
EN 14651 three-point notched-bending tests on 150 mm-square prisms (25 mm
notch), `fR,j = 3FRj·L/(2b·hsp²)`, reading load `FRj` at CMOD `j` off a
force–CMOD plot (Figure 16.3.3.7 — describes the four standard CMOD readings
`FR,1`–`FR,4`, not reproduced). NATA-accredited testing is recommended.

### Minimum fibre dosage and modulus (Cl 16.3.3.8, Cl 16.3.4)

`[code]` Serviceability: `fR,1m/fLm > 0.4`. Strength: `fR,1m/fLm > 0.4` **and**
`fR,3m/fR,1m > 0.5` (`fLm` = mean flexural strength at the limit of
proportionality). Alternatively, minimum dosage = the greater of
`12γs(df/lf)²` (`γs` = mass density of steel, taken as 7850 kg/m³; `df` =
fibre diameter, `lf` = fibre length) and 20 kg/m³. `Ecj` per Cl 3.1.2.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-sfrc-member-design]] — Cl 16.4, how `f'1.5` and `fR,j` feed
  bending, shear and serviceability design.
- [[as3600-sfrc-durability-fire-and-production]] — Cl 16.5–16.7,
  durability/fire treatment and production QA for the fibres classified
  here.
- [[as3600-properties-of-concrete]] — Cl 3.1, the base `f'c`/`Ecj`
  framework this section extends for fibres.
- [[as3600-fatigue-design-detailed-provisions]] — Cl 16.4.6 bars fibres
  from fatigue-resistance calculations absent test evidence.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clauses 16.1–16.3
  (Figure 16.3.3.1 reproduced in `wiki/0-standards/assets/`; Figure 16.3.3.7
  described in words).
