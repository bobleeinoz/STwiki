---
title: Fatigue design — S-N curves, capacity factors, exemption and assessment
category: 0-standards
tags: [fatigue, sn-curve, stress-range, constant-amplitude, variable-amplitude, thickness-correction, cranes, miners-rule]
standards: [AS 4100:2020 Section 11]
status: draft
reviewed: 2026-09-13
---

# Fatigue design

> Scope: AS 4100:2020 Section 11 — scope/exclusions, capacity factor
> philosophy for fatigue, thickness correction, fatigue loading sources
> (crane/bridge Standards), design stress spectrum (incl. hollow-section
> truss multiplying factors), exemption from assessment, S-N curves for
> normal and shear stress (Figures 11.6.1/11.6.2), constant/variable
> amplitude assessment (Miner's-rule-based), punching limitation. Detail
> category tables are on [[as4100-fatigue-detail-categories]].

## Summary

`[code]` Fatigue assessment verifies, at every point, that the design
stress range `f*` stays within the detail category's `n_sc`-cycle
capacity, `φ` applied. Two-part S-N curve: slope `α_s = 3` for
`n_sc ≤ 5×10⁶` (constant-amplitude fatigue limit `f_3`), slope `α_s = 5`
for `5×10⁶ < n_sc ≤ 10⁸` (cut-off limit `f_5` at `10⁸` cycles); beyond
`10⁸` cycles, no further damage is assumed.

`[code]` `φ = 1.0` for the "reference design condition" (redundant load
path, conventional stress-history estimate, cycles not highly irregular,
detail accessible for regular inspection); reduced otherwise, and
`φ ≤ 0.70` for **non-redundant load paths** (Cl 11.1.5).

## Detail

### Scope and exclusions (Cl 11.1.1)

`[code]` Applies to structures/elements subject to loading that could cause
fatigue. **Not covered**: (a) fatigue-life reduction from corrosion or
immersion; (b) high-stress low-cycle fatigue; (c) thermal fatigue; (d)
stress corrosion cracking. Design must verify Section 11 requirements at
every point for the structure's design life, **and** still satisfy the
strength and serviceability limit states.

### Notation highlights (Cl 11.1.2)

`[code]` `f_c` = thickness-corrected fatigue strength; `f_f` = uncorrected
fatigue strength; `f_rn`, `f_rs` = detail-category reference fatigue
strength at `n_r` (normal / shear); `f_3` = category strength at the
constant-amplitude fatigue limit (5×10⁶ cycles); `f_5` = category strength
at the cut-off limit (10⁸ cycles); `f*` = design stress range; `f*_i` =
design stress range for loading event `i`; `n_i` = cycles of loading event
`i`; `n_r` = reference cycles (2×10⁶); `n_sc` = number of stress cycles;
`α_s` = inverse slope of the S-N curve.

### Limitation (Cl 11.1.3)

`[code]` In all stress cycles, the design stress magnitude must not exceed
`f_y`, and the stress **range** must not exceed `1.5 f_y`.

### Designation of weld category (Cl 11.1.4)

`[code]` Welds in details of Table 11.5.1(B)/(D) for **Detail Category 112
and below** must be **SP** category per AS/NZS 1554.1 or 1554.4. Welds in
Table 11.5.1(B) for **Detail Category 125** need the higher quality of
AS/NZS 1554.5.

### Method — capacity factor (Cl 11.1.5)

`[code]` `φ = 1.0` for the "reference design condition": (a) detail on a
redundant load path, where local failure alone would not cause overall
collapse; (b) stress history estimated by conventional methods; (c) load
cycles not highly irregular; (d) detail accessible for, and subject to,
regular inspection. `φ` is **reduced** when any condition fails to hold,
and **for non-redundant load paths, `φ ≤ 0.70`**.

`[derived]` This makes fatigue the one AS 4100 limit state where `φ` is a
judgement call rather than a table lookup — a crane runway girder
(inaccessible weld root, non-redundant single girder under one rail) should
be assessed with a materially lower `φ` than a redundant, inspectable truss
chord, even for the identical detail category.

### Thickness effect (Cl 11.1.6)

`[code]` `β_tf = 1.0`, except for a **transverse** fillet or butt weld with
plate thickness `t_p > 25 mm`:

`β_tf = (25/t_p)^0.25`

Apply to correct every strength value: `f_c = β_tf f_f`; `f_rnc = β_tf
f_rn`; `f_rsc = β_tf f_rs`; `f_3c = β_tf f_3`; `f_5c = β_tf f_5`.

### Fatigue loading (Cl 11.2)

`[code]` From the referring Standard where applicable: **AS 1418.1**
(cranes/hoists/winches — general), **AS 1418.3** (bridge, gantry, portal
incl. container cranes, and jib cranes), **AS 1418.5** (mobile cranes),
**AS 1418.18** (crane runways and monorails), **AS 5100.1/5100.2**
(bridges). Otherwise, use the actual service loading including dynamic
effects.

`[derived]` For mining/material-handling structures this is the key
pointer: conveyor drive/take-up structures, stacker/reclaimer rail
structures, crane runway beams under overhead travelling cranes, and
vibrating-equipment supports (screens, crushers) all route their fatigue
loading through AS 1418 (cranes) or the equipment manufacturer's actual
duty cycle — AS 4100 itself supplies no load magnitudes, only the
resistance side.

### Design spectrum (Cl 11.3)

`[code]` Stress determination (11.3.1): design stresses from an elastic
analysis or from measured strain-gauge stress history; normal or shear
stress including all design actions but **excluding** the detail's own
geometric stress concentration (already built into the detail category);
stress concentrations *not* characteristic of the detail are accounted for
separately. Table 11.5.1 arrows show the plane and location for the stress
range. For non-pinned open-section truss connections, secondary bending
moments must be included **unless** `l/d_x > 40` or `l/d_y > 40`.

`[code]` **Hollow-section truss connections**: stress range may be
calculated ignoring connection stiffness/eccentricity, subject to: (a)
CHS connections — multiply by Table 11.3.1(A); (b) RHS connections —
multiply by Table 11.3.1(B); (c) fillet weld design throat thickness >
connected member wall thickness.

`[code]` Table 11.3.1(A) — CHS multiplying factors:

| Connection | Chords | Verticals | Diagonals |
|---|---|---|---|
| Gap, K type | 1.5 | 1.0 | 1.3 |
| Gap, N type | 1.5 | 1.8 | 1.4 |
| Overlap, K type | 1.5 | 1.0 | 1.2 |
| Overlap, N type | 1.5 | 1.65 | 1.25 |

`[code]` Table 11.3.1(B) — RHS multiplying factors:

| Connection | Chords | Verticals | Diagonals |
|---|---|---|---|
| Gap, K type | 1.5 | 1.0 | 1.5 |
| Gap, N type | 1.5 | 2.2 | 1.6 |
| Overlap, K type | 1.5 | 1.0 | 1.3 |
| Overlap, N type | 1.5 | 2.0 | 1.4 |

`[code]` Design spectrum calculation (11.3.2): for irregular stress cycles,
obtain the spectrum by a rational stress-cycle-counting method — rainflow
counting or equivalent.

### Exemption from assessment (Cl 11.4)

`[code]` No fatigue assessment is needed at a point if either:

`f* < φ × 27 MPa`

or the number of stress cycles satisfies:

`n_sc < 2×10⁶ (φ×36 / f*)³`

### Fatigue strength — normal stress (Cl 11.6.1, Figure 11.6.1)

`[code]` Two-part S-N law:

`f_f³ = f_rn³ × 2×10⁶ / n_sc` when `n_sc ≤ 5×10⁶` (slope `α_s = 3`)

`f_f⁵ = f_5⁵ × 10⁸ / n_sc` when `5×10⁶ < n_sc ≤ 10⁸` (slope `α_s = 5`)

![[as4100-fig-11.6.1-SN-curve-normal-stress.png]]
*Figure 11.6.1 — S-N curve for normal stress: uncorrected fatigue strength f_f vs number of stress cycles n_sc, one line per detail category f_rn (160 down to 36), with the constant-stress-range fatigue limit f_3 at 5×10⁶ cycles and cut-off limit f_5 at 10⁸ cycles (AS 4100:2020).*

`[derived]` Reading the chart: `f_3` values (at 5×10⁶ cycles) run from 133
(category 160) down to 27 (category 36); `f_5` (cut-off, 10⁸ cycles) runs
from 73 down to 15. These are the numeric values used directly in the
Cl 11.7 exemption and Cl 11.8 assessment formulae — read them off the chart
or compute via the two S-N equations above for a category not tabulated
elsewhere.

### Fatigue strength — shear stress (Cl 11.6.2, Figure 11.6.2)

`[code]` Single-slope law over the full range:

`f_f⁵ = f_rs⁵ × 2×10⁶ / n_sc` when `n_sc ≤ 10⁸` (slope `α_s = 5` throughout)

![[as4100-fig-11.6.2-SN-curve-shear-stress.png]]
*Figure 11.6.2 — S-N curve for shear stress: two detail categories only (100, 80), single slope α_s = 5, cut-off limit f_5 at 10⁸ cycles (46 and 37 respectively) (AS 4100:2020).*

### Exemption from further assessment (Cl 11.7)

`[code]` At any point where the design stress range `f* < φf_3c` for **all**
normal stress ranges, no further assessment is required at that point.

### Fatigue assessment (Cl 11.8)

`[code]` **Constant stress range** (11.8.1): `f*/(φf_c) ≤ 1.0`.

`[code]` **Variable stress range** (11.8.2) — a Miner's-rule-style
cumulative damage check:

Normal stresses:

`Σᵢ nᵢ(f*ᵢ)³ / [5×10⁶(φf_3c)³] + Σⱼ nⱼ(f*ⱼ)⁵ / [5×10⁶(φf_3c)⁵] ≤ 1.0`

Shear stresses:

`Σₖ nₖ(f*ₖ)⁵ / [2×10⁶(φf_rsc)⁵] ≤ 1.0`

- Sum `i`: design stress ranges `f*ᵢ` with `φf_3c ≤ f*ᵢ` (above the
  constant-amplitude limit — use the `α_s=3` slope).
- Sum `j`: design stress ranges `f*ⱼ` with `φf_5c ≤ f*ⱼ < φf_3c` (between
  cut-off and constant-amplitude limits — use the `α_s=5` slope).
- Sum `k`: shear design stress ranges `f*ₖ` with `φf_5c ≤ f*ₖ` (shear uses
  the single `α_s=5` slope throughout, per Cl 11.6.2).
- Stress ranges **below** `φf_5c` contribute no damage and are excluded
  from every sum.

### Punching limitation (Cl 11.9)

`[code]` For members/connections requiring fatigue assessment, a **punched
hole** is only permitted in material ≤ **12.0 mm** thick (thicker material
must be drilled, or punched-and-reamed, per fabrication practice — punching
alone leaves a cold-worked, crack-initiation-prone hole edge in thicker
material).

## Worked reference

`[derived]` Illustrative exemption check: a bracket detail category 71
(`f_3c ≈ 45` from the chart at `β_tf=1`), `φ = 0.85` (redundant, but
inspection access is only occasional): `φf_3c ≈ 38 MPa`. If the actual
design stress range `f* = 25 MPa`, since `25 < φ×27 = 23`... this fails the
`f* < φ×27` test (25 > 23), so check the cycle-count exemption instead: if
service life gives `n_sc = 500,000` cycles, test
`n_sc < 2×10⁶(φ×36/f*)³ = 2×10⁶(0.85×36/25)³ = 2×10⁶×1.5³ ≈ 6.8×10⁶` — since
500,000 < 6.8×10⁶, the detail is **exempt** from further assessment despite
failing the simple stress-range test. Illustrative only — always compute
both Cl 11.4 tests before concluding a detail needs full Cl 11.8
assessment.

## Contradictions

None recorded.

## Related

- [[as4100-fatigue-detail-categories]] — the `f_rn`/`f_rs` detail-category
  lookup tables consumed by every formula here.
- [[as4100-weld-design]] — weld quality/geometry (SP/GP, throat) that
  Cl 11.1.4 and the detail categories build on.
- [[as4100-limit-state-design-basis]] — Cl 3.9 routing to this Section.
- [[as4100-brittle-fracture-material-selection]] — a related but distinct
  low-temperature failure mode that can compound with fatigue cracking.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Cl 11.1–11.4, 11.6–11.9
  (pp. 145–149, 159–161). Figures 11.6.1, 11.6.2 reproduced in
  `wiki/0-standards/assets/`.
