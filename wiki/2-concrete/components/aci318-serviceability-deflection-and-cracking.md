---
title: ACI 318M-19 serviceability — deflection limits, effective Ie, crack-control spacing, prestressed stress limits
category: 2-concrete
tags: [aci, serviceability, deflection, crack-control, prestressed-stress-limits]
standards: [ACI 318M-19 Cl 24.2, ACI 318M-19 Cl 24.3, ACI 318M-19 Cl 24.4, ACI 318M-19 Cl 24.5]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 serviceability

> Scope: ACI 318M-19 Chapter 24 — deflection due to service-level gravity
> loads (including the 2019-revised effective moment of inertia), flexural
> reinforcement distribution for crack control in one-way slabs/beams,
> shrinkage and temperature reinforcement, and permissible stresses in
> prestressed flexural members (U/T/C classification). This is an **ACI
> 318M-19 page, kept separate from the AS 3600:2018 concept pages**
> elsewhere in `2-concrete` — see [[aci-318m-19-building-code-concrete]] for
> why.

## Summary

`[code]` Chapter 24 is explicitly **not** a complete, self-contained
serviceability compilation — it covers only the four topics referenced by
other chapters: deflection (24.2), one-way crack-control spacing (24.3),
shrinkage/temperature reinforcement (24.4), and prestressed permissible
stresses (24.5) (Cl R24.1). It has **no vibration requirements** — the
Commentary notes ordinary thickness/deflection compliance has generally
proven adequate for human-comfort vibration, except for long spans, strict
vibration-sensitive uses, or rhythmic/vibrating equipment loads, where
specialist guidance (PCI MNL 120, ATC DG-1, etc.) should be consulted
(Cl R24.1).

## Detail

### Deflection due to service-level gravity loads (Cl 24.2)

`[code]` Two compliance routes (Cl R24.2): nonprestressed one-way members
meeting the Cl 7.3.1/9.3.1 minimum-thickness tables (or two-way meeting
Cl 8.3.1) are **deemed to satisfy** deflection without calculation, for
members not supporting elements likely to be damaged by large deflections.
Everything else — members below minimum thickness, one-way members
attached to deflection-sensitive nonstructural elements, and **all**
prestressed flexural members — must have deflections calculated per
Cl 24.2.3–24.2.5 and checked against:

![[aci318-table-24.2.2-max-permissible-deflections.png]]
*Table 24.2.2 — maximum permissible calculated deflections: `ℓ/180` (flat
roofs not supporting deflection-sensitive elements), `ℓ/360` (floors,
same), `ℓ/480` (supporting elements likely to be damaged by large
deflection), `ℓ/240` (supporting elements not likely to be damaged)
(ACI 318M-19).* `[derived]` The `ℓ/480`/`ℓ/240` limits apply only to the
*portion* of deflection occurring **after** nonstructural element
attachment — the time-dependent deflection from sustained loads plus any
additional immediate live-load deflection, not the member's total
deflection from first loading (Table 24.2.2 note [2]). The `ℓ/180` flat-roof
limit is explicitly **not** a ponding safeguard — ponding needs its own
deflection check including the added weight of ponded water (note [1]).

`[code]` **Immediate deflection** (Cl 24.2.3): calculated by elastic methods
accounting for cracking/reinforcement effects on stiffness, considering
cross-section variation (haunches) and, for two-way slabs, panel size/shape/
support/restraint conditions. The 2019 Code introduced a revised **effective
moment of inertia**:

Table 24.2.3.5 — effective moment of inertia `I_e`:
- `M_a ≤ (2/3)M_cr`: `I_e = I_g` (uncracked)
- `M_a > (2/3)M_cr`: `I_e = I_cr / [1 − ((2/3)M_cr/M_a)²(1 − I_cr/I_g)]`

where `M_cr = f_r I_g / y_t` (modulus of rupture `f_r`, Cl 19.2.3). `[code]`
The two-thirds factor on `M_cr` in the trigger condition accounts for
restraint effects and reduced early-age tensile strength that can cause
cracking affecting later service deflections (Cl R24.2.3.5). `[derived]`
This Bischoff (2005) formulation **replaced** the pre-2019 Branson (1965)
equation specifically because Branson's formula underestimated deflections
for low-reinforcement-ratio members (common in slabs) and ignored restraint
— a page citing the old Branson `I_e` form is citing a pre-2019 edition. For
continuous one-way members, `I_e` may be averaged from the critical
positive/negative sections (Cl 24.2.3.6); for prismatic members, the
midspan value (or support value for cantilevers) may be used throughout
(Cl 24.2.3.7). Prestressed Class U members may use `I_g` directly
(Cl 24.2.3.8); Class T/C members need a cracked-transformed-section or
bilinear `I_e` analysis (Eq. 24.2.3.9a/b, Cl 24.2.3.9) — see classification
below.

