---
title: ACI 318M-19 structural analysis — method menu, modeling assumptions, T-beam flange, simplified method
category: 2-concrete
tags: [aci, structural-analysis, modeling, t-beam, simplified-method]
standards: [ACI 318M-19 Cl 6.1, ACI 318M-19 Cl 6.2, ACI 318M-19 Cl 6.3, ACI 318M-19 Cl 6.4, ACI 318M-19 Cl 6.5]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 structural analysis methods

> Scope: ACI 318M-19 Cl 6.1–6.5 — the five permitted analysis methods menu,
> general modelling assumptions (stiffness, T-beam effective flange width),
> live load arrangement/pattern loading, and the simplified method of
> analysis for nonprestressed continuous beams and one-way slabs
> (Tables 6.5.2/6.5.4). Column slenderness and the moment magnifier method
> are covered on [[aci318-column-slenderness-and-moment-magnification]];
> section properties for factored/service analysis, moment redistribution,
> second-order, inelastic and finite element analysis are covered on
> [[aci318-second-order-and-advanced-analysis]]. This is an **ACI 318M-19
> page, kept separate from the AS 3600:2018 concept pages** elsewhere in
> `2-concrete` — see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Chapter 6 covers methods of analysis, member/system modelling, and
load-effect calculation (Cl 6.1.1). Five analysis methods are permitted
(Cl 6.2.3): (a) the simplified method for continuous beams/one-way slabs
under gravity load (Cl 6.5); (b) linear elastic first-order analysis
(Cl 6.6); (c) linear elastic second-order analysis (Cl 6.7); (d) inelastic
analysis (Cl 6.8); (e) finite element analysis (Cl 6.9) — the last
introduced explicitly in the 2014 Code to recognise an already-widespread
method (Cl R6.2.3).

## Detail

### Additional analysis methods and general requirements (Cl 6.2.1–6.2.4)

`[code]` Beyond the Cl 6.2.3 menu, four further analysis routes are
explicitly permitted (Cl 6.2.4): two-way slabs for gravity load may use the
direct design method (nonprestressed only) or the equivalent frame method
(nonprestressed and prestressed) (Cl 6.2.4.1) — `[derived]` these two
methods were themselves *removed* from the main body of the Code in 2014
(considered merely two of several available two-way slab analysis methods)
but remain explicitly permitted by cross-reference to the 2014 Code's own
text (Cl R6.2.4.1); slender walls may use the Cl 11.8 out-of-plane method
(Cl 6.2.4.2); diaphragms may use Cl 12.4.2 (Cl 6.2.4.3); and any member or
region may use the strut-and-tie method of Chapter 23 (Cl 6.2.4.4, see
[[aci318-strut-and-tie-method]]).

`[code]` All members/systems must be analysed for maximum load effects,
including live load arrangements per Cl 6.4 (Cl 6.2.2); analysis assumptions
must be consistent throughout a given analysis (Cl 6.3.1.1).

### Modelling assumptions (Cl 6.3)

`[code]` For gravity-load moments/shears in columns, beams and slabs, a
model may be limited to the members at the level under consideration plus
the columns immediately above/below, with far column ends built integrally
with the structure assumed fixed (Cl 6.3.1.2). Cross-sectional variation
(e.g. haunches) must be reflected in the model (Cl 6.3.1.3). `[derived]` A
common simplifying assumption for braced frames is `0.5I_g` for beams and
`I_g` for columns, reflecting relative (not absolute) stiffness; sway frames
instead need a more realistic `I` estimate per Cl 6.6.3.1 if a second-order
analysis is performed (Cl R6.3.1.1). Torsional stiffness only needs
inclusion for **equilibrium torsion** (required for the structure's
equilibrium, e.g. edge beams); it is usually omitted for **compatibility
torsion**, since a beam's cracked torsional stiffness is typically a small
fraction of the flexural stiffness of members framing into it
(Cl R6.3.1.1) — see [[aci318-torsional-strength]] for the equilibrium vs
compatibility torsion distinction itself.

`[code]` **T-beam effective flange width** (Cl 6.3.2), nonprestressed,
monolithic or composite slabs:

![[aci318-table-6.3.2.1-tbeam-effective-flange-width.png]]
*Table 6.3.2.1 — effective overhanging flange width beyond the face of the
web: least of `8h`/`s_w/2`/`ℓ_n/8` per side (both sides of web), or least of
`6h`/`s_w/2`/`ℓ_n/12` (one side of web) (ACI 318M-19).* `[derived]` This
simplified the pre-2011 limit of one-quarter span to one-eighth span per
side — a change made to simplify the table with negligible design impact
(Cl R6.3.2.1). **Isolated** T-beams using the flange as added compression
area additionally need flange thickness ≥ `0.5b_w` and effective flange
width ≤ `4b_w` (Cl 6.3.2.2). Prestressed T-beams may use the same geometry,
though the Commentary notes many standard prestressed products don't
actually satisfy it and still perform satisfactorily — final flange width
is left to engineering judgement for prestressed members (Cl 6.3.2.3,
Cl R6.3.2.3).

