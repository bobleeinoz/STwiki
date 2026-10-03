---
title: Concrete fatigue design — general, plain concrete, shear, bond factor and flexural-member provisions
category: 0-standards
tags: [fatigue, plain-concrete, shear, slabs, bond, prestressing, strut-angle]
standards: [AS 3600:2018 Cl 18.1, AS 3600:2018 Cl 18.3, AS 3600:2018 Cl 18.4, AS 3600:2018 Cl 18.5, AS 3600:2018 Cl 18.6, AS 3600:2018 Cl 18.7, AS 3600:2018 Cl 18.9]
status: draft
reviewed: 2026-10-03
---

# Concrete fatigue design — general, plain concrete, shear, bond factor and flexural-member provisions

> Scope: AS 3600:2018 Section 18 clauses other than 18.2 (compression in
> concrete) and 18.8 (steel stress range), which sit on
> [[as3600-fatigue-design-overview]]. Covers the general basis (18.1), plain
> concrete in tension (18.3, 18.4), shear (18.5, 18.6), the bond adjustment
> factor for mixed reinforcing/prestressing steel (18.7) and flexural-member
> stress calculation (18.9). Equations are described in words and by symbol;
> see the source for the printed forms.

## Summary

`[code]` Fatigue is treated as a strength limit state evaluated at the
operational/serviceability load combination (Cl 18.1, Note). The fatigue
design action `Qfat` and foreseen cycle count `nsc` come from Cl 2.1.5, and the
load combination from Cl 2.5.2.3 (Cl 18.1) — see
[[as3600-limit-state-design-basis]].

`[code]` Capacity factors for fatigue are in Table 2.4 (see
[[as3600-fatigue-design-overview]]); Cl 18.8 fixes the steel factor
`φs,fat` at 0.85.

## Detail

### 18.1 General

- `[code]` For prestressed members the section shall be assessed for
  sensitivity to cracking. If any combination causes tensile stress at the
  concrete surface, stress ranges for concrete, reinforcing steel and tendons
  shall be calculated on a cracked section (Cl 18.1).
- `[code]` Nominal stresses are calculated at the site of potential fatigue
  initiation. The critical section is per Section 6 including Cl 6.2.1 and
  6.2.3, with additional checks at changes in section, or in quantity or
  direction of reinforcement (Cl 18.1).
- `[code]` Concrete compression stress under the permanent design actions
  `[G, γpP]` shall not exceed `0.45 f'c` (Cl 18.1).

### 18.3 Plain concrete — compression with tension stress

- `[code]` The maximum tensile stress `σct,max` is limited to
  `σc,max / 38.5` (Eq 18.3(1)). The resisting cycles satisfy
  `log N = 9 (1 − σc,max / (φc,fat·fc,fat))` (Eq 18.3(2)), with `fc,fat` as in
  Cl 18.2 (Cl 18.3, amended by A1/A2).
- `[code]` Note to Cl 18.3: equivalently, the permitted `σc,max` is
  `φc,fat·fc,fat·(1 − log nsc / 9)`.

### 18.4 Plain concrete — pure tension or combined tension-compression

- `[code]` Applies where `σct,max > σc,max / 38.5` (Eq 18.4(1)). The resisting
  cycles satisfy `log N = 12 (1 − σct,max / (φc,fat·f'ct))` (Eq 18.4(2)); the
  Note gives the permitted tensile stress as
  `φc,fat·f'ct·(1 − log nsc / 12)` (Cl 18.4, amended A1/A2).

### 18.5 Shear limited by web compressive stresses

- `[code]` In flexural members, the maximum shear under permanent effects plus
  fatigue loading shall not exceed `0.6 φ Vu.max`, with `Vu.max` from
  Cl 8.2.3.3 (Cl 18.5). See [[as3600-beam-shear-and-torsion-design]].

### 18.6 Shear in slabs

- `[code]` Maximum slab shear force, determined per Cl 9.3 under permanent
  effects plus fatigue loading, is limited as follows (Cl 18.6.1).
- `[code]` Where the number of stress cycles is not greater than 2 × 10⁶ and the
  slab can act as a wide beam with a shear failure across a substantial width:
  `0.6 φ Vu`; otherwise `0.54 φ Vu` (Cl 18.6.2(a)).
- `[code]` If the longitudinal tensile reinforcement ratio
  `(Ast + Apt)/(b·do)` is below 0.01, multiply the permissible shear by
  `(100(Ast + Apt)/(b·do))^(1/3)` (Cl 18.6.2(a)).
- `[code]` Where the failure surface could form a truncated cone or pyramid
  around a support or loaded area, the calculated shear shall not exceed
  `0.5 φ Vuo` (Vuo per Cl 9.3.4) (Cl 18.6.2(b)). See
  [[as3600-slab-punching-shear]].

### 18.7 Bond adjustment factor for reinforcing and prestressing steel

- `[code]` To allow for different bond behaviour, the tensile stress range in
  the reinforcing steel is multiplied by `ηs` unless a more refined method is
  used: `ηs = (1 + Ap/As) / (1 + (Ap/As)·√(ξ·db/dp))` (Eq 18.7). Here `As`,
  `Ap` are reinforcing and prestressing steel areas, `db` the smallest
  reinforcing bar diameter in the section, `dp` the prestressing steel diameter
  (for bundles an equivalent `1.6√Ap`) (Cl 18.7).
- `[code]` `ξ` for post-tensioned members: 0.2 smooth prestressing steel; 0.4
  strands; 0.6 ribbed wires; 1.0 ribbed bars. For pretensioned members: 0.6
  strands; 0.8 ribbed prestressing steels (Cl 18.7).

### 18.9 Stresses in reinforcement and tendons of flexural members

- `[code]` Fatigue resistance of the longitudinal reinforcement and tendons,
  and of the shear reinforcement, shall be determined (Cl 18.9).
- `[code]` The strut angle to the member axis is chosen between 35° and 55°,
  except non-prestressed slabs and trough girders: 40° to 55° (Cl 18.9).

## Contradictions

None recorded.

`[derived]` Editorial inconsistencies in the printed standard, noted for the
reader and not changing any requirement: Cl 18.2's list of variables says the
strength-gain coefficient `s` is "given in Table 18.3", but the table is
printed as Table 18.2; and the variable-amplitude damage sum in Cl 18.2 is
numbered 18.2(3), duplicating the number used for the cycle equation. Treat
the page as a draft until the human confirms these against the current
amendment.

## Related

- [[as3600-fatigue-design-overview]] — Cl 2.4, 18.2 and 18.8 (Tables 2.4, 18.2,
  18.8, Figure 18.8).
- [[as3600-limit-state-design-basis]] — Cl 2.1.5 applicability and combinations.
- [[as3600-sfrc-member-design]] — Cl 16.4.6, why fibres cannot replace
  fatigue-resistant reinforcement absent testing.
- [[as-3600-2018-concrete-structures]] — source register.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Section 18, Cl 18.1,
  18.3–18.7 and 18.9 (printed pp. 241–248; read visually). AS 3600:2018
  incorporating the amendments (A1, A2) marked in the margin of the reprint.
