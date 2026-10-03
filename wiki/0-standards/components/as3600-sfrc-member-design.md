---
title: SFRC member design — bending, shear, strut-and-tie, fatigue, serviceability
category: 0-standards
tags: [sfrc, bending, shear, deflection, crack-control, strut-and-tie]
standards: [AS 3600:2018 Cl 16.4]
status: draft
reviewed: 2026-09-16
---

# SFRC member design

> Scope: AS 3600 Cl 16.4 — design of reinforced/prestressed beams containing
> steel fibres, for bending, shear, strut-and-tie tension, fatigue and
> serviceability (stress limits, deflection, crack control).

## Summary

`[code]` Cl 16.4.1 applies to reinforced/prestressed beams with steel fibres
under any combination of shear, bending and axial force — **not** where
torsion acts with shear, and not to non-flexural members (which use Section
12/16.4.5 strut-and-tie provisions instead).

## Detail

### Strength in bending and combined bending/axial force (Cl 16.4.2)

`[code]` Assumptions: plane sections remain plane; for a rectangular tension
zone, SFRC tensile stress = `0.9 kg f'1.5` (`kg` = member-size factor); for
I-sections/non-rectangular tension zones, tensile-side flange overhang area
is factored by 0.67; compressive stress distribution per Cl 3.1.4; maximum
compressive-fibre strain 0.003. Member size factor: `kg = 1 + 0.0067·Actu/Ao
≤ 1.6`, with `Ao = 15 600 mm²` (`Actu` = tensile-zone concrete area at
ULS). Strength is determined from rectangular stress blocks for concrete in
compression **and** in tension (Figure 16.4.2). Where the average tensile
strain `εt = 0.003(dz − dn)/dn` exceeds 0.025 at some depth `dz`, the fibre
contribution there is ignored.

![[as3600-fig-16.4.2-sfrc-stress-block.png]]
*Figure 16.4.2 — stress block and forces on a reinforced SFRC section: (a)
single tensile reinforcement layer; (b) multiple layers — compression `Cs +
Cc`, fibre tension `Tf = 0.9kg f'1.5`, steel tension `Ts` (AS 3600:2018).*

`[code]` Minimum tensile reinforcement (Cl 16.4.3) follows the Cl 8.1.6
principles excluding fibres — waived at critical sections of a statically
indeterminate member if sudden collapse/reduced collapse load is precluded;
doesn't apply to soil-supported foundation/pavement slabs.

### Shear strength (Cl 16.4.4)

`[code]` `Vu = Vuc + Vuf + Vus` (`Vuc`, `Vus` per Cl 8.2.3; `Vuf` per Cl
16.4.4.2). `Vuf` is capped at `max(Vuc, Cl 16.4.4.3 value with Vus = 0)`.

`[code]` **Refined `Vuf`** (Cl 16.4.4.2.1): `Vuf = ks·kg·dv·bv·f'w·cotθv`,
with `ks = 0.64` (fibre orientation/casting bias), `kg` per Cl 16.4.2,
`θv`/`dv` per Cl 8.2.4.2/8.2.1.9. `f'w` (residual tensile strength at crack
width `w`) comes from Cl 16.3.3.4/.5/.6, with `w = (0.2 + 1000εx)·[(1000 +
kdg·dv)/1300]·(1/cosθ) ≥ 0.125 mm`, driven by `εx` (Cl 8.2.4.3); for beams
<1000 mm deep, `f'w` may simply equal `f'1.5`.

`[code]` **Simplified `Vuf`** (Cl 16.4.4.2.2): for non-prestressed members
without axial tension, `fsy ≤ 500 MPa`, `f'c ≤ 65 MPa`, max aggregate
≥10 mm, fibre length ≤70 mm, depth ≤1000 mm — `θv = 36°` fixed, `kv` per Cl
8.2.4.3, `f'w = f'1.5`.