### Arrangement of live load (Cl 6.4)

`[code]` Live load may be assumed applied only to the level under
consideration (Cl 6.4.1). **One-way slabs/beams** (Cl 6.4.2): maximum
positive `M_u` near midspan — factored `L` on the span **and alternate
spans**; maximum negative `M_u` at a support — factored `L` on **adjacent
spans only**. **Two-way slab systems** (Cl 6.4.3): factored moments must be
at least those from `L` applied simultaneously to every panel, and —
depending on which of three cases applies — may instead use: the known `L`
arrangement directly (Cl 6.4.3.1); full factored `L` on all panels
simultaneously, if `L` is variable but `≤ 0.75D` or will realistically load
all panels together (Cl 6.4.3.2); or, for every other case, a **75%**-of-
factored-`L` pattern-loading rule — positive `M_u` with 75% `L` on the panel
and alternate panels, negative `M_u` with 75% `L` on adjacent panels only
(Cl 6.4.3.3). `[derived]` The 75% factor (rather than 100%) reflects that
maximum positive and maximum negative live-load moments can't physically
occur simultaneously, and that some moment redistribution is possible before
failure — it permits local overstress under the *full* factored load if
distributed per the prescribed pattern, while still guaranteeing design
strength isn't less than that needed for full factored load on all panels
(Cl R6.4.3.3). **Consequence**: Cl 6.6.5 moment redistribution is **not**
separately permitted on top of a Cl 6.4.3.3 pattern-loading analysis — the
75% rule already *is* the redistribution allowance for two-way systems (see
[[aci318-second-order-and-advanced-analysis]]).

### Simplified method for nonprestressed continuous beams and one-way slabs (Cl 6.5)

`[code]` Permitted only where **all** of: members prismatic; loads uniformly
distributed; `L ≤ 3D`; at least two spans; and adjacent-span lengths within
20% of each other (Cl 6.5.1):

![[aci318-table-6.5.2-approximate-moments.png]]
*Table 6.5.2 — approximate `M_u` by location/condition, all in terms of
`w_u ℓ_n²`: positive moments 1/11 to 1/16 depending on end condition;
negative moments 1/9 to 1/24 depending on support type and span count
(ACI 318M-19).*

![[aci318-table-6.5.4-approximate-shears.png]]
*Table 6.5.4 — approximate `V_u`: `1.15 w_u ℓ_n/2` at the exterior face of
the first interior support (the 15% increase reflecting the higher shear
expected there), `w_u ℓ_n/2` at all other supports (ACI 318M-19).*

`[code]` Moments from Table 6.5.2 **may not be redistributed** (Cl 6.5.3) —
`[derived]` these are already approximate/conservative envelope values, not
an elastic-analysis result eligible for the Cl 6.6.5 redistribution
procedure. `ℓ_n` for negative-moment locations is the **average** of the two
adjacent clear spans (Table 6.5.2 note). Floor/roof-level column moments
from this method must still be distributed between the columns above and
below in proportion to relative column stiffness (Cl 6.5.5) — `[derived]`
this exists specifically to make sure *some* moment reaches the columns,
since the critical load patterns for column moments differ from those
producing the Table 6.5.2 beam moments (Cl R6.5.5).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-loads-and-load-combinations]] — Chapter 5, the factored loads fed
  into every method on this page.
- [[aci318-column-slenderness-and-moment-magnification]] — Cl 6.2.5/6.6.4,
  slenderness-effects screening and the moment magnifier method.
- [[aci318-second-order-and-advanced-analysis]] — Cl 6.6.3, 6.6.5, 6.7–6.9,
  section properties, moment redistribution, second-order/inelastic/FE
  analysis.
- [[aci318-two-way-slab-design-basis]] — Cl 8.2.1, where DDM/EFM are named
  as permitted two-way slab analysis methods without being given a
  step-by-step procedure in Chapter 8 itself — this page's Cl 6.2.4.1 records
  why.
- [[concrete-simplified-flexural-analysis]], [[concrete-structural-analysis-overview]]
  — the AS 3600 equivalents, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 6 Cl 6.1–6.5 (pp. 67–75), incl.
  Tables 6.3.2.1, 6.5.2, 6.5.4.