`[code]` **Time-dependent deflection** (Cl 24.2.4), nonprestressed members:
additional deflection = immediate sustained-load deflection × `λ_Δ`, where:

**λ_Δ = ξ / (1 + 50ρ′)**  (Eq. 24.2.4.1.1, `ρ′` = compression
reinforcement ratio at midspan/support)

| Sustained load duration (months) | ξ |
|---|---|
| 3 | 1.0 |
| 6 | 1.2 |
| 12 | 1.4 |
| 60 or more | 2.0 |

*(Table 24.2.4.1.3 — ξ interpolated from the Fig. R24.2.4.1 curve for
intermediate durations.)* `[derived]` The `(1 + 50ρ′)` denominator captures
compression reinforcement's effect in reducing long-term creep camber/
deflection (Cl R24.2.4.1) — a section with more compression steel creeps
less. Prestressed members instead need explicit consideration of sustained-
load stresses, creep, shrinkage and prestress relaxation together
(Cl 24.2.4.2.1) — no simplified multiplier is given, because time-dependent
prestress loss interacts with the deflection itself (Cl R24.2.4.2.1).

`[code]` **Composite members** (Cl 24.2.5): if shored during construction so
dead load is resisted by the full composite section after shore removal,
treat as monolithic for deflection; if unshored, the loading
magnitude/duration before vs after composite action becomes effective must
be tracked separately, and differential-shrinkage deflection between precast
and cast-in-place components must be considered.

### Flexural reinforcement distribution for crack control (Cl 24.3)

`[code]` Applies to tension-zone bonded reinforcement in nonprestressed and
Class C prestressed one-way slabs/beams. Maximum spacing of the
reinforcement closest to the tension face:

![[aci318-table-24.3.2-max-spacing-crack-control.png]]
*Table 24.3.2 — maximum spacing `s` of bonded reinforcement: deformed
bars/wires use `f_s` (service-load stress); bonded prestressed reinforcement
uses `Δf_ps` scaled by a two-thirds effectiveness factor (weaker bond than
deformed bar); a combined case uses a five-sixths factor; all forms subtract
`2.5c_c` (least cover to the tension face) in one branch and cap at a flat
value in the other, whichever is lesser (ACI 318M-19).*

`[code]` `f_s` may be calculated from the unfactored service moment, or
taken simply as `(2/3)f_y` (Cl 24.3.2.1). `Δf_ps` is the cracked-section
service stress minus decompression stress `f_dc` (may be taken as `f_se`),
capped at 250 MPa, with the **spacing check waived entirely** if
`Δf_ps < 140 MPa` (Cl 24.3.2.2) — `[derived]` the waiver reflects that many
structures with such low prestressed-reinforcement stress change have
historically shown very limited flexural cracking (Cl R24.3.2.2). If only
one bonded bar/strand/tendon is nearest the tension face, the **extreme
tension face width itself** is limited to the Table 24.3.2 spacing
(Cl 24.3.3). For a tension-flange T-beam, reinforcement not over the web
must be spread across the lesser of the effective flange width or `ℓ_n/10`,
with extra bonded steel required in the outer flange if `ℓ_n/10` controls
(Cl 24.3.4). Members subject to fatigue, required to be watertight, or in
corrosive environments need spacing selected from specific investigation,
but never exceeding the Cl 24.3.2 limits (Cl 24.3.5).

### Shrinkage and temperature reinforcement (Cl 24.4)

`[code]` Required at right angles to the principal flexural reinforcement in
**structural** one-way slabs (not slabs-on-ground) to control cracking and
tie the structure together (Cl 24.4.1); where shrinkage/temperature movement
is restrained, Cl 5.3.6 thermal-effect load combinations apply (Cl 24.4.2).

`[code]` **Nonprestressed**: minimum ratio of deformed shrinkage/temperature
steel to gross concrete area = **0.0018** (Cl 24.4.3.2) — unchanged from
long practice, and the Commentary notes increased reinforcement grade gives
no crack-control benefit, so (unlike some earlier editions) there is **no
reduction for Grade > 420 reinforcement** (Cl R24.4.3.2). Spacing ≤ lesser
of `5h` and 450 mm (Cl 24.4.3.3); reinforcement must develop `f_y` in
tension at every section where required (Cl 24.4.3.4). One-way precast slabs
and precast/prestressed wall panels ≤ 3.6 m wide, not mechanically
restrained transversely, needing no transverse flexural reinforcement, are
exempt from the transverse shrinkage/temperature requirement entirely
(Cl 24.4.3.5) — the waiver does **not** apply where flexural strength needs
that reinforcement (e.g. thin tee flanges).