`[code]` Minimum shear reinforcement (Cl 16.4.4.3): `(Vus + Vuf)min ≥
0.1 bv do √f'c` and `≥ 0.6 bv do`.

### Strut-and-tie, fatigue (Cl 16.4.5–16.4.6)

`[code]` Fibres may combine with bar reinforcement for strut-and-tie
bursting tension if service-load crack width ≤0.5 mm and fibres carry ≤30%
of the total ULS tension (bars carry the remainder) — see
[[as3600-strut-and-tie-modelling]]. Fibres are excluded from fatigue-
resistance calculations unless demonstrated by testing.

### Serviceability — stresses, deflection, crack control (Cl 16.4.7)

`[code]` **General** (Cl 16.4.7.1): an uncracked section is fully active,
elastic in both tension and compression; a cracked section is elastic in
compression and sustains tensile stress `1.1 f'0.5` (default `f'0.5 =
1.1 f'1.5` if unspecified). **Stress limits** (Cl 16.4.7.2): concrete
compressive stress ≤`0.6 fcmi(t)` at SLS, ≤`0.4 fcmi(t)` under permanent
effects (concrete tensile-stress SLS limits may be skipped if ULS
performance is satisfactory); reinforcing steel SLS tensile stress ≤`0.8
fsy`.

`[code]` **Deflection** (Cl 16.4.7.3): short-term deflection uses `Ecj` (Cl
3.1.2) and effective second moment of area `Ief`, by rational calculation or
at nominated cross-sections (mid-span for simple spans; half mid-span + 1/4
each support for interior continuous spans; half mid-span + half the
continuous-support value for end spans; support value for cantilevers).
`Ief` at each section derives from the instantaneous curvature `ki =
Ms*/(Ecj Ief)`, obtained as the slope of the strain diagram satisfying
rotational/horizontal equilibrium of the stress distribution.

![[as3600-fig-16.4.7.3.2-cracked-section-stress-strain.png]]
*Figure 16.4.7.3.2 — stress and strain distribution on a cracked SFRC
section under `Ms*`: (a) section with `Ast`; (b) strain (`ε0` at top,
`εs = ε0(d−dn)/dn` at steel); (c) stress (`σ0 = Ecjε0` compression,
`f'0.5` tension plateau, `σs = Esεs` at steel); (d) resultant forces `Cc` at
`dn/3`, tension couple at `(D+dn)/2` (AS 3600:2018).*

`[code]` Long-term deflection (Cl 16.4.7.3.3) = shrinkage component (from
design shrinkage strain `εcs`, Cl 3.1.7.1) + creep component (from design
creep coefficient `φcc(t)`, Cl 3.1.8.3), both via mechanics principles.

`[code]` **Flexural crack control** (Cl 16.4.7.4): calculated per Cl 8.6.2.3,
except the second RHS term of Eq 8.6.2.3(2) is multiplied by `kf1 = 1/(1 +
f'1.5/fct)`, and `sr,max` (Eq 8.6.2.3(3)) is multiplied by `kf2 =
fct/(kg(fct − 1.1f'1.5) + 0.25fct)`.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-sfrc-classification-and-tensile-properties]] — Cl 16.3, the
  `f'1.5`/`fR,j`/`kg` inputs used throughout this page.
- [[as3600-beam-strength-in-bending]], [[as3600-beam-shear-and-torsion-design]]
  — Sections 8.1/8.2 baseline `Vuc`/`Vus`/stress-block framework this
  section extends with fibre terms.
- [[as3600-beam-crack-control]] — Cl 8.6.2.3, the crack-width formula
  modified by `kf1`/`kf2`.
- [[as3600-strut-and-tie-modelling]] — Section 7, host framework for
  Cl 16.4.5's fibre/bar tension split.
- [[as3600-fatigue-design-detailed-provisions]] — Section 18, why fibres
  can't substitute for fatigue-resistant reinforcement absent testing.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 16.4 (Figures
  16.4.2 and 16.4.7.3.2 reproduced in `wiki/0-standards/assets/`).
