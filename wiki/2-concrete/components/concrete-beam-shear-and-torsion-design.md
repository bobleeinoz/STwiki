---
title: Strength of beams in shear and torsion
category: 2-concrete
tags: [beams, shear, torsion, mcft]
standards: [AS 3600:2018 Cl 8.2]
status: draft
reviewed: 2026-09-12
---

# Strength of beams in shear and torsion

> Scope: AS 3600 Cl 8.2 — the modified-compression-field-theory (MCFT) based
> shear and torsion design method for reinforced and prestressed beams under
> any combination of torsion, flexure, shear and axial load. Does not apply
> to non-flexural members (Sections 7, 12).

## Summary

`[code]` This is the densest clause in Section 8, and its core variables
(`kv`, `θv`, `εx` — the concrete strut angle and the longitudinal strain that
drives it) recur through nearly every sub-clause. `[derived]` **Caveat on
this page**: the source PDF's text extraction badly mangled Greek symbols and
subscripts throughout this clause (a known OCR limitation, not a content
choice). The formula *structures* and governing variables below are restated
with reasonable confidence from the extracted text and general knowledge of
AS 3600:2018 Amendment 2's MCFT shear provisions, but **every specific
numeric coefficient on this page should be checked against Cl 8.2 directly**
before being used in an actual calculation — this page is a map of the
method, not a substitute for the clause text.

## Detail

### General requirements (Cl 8.2.1)

`[code]` Torsion may be disregarded (with only minimum torsion reinforcement
per Cl 8.2.5.5 and detailing per Cl 8.3.3) where it isn't needed for
equilibrium and arises only from restrained rotation of adjoining members,
**provided** the torsional moment stays below a threshold fraction (25%) of
the cracking torque `Tcr` — `Tcr` itself is a function of `f'c`, the gross
section's enclosed area and perimeter, and average prestress at the
centroid. Box sections cap a geometric term in the `Tcr` formula at a value
tied to the shear-flow-path area.

`[code]` **Vertical component of prestress** (Cl 8.2.1.3): a load factor
`ψp` applies to the factored vertical prestress component `Pv` — one value
where `Pv` reduces the shear demand (favourable), a different, larger value
where it increases shear demand (unfavourable) — the same asymmetric-bounding
logic seen elsewhere in the standard (see e.g.
[[concrete-limit-state-design-basis]] prestress-at-transfer combinations).

