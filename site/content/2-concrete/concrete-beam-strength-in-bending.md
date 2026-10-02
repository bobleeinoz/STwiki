---
title: Strength of beams in bending
category: 2-concrete
tags: [beams, bending, flexure, rectangular-stress-block]
standards: [AS 3600:2018 Cl 8.1]
status: draft
reviewed: 2026-09-12
---

# Strength of beams in bending

> Scope: AS 3600 Cl 8.1 — the assumptions and rectangular-stress-block method
> for beam bending strength, minimum strength, tendon/reinforcement stress at
> ultimate, and bar/tendon spacing. Applies to reinforced and bonded
> prestressed beams; does not apply to non-flexural members (Section 12).
> T-/L-beam flange properties come from Cl 8.8 — see
> [[concrete-beam-vibration-tbeams-slenderness]].

## Summary

`[code]` Bending strength calculations must satisfy equilibrium and
strain-compatibility using: plane sections remain plane (except unbonded
tendons, Cl 8.1.8); concrete has no tensile strength; compressive stress
distribution from the Cl 3.1.4 stress-strain relationship; and compressive
reinforcement strain capped at 0.003 (Cl 8.1.2).

## Detail

### Rectangular stress block (Cl 8.1.3)

`[code]` Deemed to satisfy Cl 8.1.2 by assuming: maximum extreme-fibre
compressive strain of 0.003, and a uniform compressive stress of `γ₂·f'c`
over the area bounded by the section edges and a line parallel to the neutral
axis at depth `kᵤd` from the extreme compression fibre — where `γ₂` is a
strength-dependent factor (bounded roughly 0.67–0.85, reducing as `f'c`
increases) already incorporating the 0.9 modifier from Cl 3.1.4. `[derived]`
The exact linear coefficients defining `γ₂` (and the companion `kᵤ`-limit
factor) are short formulas rather than a table, but the OCR extraction of
this clause was unreliable on the numeric coefficients — confirm the precise
values against Cl 8.1.3 before use. `γ₂` is reduced 5% for circular sections
and 10% for sections that narrow from the neutral axis toward the compression
face. Dispersion angle for a concentrated/anchorage load, absent more exact
calculation, is 60° total (30° each side of the load's line of action);
resulting splitting/bursting forces are designed per Section 7 — see
[[concrete-strut-and-tie-modelling]].

### Design strength in bending (Cl 8.1.5)

`[code]` Design strength is capped at `φ·Muo`, `φ` from Table 2.2.2(b) (see
[[concrete-strength-check-procedures]]). Sections with a high neutral-axis
parameter `kᵤo > 0.36` combined with `M* > 0.8·φ·Muo` may only be used where
the structural analysis is elastic (Cl 6.2–6.6, not plastic) **and**
compression reinforcement of at least 1% of the compression-zone concrete
area is provided and restrained per Cl 8.3.1.6/10.7.4 — own-words: this
prevents an over-reinforced, brittle section from being pushed hard by
elastic analysis without a ductility safeguard. Earthquake ductility
requirements (Cl 14.4.6) apply where relevant.

### Minimum strength (Cl 8.1.6)

`[code]` `Muo` at any critical section must be ≥ `(Muo)min`, calculated from
the uncracked section modulus, characteristic flexural tensile strength, and
effective prestress force/eccentricity (own-words: this is a
cracking-moment-based floor on strength, ensuring a section doesn't fail the
instant it cracks). May be waived at a statically indeterminate member's
critical section if sudden span collapse or reduced collapse load can be
shown not to result. For reinforced (non-prestressed) sections, deemed
satisfied by providing tensile reinforcement above a ratio that scales with
`√f'ct.f/fsy` and, for T-/L-sections, with flange geometry — different
coefficients apply depending on whether the web or the flange is in tension.

`[code]` **Prestressed beams at transfer**: checked under Cl 2.5.2.2 load
combinations (see [[concrete-limit-state-design-basis]]) with `φ = 0.6`.
Deemed satisfied if maximum concrete compressive stress at transfer doesn't
exceed 0.6×`f'cp` (rectangular section, triangular stress distribution) or
0.5×`f'cp` otherwise, where `f'cp` is concrete strength at transfer.

### Stress in reinforcement and bonded tendons at ultimate (Cl 8.1.7)

`[code]` Reinforcement stress capped at `fsy`. Bonded-tendon stress at
ultimate, absent more accurate calculation and provided minimum effective
tendon stress ≥ 0.5×`fpb`, is estimated from `fpb` reduced by a factor
involving the reinforcement/tendon area ratio, section geometry and concrete
strength — a bond-slip-based empirical model rather than a simple yield
check. Compression reinforcement only counts if its distance from the
extreme compression fibre stays within a stated fraction of the effective
prestressed depth.

### Stress in unbonded tendons (Cl 8.1.8)

`[code]` For unbonded tendons, ultimate stress is capped at `fpy` and
estimated from the effective post-loss stress plus an increment that depends
on concrete strength, tendon area ratio and effective depth — using one
formula for span-to-depth ratio ≤35 and a different (more conservative)
formula above 35, reflecting reduced strain compatibility in longer-span
unbonded members.

### Spacing (Cl 8.1.9)

`[code]` Minimum clear spacing between bars/bundles/ducts/tendons is set by
placement/compaction needs (Cl 17.1.3); maximum spacing is set by crack
control (Cl 8.6.1(b)) — see [[concrete-beam-crack-control]].

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-strength-check-procedures]] — φ values (Table 2.2.2) used
  throughout this page.
- [[concrete-beam-shear-and-torsion-design]] — the companion strength check
  for the same cross-sections.
- [[concrete-strut-and-tie-modelling]] — bursting/splitting design under
  concentrated loads.
- [[concrete-properties-of-concrete]], [[concrete-properties-of-tendons-and-prestress-losses]]
  — Cl 3.1.4/3.2.3 stress-strain inputs.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clause 8.1.
