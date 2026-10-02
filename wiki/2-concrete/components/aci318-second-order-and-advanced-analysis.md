---
title: ACI 318M-19 section properties, moment redistribution, second-order/inelastic/finite element analysis
category: 2-concrete
tags: [aci, second-order-analysis, inelastic-analysis, finite-element-analysis, moment-redistribution]
standards: [ACI 318M-19 Cl 6.6.3, ACI 318M-19 Cl 6.6.5, ACI 318M-19 Cl 6.7, ACI 318M-19 Cl 6.8, ACI 318M-19 Cl 6.9]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 second-order and advanced analysis

> Scope: ACI 318M-19 Cl 6.6.3 (section properties for factored-load and
> service-load elastic analysis), Cl 6.6.5 (moment redistribution), Cl 6.7
> (linear elastic second-order analysis), Cl 6.8 (inelastic analysis), and
> Cl 6.9 (finite element analysis). This is an **ACI 318M-19 page, kept
> separate from the AS 3600:2018 concept pages** elsewhere in `2-concrete` —
> see [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Every elastic analysis method in Chapter 6 — first-order
(Cl 6.6), second-order (Cl 6.7) — uses reduced "cracked" section properties
rather than gross section properties, to approximate real stiffness near
ultimate load. Inelastic analysis (Cl 6.8) and finite element analysis
(Cl 6.9) instead model material nonlinearity directly. Moment redistribution
(Cl 6.6.5) lets the designer shift elastic-analysis moments between sections
within limits tied to section ductility.

## Detail

### Section properties for factored-load analysis (Cl 6.6.3.1)

![[aci318-table-6.6.3.1.1a-moment-of-inertia-factored-load.png]]
*Table 6.6.3.1.1(a) — moment of inertia and cross-sectional areas for
elastic analysis at factored load: columns `0.70I_g`; walls `0.70I_g`
(uncracked) or `0.35I_g` (cracked); beams `0.35I_g`; flat plates/flat slabs
`0.25I_g`; axial-deformation area `1.0A_g`; shear-deformation area `b_w h`
(ACI 318M-19).* `[derived]` These `I` values already embed a stiffness
reduction factor `φ_K = 0.875` (e.g. columns: `0.875 × 0.80I_g = 0.70I_g`,
Cl R6.6.3.1.1) — distinct from both the Chapter 21 strength `φ` and the
`φ_K = 0.75` used explicitly in the nonsway moment magnifier denominator
(see [[aci318-column-slenderness-and-moment-magnification]]). If sustained
lateral load is present, column/wall `I` is further divided by `(1 + β_ds)`
(`β_ds` = ratio of max. factored sustained shear to max. factored shear in
the story, same combination) (Cl 6.6.3.1.1).

`[code]` An **alternative**, more refined set of `I` expressions is given in
Table 6.6.3.1.1(b) — accounting explicitly for axial load, eccentricity,
reinforcement ratio and `f'c` (Khuntia and Ghosh 2004), bounded between a
stated minimum and `0.875I_g`/`0.5I_g` maximum (Cl 6.6.3.1.1). `[derived]`
Not reproduced here given its narrower use (a refinement, not the default) —
see Table 6.6.3.1.1(b) in the source.

`[code]` For **lateral load analysis specifically**, a simpler blanket
`I = 0.5I_g` for all members is permitted, or a more detailed effective-
stiffness calculation (Cl 6.6.3.1.2). Two-way slab systems without beams,
when part of the seismic-force-resisting system, need a slab-member
stiffness model shown to substantially agree with comprehensive test/
analysis results — other frame members still follow Cl 6.6.3.1.1/6.6.3.1.2
(Cl 6.6.3.1.3).

### Section properties for service-load analysis (Cl 6.6.3.2)

`[code]` Immediate/time-dependent deflections under gravity load follow
Chapter 24 directly (Cl 6.6.3.2.1, see
[[aci318-serviceability-deflection-and-cracking]]). For **lateral**
deflections at service load, `I` may instead be taken as **1.4×** the
Cl 6.6.3.1 factored-load value, capped at `I_g` (Cl 6.6.3.2.2) — `[derived]`
`1.0/0.70 = 1.4` recovers an estimate of actual cracking at service-load
levels (lower than the more-cracked factored-load state), absent a more
accurate direct estimate (Cl R6.6.3.2.2).

### Moment redistribution (Cl 6.6.5)

`[code]` Except where Cl 6.5 approximate moments, Cl 6.8 inelastic-analysis
moments, or Cl 6.4.3.3 two-way pattern-loading moments are used, elastic-
theory moments at maximum-moment sections may be redistributed for any
assumed loading arrangement if: (a) the flexural member is continuous, and
(b) net tensile strain `ε_t ≥ 0.0075` at the section being reduced
(Cl 6.6.5.1). Redistribution at that section is capped at the **lesser of
`1000ε_t` percent and 20%** (Cl 6.6.5.3):

![[aci318-fig-r6.6.5-permissible-moment-redistribution.png]]
*Fig. R6.6.5 — permissible redistribution vs `ε_t`: the green line is the
Cl 6.6.5.3 permissible limit; the blue lines are calculated percentages
available for Grade 420 and Grade 550 reinforcement (`ℓ/d = 23`, `b/d =
1/5`) — the permissible limit sits conservatively below both (ACI 318M-19).*

`[code]` For prestressed members, moments include those from reactions
induced by prestressing (secondary moments) (Cl 6.6.5.2). The reduced
moment must then be used to recalculate redistributed moments at **every**
other section within the span, maintaining static equilibrium for each
loading arrangement (Cl 6.6.5.4); shears and reactions follow from that same
equilibrium with the redistributed moments (Cl 6.6.5.5). `[derived]` The
net effect, in practice, narrows the envelope of maximum positive and
negative moment at a section by trading some of each against the other —
economies in reinforcement are possible because negative moments typically
govern under one loading pattern and positive moments under another
(Cl R6.6.5). Redistribution is explicitly **not** appropriate on top of
approximate (Cl 6.5), inelastic (Cl 6.8), or two-way-pattern-loaded
(Cl 6.4.3.3) moments — each of those already has its own, different
built-in conservatism or explicit nonlinear accounting (Cl R6.6.5).

### Linear elastic second-order analysis (Cl 6.7)

`[code]` Must consider axial load influence, cracked-region effects along
the member, and load-duration effects — satisfied via the Cl 6.7.2 section
properties (same as Cl 6.6.3.1 for factored load, Cl 6.6.3.2/Chapter 24 for
service load) (Cl 6.7.1.1, Cl 6.7.2). Slenderness effects **along** a
column's length may still be calculated via the Cl 6.6.4.5 nonsway moment
magnifier, using member-end moments from the second-order analysis as input
(Cl 6.7.1.2) — `[derived]` the second-order analysis itself already accounts
for relative displacement between member ends, so this only layers in
within-length (not end-to-end) slenderness. Member dimensions must stay
within 10% of specified values, as elsewhere (Cl 6.7.1.3); redistribution
per Cl 6.6.5 remains permitted (Cl 6.7.1.4).

`[derived]` The conceptual difference from first-order analysis: a
second-order analysis solves equilibrium on the **deformed** geometry
directly (capturing P-Δ without a separate magnifier), whereas first-order
analysis solves on the **undeformed** geometry and estimates P-Δ afterward
by magnifying sway moments via Eq. 6.6.4.6.2a/b (Cl R6.7.1).

### Inelastic analysis (Cl 6.8)

`[code]` Must represent nonlinear material stress-strain response, satisfy
deformation compatibility, and satisfy equilibrium — on the undeformed
configuration for first-order inelastic analysis, or the deformed
configuration for second-order inelastic analysis (Cl 6.8.1.1). The
procedure used must be shown to produce strength/deformation results in
**substantial agreement** with physical test results of components,
subassemblages or systems exhibiting comparable response mechanisms
(Cl 6.8.1.2). `[derived]` "Substantial agreement" is deliberately open —
what counts as a characteristic comparison point depends on the analysis's
purpose: service-level-only checks need agreement below reinforcement
yield; design/assessment under design-level loading needs agreement through
yield and the onset of strength loss too, unless the design loading doesn't
reach that range (Cl R6.8.1.2). Slenderness along a column length may still
use Cl 6.6.4.5 (Cl 6.8.1.3); the 10%-dimension-tolerance rule applies again
(Cl 6.8.1.4); and — unlike elastic analysis — **redistribution is not
permitted** on inelastic-analysis moments (Cl 6.8.1.5), since the inelastic
response (and any resulting redistribution) is already explicit in the
analysis itself (Cl R6.8.1.5).

### Finite element analysis (Cl 6.9)

`[code]` Explicitly permitted to determine load effects (Cl 6.9.1), provided
the model is appropriate for its intended purpose (Cl 6.9.2) — `[derived]`
left deliberately non-prescriptive on software, element type and mesh
choice, placing responsibility on the licensed design professional to
justify the model (element types capable of the required response, mesh
fine enough to resolve it, any reasonable set of member-stiffness
assumptions) (Cl R6.9.2). For an **inelastic** finite element analysis,
**linear superposition does not apply** — a separate full inelastic analysis
must be run for each factored load combination, rather than analysing at
service load and combining results afterward with load factors (Cl 6.9.3,
Cl R6.9.3). The licensed design professional must confirm results are fit
for purpose (Cl 6.9.4); the 10%-dimension-tolerance rule applies again
(Cl 6.9.5); and, as with Cl 6.8, **redistribution is not permitted** on
finite-element-analysis moments (Cl 6.9.6).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-structural-analysis-methods]] — Cl 6.1–6.5, the method menu this
  page's remaining methods belong to.
- [[aci318-column-slenderness-and-moment-magnification]] — Cl 6.2.5/6.6.4,
  the moment magnifier method and `φ_K` stiffness reduction factors this
  page's section properties feed into.
- [[aci318-serviceability-deflection-and-cracking]] — Chapter 24, the
  deflection calculation this page's service-load section properties
  support.
- [[concrete-elastic-analysis-methods]], [[concrete-nonlinear-analysis-methods]]
  — the AS 3600 equivalents, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 6 Cl 6.6.3, 6.6.5, 6.7–6.9
  (pp. 76–87), incl. Table 6.6.3.1.1(a) and Fig. R6.6.5.
