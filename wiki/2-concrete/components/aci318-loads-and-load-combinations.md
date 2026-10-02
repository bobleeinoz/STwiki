---
title: ACI 318M-19 loads and load combinations — Table 5.3.1, special load factors
category: 2-concrete
tags: [aci, loads, load-combinations, asce-7]
standards: [ACI 318M-19 Cl 5.2, ACI 318M-19 Cl 5.3]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 loads and load combinations

> Scope: ACI 318M-19 Chapter 5 — the required-strength load combinations of
> Table 5.3.1, live load reduction, and the special load-factor provisions
> for wind, seismic, volume change/settlement (T), fluid (F), lateral earth
> pressure (H), flood, ice and prestressing. This is an **ACI 318M-19 page,
> kept separate from the AS 3600:2018 concept pages** elsewhere in
> `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Chapter 5 governs selection of load factors and combinations
(Cl 5.1.1). Loads themselves — dead, live, wind, earthquake, and Seismic
Design Category (SDC) assignment — are **not defined by this Code**; they
come from the jurisdiction's general building code, or from ASCE/SEI 7 in
its absence (Cl 5.2.1–5.2.2, Cl R5.2.1). `[derived]` This is a structural
difference from AS 3600, which cross-references AS/NZS 1170 directly as part
of the concrete standard's own ecosystem — ACI 318 instead treats loads as
entirely external to itself, deferring to ASCE/SEI 7 or whatever general
building code applies.

## Detail

### Required strength — Table 5.3.1 (Cl 5.3.1)

![[aci318-table-5.3.1-load-combinations.png]]
*Table 5.3.1 — load combinations: `U = 1.4D`; `U = 1.2D + 1.6L +
0.5(Lr or S or R)`; `U = 1.2D + 1.6(Lr or S or R) + (1.0L or 0.5W)`;
`U = 1.2D + 1.0W + 1.0L + 0.5(Lr or S or R)`; `U = 1.2D + 1.0E + 1.0L + 0.2S`;
`U = 0.9D + 1.0W`; `U = 0.9D + 1.0E` (ACI 318M-19).*

`[code]` The `0.9D` combinations (5.3.1f/g) cover the case where a **higher**
dead load reduces the effects of other loads — e.g. uplift/overturning
checks, or a tension-controlled column section where less axial compression
combined with the same or greater moment governs (Cl R5.3.1). `[code]`
Load effects not acting simultaneously must still each be investigated
(Cl 5.3.2). `[derived]` Due regard must be given to sign — one load type can
produce effects opposite in sense to another, and it should not be assumed
every critical combination is captured by the table as written (Cl R5.3.1).

`[code]` Earthquake effect `E` in the model-code references this table draws
from already includes **both** horizontal (`E_h`) and vertical (`E_v`)
ground-motion components — the vertical component applies as an addition to
or subtraction from `D`, to **every** structural element whether or not it's
part of the seismic-force-resisting system, unless the general building code
specifically excludes it (Cl R5.3.1). `[derived]` A page or calculation
using `E` from this table without separately accounting for `E_v` is
silently dropping part of the seismic load effect the equation assumes is
already folded in.

### Live load factor reduction (Cl 5.3.3) and live load scope (Cl 5.3.4)

`[code]` The live load factor in Eq. 5.3.1c/d/e may be reduced from 1.0 to
**0.5**, *except* for: (a) garages, (b) areas of public assembly, or
(c) areas where `L > 4.8 kN/m²` (Cl 5.3.3). `[derived]` This 0.5 reduction
is a **load-combination-level** adjustment, separate from and usable in
combination with any loaded-area-based live load reduction (`L_0 → L`)
already applied per the general building code (Cl R5.3.3) — the two are not
mutually exclusive. `L` where applicable must include concentrated loads,
vehicular loads, crane loads, handrail/guardrail/vehicular barrier loads,
impact and vibration effects (Cl 5.3.4).

### Wind load factor (Cl 5.3.5)

`[code]` If `W` is supplied at **service-level** (not strength-level), use
`1.6W` in place of `1.0W` in Eq. 5.3.1d/f, and `0.8W` in place of `0.5W` in
Eq. 5.3.1c (Cl 5.3.5). `[derived]` ASCE/SEI 7-16 and later give strength-level
wind loads directly (factor 1.0 already baked in via mean-recurrence-interval
design wind speeds of 300–1700 years depending on risk category); the
1.6/0.8 factors exist specifically for the older ASCE/SEI 7-05 convention of
service-level (50-year MRI) wind loads (Cl R5.3.5) — citing which edition of
wind-load basis is in use is necessary to know which factor set applies.

### Volume change, settlement, and other special loads (Cl 5.3.6–5.3.13)

`[code]` **Restraint effects `T`** (volume change, differential settlement):
included in combination with other loads only where they can adversely
affect safety/performance, with a load factor reflecting uncertainty in
magnitude/simultaneity/consequences, **never less than 1.0** (Cl 5.3.6).
`[derived]` In practice, `T` forces are rarely calculated explicitly — design
instead typically relies on compliant members, ductile connections,
expansion joints and shrinkage/temperature reinforcement proportioned on
gross area rather than calculated force (Cl R5.3.6); see
[[aci318-serviceability-deflection-and-cracking]] for the shrinkage/
temperature steel minimum.

`[code]` **Fluid load `F`**: factor 1.4 if acting alone/adding to `D`
(Eq. 5.3.1a); 1.2 if adding to the primary load (Eq. 5.3.1b–e); 0.9 if
permanent and counteracting the primary load (Eq. 5.3.1g); excluded entirely
if non-permanent and counteracting (Cl 5.3.7). **Lateral earth pressure
`H`**: factor 1.6 if acting alone/adding; 0.9 if permanent and counteracting;
excluded if non-permanent and counteracting (Cl 5.3.8) — reflecting that
retained material can potentially be removed (Cl R5.3.8). **Flood** and
**atmospheric ice** loads: use ASCE/SEI 7's own load factors/combinations
directly, not this table (Cl 5.3.9–5.3.10).

`[code]` **Prestressing**: internal load effects from reactions induced by
prestressing (secondary moments in indeterminate structures) use load factor
**1.0** always (Cl 5.3.11). Post-tensioned anchorage zone design uses a
**1.2** factor on the maximum jacking force (Cl 5.3.12) — calibrated to
roughly 113% of specified yield strength but no more than 96% of nominal
tensile strength, comparing well against the ≥95%-of-nominal-tensile-strength
minimum anchorage capacity (Cl R5.3.12). For the strut-and-tie method (see
[[aci318-strut-and-tie-method]]): prestressing gets a **1.2** factor where it
*increases* net strut/tie force, **0.9** where it *reduces* it (Cl 5.3.13).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-structural-analysis-methods]] — Chapter 6, the analysis methods
  these factored loads feed into.
- [[concrete-limit-state-design-basis]] — the AS 3600 equivalent (AS/NZS
  1170-based combinations), for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 5 (Cl 5.1–5.3.13, pp. 61–66),
  incl. Table 5.3.1.