`[code]` **Effective web width** `bv` (Cl 8.2.1.5): minimum web width within
the effective shear depth, reduced for prestressing ducts present in that
plane — the reduction factor differs for grouted steel duct, grouted plastic
duct, and ungrouted duct (ungrouted ducts cost more effective width, since
there's no bond to help transfer shear across the duct). Solid circular
sections may take `bv` as the section diameter.

`[code]` **Transverse shear reinforcement is required** (Cl 8.2.1.6) wherever
the design shear exceeds a reduced concrete-only capacity (the reduction
factor `ks` depends on overall depth `D`: full concrete contribution allowed
below 300 mm, a sliding scale from 300–650 mm, half credit above 650 mm —
unless rational calculation shows a local shear failure wouldn't cause
structural collapse, in which case `ks = 1.0` regardless), wherever torsion
exceeds the same 25%-of-`Tcr` threshold as Cl 8.2.1.2, or wherever overall
depth exceeds 750 mm regardless of demand.

`[code]` **Minimum transverse shear reinforcement** (Cl 8.2.1.7): a minimum
`Asv/s` ratio scaled by `√f'c`, web width and fitment yield strength.
**Effective shear depth** `dv`: the greater of a fraction of overall depth
`D` or a fraction of effective depth `d` to the tension-reinforcement
centroid.

### Design method selection (Cl 8.2.2)

`[code]` Flexural regions (plane-sections-remain-plane valid): sectional
model (Cl 8.2.3, below) or strut-and-tie (Section 7). Regions near
discontinuities (plane-sections assumption invalid): strut-and-tie only, with
Cl 12.2 non-flexural-member provisions applying — see
[[concrete-strut-and-tie-modelling]]. Interface regions: shear-friction design
per Cl 8.4 — see [[concrete-beam-longitudinal-shear-composite]]. A detailed
equilibrium/compatibility analysis using actual cracked-concrete and
reinforcement stress-strain relationships is permitted in lieu of any of the
above.

### Sectional design (Cl 8.2.3)

`[code]` Design shear strength check: `φ·Vu ≥ V* − ψp·Pv`, where
`Vu = Vuc + Vus` (concrete contribution + reinforcement contribution, Cl
8.2.4/8.2.5). Design torsional strength check: `φ·Tus ≥ T*`. Both checks
also require satisfying a web-crushing limit (below). `φ` values come from
Table 2.2.2 (see [[concrete-strength-check-procedures]]); shear and torsion
reinforcement demands are additive (Cl 8.2.5.3).

`[code]` Maximum shear near a support may be taken at the support face, or —
where the member is directly supported and diagonal cracking can't extend
into the support, with reinforcement continued unchanged to the face — at a
distance `dv` from the face. Members with the zero-shear point closer than
`2dv` to a support face, or with a near-support concentrated load
contributing >50% of the support shear, are treated as **deep** components
under Section 12 instead of this clause — see
[[concrete-non-flexural-members-and-strut-tie-models]].

`[code]` **Web crushing** (Cl 8.2.3.3): shear+torsion strength is separately
capped by a web-crushing shear force `Vu.max`, a function of `f'c`, `bv`,
`dv` and the strut angle `θv` (a different, more conservative form applies
at transfer using `f'cp`). Box sections check wall thickness against a
geometric threshold to decide which of two combined-action interaction
formulas governs; other sections use a single combined shear-and-torsion
interaction check against `Vu.max`.

### Concrete contribution `Vuc` (Cl 8.2.4)

`[code]` General form: `Vuc = kv·bv·dv·√f'c` (with `√f'c` capped at 8.0 MPa
regardless of actual strength — a ceiling on how much the concrete term can
contribute). `kv` and the strut angle `θv` come from either:

- **General method** (Cl 8.2.4.2): `θv` increases linearly with the
  longitudinal strain `εx` at mid-depth (a `29° + (coefficient)·εx` form);
  `kv` reduces as `εx` increases, via a formula split by whether
  `Asv/s ≥ Asv.min/s` and further adjusted for high-strength/lightweight
  concrete via an aggregate-size-dependent factor `kdg` (coarser aggregate →
  better aggregate interlock → less penalty). `εx` itself (Cl 8.2.4.2.2) is
  calculated from `M*`, `V*`, `N*`, prestress terms and the reinforcement/
  tendon areas in the tension half-depth, floored at zero for net-compression
  sections (or, alternatively, calculated as a small negative value within a
  stated limit using the full concrete area in tension for extra precision).
  `M*` has a floor tied to `(V* − ψp·Pv)·dv` so a nominally-zero-moment
  section still gets a sensible strain estimate. `N*` is positive for tension.
  For combined shear+torsion, a separate `εx` formula (Cl 8.2.4.2.3) folds in
  a torsion term using the shear-flow-path area `Ao`. Both `εx` formulas are
  capped at an upper limit (`3.0×10⁻³`), doubled if axial tension is large
  enough to crack the flexural compression face, and may use the value
  calculated at `dv` from the support face for sections closer than that.
- **Simplified method** (Cl 8.2.4.3): for normal-weight, non-prestressed
  components without axial tension or torsion, `f'c ≤ 65 MPa`, `fsy ≤ 500 MPa`
  and aggregate ≥10 mm — `θv` fixed at 36°, `kv` from a two-branch formula
  keyed only to whether `Asv ≥ Asv.min`.

`[code]` **Load reversal** (Cl 8.2.4.5): where cracking occurs in a zone
usually in compression, `Vuc` from the standard method may not apply —
reassess or take `Vuc = 0`.

### Reinforcement contribution `Vus` and torsional resistance (Cl 8.2.5)

`[code]` `Vus` for perpendicular shear reinforcement: `Asv·fsy.f·dv·cot(θv)/s`;
for inclined shear reinforcement, an equivalent form scaled by the
reinforcement's own angle. Where `Asv/s` changes along the member, the
transition may be assumed linear over a length equal to `D`. Torsional
resistance `Tus` uses the enclosed shear-flow-path area `Ao` (taken as
0.85×`Aoh` for solid sections) and the same `θv`.

`[code]` **Minimum torsional reinforcement** (Cl 8.2.5.5) applies wherever
torsional reinforcement is triggered by Cl 8.2.3.1, or wherever torsion is
disregarded under the Cl 8.2.1.2 exemption: longitudinal torsional steel per
Cl 8.2.7/8.2.8 (below), and transverse reinforcement at the greater of the
Cl 8.2.1.7 minimum shear requirement or a capacity equal to 25% of `Tcr`.

### Additional longitudinal tension from shear/torsion (Cl 8.2.7–8.2.8)

`[code]` Shear and torsion each induce an additional longitudinal tensile
force (`Ftds` from shear, `Ftdt` from torsion — both floored at zero), summed
to `Ftd`. This must be resisted alongside flexural and axial tension by
reinforcement/tendons proportioned per Cl 8.2.8: on the flexural **tension**
side, sized against the total tension demand (flexure + axial + the shear/
torsion increment, capped at what's needed for the section of maximum
demand); on the flexural **compression** side, only where a net tension force
still results after accounting for moment/axial/shear-torsion effects.
`[practice]` A deemed-to-comply shortcut exists for ordinary reinforced
members without axial tension/torsion and without sudden tension-force
jumps: simply extend the flexural tensile reinforcement by `dv·cot(θv)`
past where it's theoretically needed (Fig 8.2.8) — this is the practical
"detail it this way and you don't need to run the longitudinal-tension
check" route most designers use.

![[as3600-fig-8.2.8-longitudinal-tension-curtailment.png]]
*Figure 8.2.8 — deemed-to-comply extension of flexural tensile
reinforcement by `dv·cot(θv)` past the point theoretically required
(AS 3600:2018).*

### Hanging reinforcement (Cl 8.2.6)

`[code]` Loads applied away from a member's top chord must be hung up to the
top chord via reinforcement sized by strut-and-tie principles — see
[[concrete-strut-and-tie-modelling]].

## Worked reference

None yet — given the OCR caveat above, this clause is the strongest
candidate in the wiki for a human-verified worked example once one is
available, so the reconstructed formulas here can be checked against a real
calculation.

## Contradictions

None recorded.

## Related

- [[concrete-strength-check-procedures]] — φ values.
- [[concrete-strut-and-tie-modelling]] — the alternative method near
  discontinuities, and hanging-reinforcement design.
- [[concrete-beam-longitudinal-shear-composite]] — Cl 8.4 interface shear.
- [[concrete-beam-detailing]] — Cl 8.3 detailing of the reinforcement sized
  here.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clause 8.2 (Figure 8.2.8
  reproduced as an image asset above). **Note**: text
  extraction from this clause was unusually degraded (missing Greek symbols
  and subscripts) — treat numeric coefficients above as provisional pending
  direct clause verification.