`[code]` **Prestressed**: shrinkage/temperature steel per Table 20.3.2.2,
with effective prestress after losses providing at least **0.7 MPa**
average compressive stress on the gross section (Cl 24.4.4.1) — calibrated
to roughly match the force needed to yield the equivalent nonprestressed
minimum steel (Cl R24.4.4.1).

### Permissible stresses in prestressed flexural members (Cl 24.5)

`[code]` Concrete stresses are limited per Cl 24.5.2–24.5.4 unless test/
analysis shows performance is unimpaired (Cl 24.5.1.1) — these are
**serviceability** limits, not a substitute for the Chapter 22 strength
check (Cl R24.5.1.1). Stress calculations at transfer, service and cracking
use elastic theory: strains linear with distance from the neutral axis
(Cl 22.2.1), and concrete resists no tension at cracked sections
(Cl 24.5.1.2).

`[code]` **Classification by extreme fibre tension `f_t`** in the
precompressed tension zone, at service loads, assuming an uncracked
section:

![[aci318-table-24.5.2.1-prestressed-member-classification.png]]
*Table 24.5.2.1 — Class U (`f_t ≤ 0.62√f'c`, uncracked), Class T
(`0.62√f'c < f_t ≤ 1.0√f'c`, transition), Class C (`f_t > 1.0√f'c`, cracked)
— prestressed two-way slabs must always be Class U with the tighter
`f_t ≤ 0.5√f'c` limit (ACI 318M-19).*

`[derived]` The class drives which serviceability route the rest of the
member design follows:

![[aci318-table-r24.5.2.1-serviceability-requirements-by-class.png]]
*Table R24.5.2.1 — serviceability design requirements by class: Class U/T
use gross-section properties and Cl 24.5.4 compressive stress limits with no
Cl 24.3 crack-control requirement; Class C uses cracked-section properties,
has no Cl 24.5.4 compressive limit, but **does** need Cl 24.3 crack control
(cracked-section `Δf_ps` analysis) exactly like a nonprestressed member
(ACI 318M-19).* `[derived]` This is the key practical consequence of the
U/T/C split: Class C members are designed much more like ordinary
reinforced concrete for crack control, while Class U/T members rely on the
tension-stress limit itself to keep cracking negligible.

`[code]` **At transfer** (before time-dependent losses): compression limited
to `0.70f'ci` at the ends of simply-supported members, `0.60f'ci` elsewhere
(Table 24.5.3.1) — the higher end-zone allowance reflects precast industry
research on anchorage-zone confinement (Cl R24.5.3.1). Tension limited to
`0.5√f'ci` at simply-supported ends, `0.25√f'ci` elsewhere (Table 24.5.3.2),
unless additional bonded reinforcement is provided to resist the full
tension-zone force at a stress of `0.6f_y` (≤ 210 MPa) (Cl 24.5.3.2.1).

`[code]` **At service loads** (Class U/T only, after all losses): compressive
stress ≤ `0.45f'c` under prestress + sustained load, ≤ `0.60f'c` under
prestress + total load (Table 24.5.4.1). `[derived]` The lower sustained-load
limit controls creep deformation under permanent load; the higher
total-load limit allows a one-third increase for transient loads, since
fatigue testing shows concrete compression is not the governing failure mode
under repeated transient loading (Cl R24.5.4.1) — in practice, whichever
load combination has sustained load as a larger fraction of total service
load tends to be governed by the `0.45f'c` limit instead.

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-sectional-strength-flexure-and-axial]] — Cl 22.2, the strain
  compatibility/stress-block assumptions `M_cr` and cracked-section analysis
  build on.
- [[aci318-one-way-slab-design]], [[aci318-two-way-slab-design-basis]] —
  Chapters 7–8, which invoke this page's Cl 24.2 deflection limits and
  Cl 24.3/24.4 crack-control/shrinkage-temperature provisions.
- [[concrete-beam-deflection]], [[concrete-beam-crack-control]] — the AS 3600
  equivalents, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 24 (Cl 24.1–24.5, pp. 455–466),
  incl. Tables 24.2.2, 24.2.3.5, 24.2.4.1.3, 24.3.2, 24.5.2.1, R24.5.2.1,
  24.5.3.1, 24.5.3.2, 24.5.4.1.
