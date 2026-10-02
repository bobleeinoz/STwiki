---
title: ACI 318M-19 strut-and-tie method — struts, ties, nodal zones, D-regions
category: 2-concrete
tags: [aci, strut-and-tie, d-region, discontinuity]
standards: [ACI 318M-19 Cl 23.1, ACI 318M-19 Cl 23.2, ACI 318M-19 Cl 23.4, ACI 318M-19 Cl 23.7, ACI 318M-19 Cl 23.9]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 strut-and-tie method

> Scope: ACI 318M-19 Chapter 23 — the strut-and-tie design method for
> discontinuity (D-) regions: general modelling rules, strut strength
> (including the βs/βc effective-strength factors), minimum distributed
> reinforcement, tie strength and anchorage, nodal zone strength (βn),
> curved-bar nodes, and the seismic design addendum. This is an **ACI
> 318M-19 page, kept separate from the AS 3600:2018 concept pages**
> elsewhere in `2-concrete` — see [[aci-318m-19-building-code-concrete]] for
> why.

## Summary

`[code]` Any structural concrete member or discontinuity region may be
designed by idealising it as a pin-jointed truss of **struts** (compression
members), **ties** (tension members) and **nodes** (joints) — the strut-and-
tie method (Cl 23.1.2). It applies specifically where load or geometric
discontinuities cause a nonlinear strain distribution across the section —
**D-regions** — as opposed to **B-regions**, where ordinary plane-sections
flexural theory (Cl 9.2.1) still applies. D-regions are assumed to extend a
distance `h` (overall member depth) from the discontinuity, per St. Venant's
principle (Cl R23.1).

## Detail

### The idealised truss and its four-step process (Cl 23.1–23.2)

![[aci318-fig-r23.2.1-strut-and-tie-model-overview.png]]
*Fig. R23.2.1 — strut-and-tie model of a single-span deep beam under two
point loads: boundary struts (at the loaded/reaction nodes), an interior
strut (the inclined compression field), a tie (the bottom tension chord),
and the nodal zones at each truss joint (ACI 318M-19).*

`[code]` Design process (Cl R23.2): (1) define and isolate each D-region;
(2) calculate the resultant forces on each D-region boundary; (3) select a
truss model with strut/tie axes approximately coincident with the actual
compression/tension field axes, and solve for member forces; (4) size
struts/nodal zones for the effective concrete strengths of Cl 23.4.3/23.9.2,
and ties for the steel strength of Cl 23.7.2, anchoring reinforcement in or
beyond the nodal zones.

`[code]` Modelling rules: the truss must be able to transfer all factored
loads to supports or adjoining B-regions (Cl 23.2.3), internal forces must
equilibrate the applied loads/reactions (Cl 23.2.4), ties may cross struts
and other ties (Cl 23.2.5), but struts may only intersect or overlap at
nodes (Cl 23.2.6). The angle between any strut and tie axis entering the
same node must be **at least 25°** (Cl 23.2.7) — `[derived]` this exists to
avoid modelling incompatibilities from a strut shortening and a tie
lengthening in nearly the same direction, and specifically rules out
modelling a slender beam's shear span with struts inclined under 25° to the
longitudinal reinforcement (Cl R23.2.7).

`[code]` Prestressing effects must be included as **external loads**, with
load factors per Cl 5.3.11 — not folded invisibly into member capacities
(Cl 23.2.8). Deep beams designed by this method must still satisfy
Cl 9.9.2.1, 9.9.3.1 and 9.9.4 (Cl 23.2.9); brackets/corbels with shear
span-to-depth ratio `a_v/d < 2.0` must satisfy Cl 16.5.2, 16.5.6 and provide
closed stirrups/ties with `A_sc ≥ 0.04(f'c/f_y) b_w d` (Eq. 23.2.10). Shear
friction (Cl 22.9, see [[aci318-bearing-and-shear-friction]]) still applies at
any crack/interface plane within or adjoining a strut-and-tie region
(Cl 23.2.11).

### Node classification and nodal zone geometry

`[code]` Nodes are classified by the sign of the forces meeting there — at
least three forces should act on every node for equilibrium (Cl R23.2.6):

![[aci318-fig-r23.2.6c-node-classification.png]]
*Fig. R23.2.6c — node classification: C-C-C (three compressive forces),
C-C-T (two compression, one tension), C-T-T (one compression, two tension)
(ACI 318M-19).*

`[derived]` A **hydrostatic** nodal zone has equal stress on every loaded
face (faces perpendicular to each strut/tie axis) — for a C-C-C node this
means the nodal-zone side lengths are proportional to the three strut
forces; a C-C-T node can be treated as hydrostatic if the tie is assumed to
extend through the node, anchored by a plate sized so its bearing stress
matches the strut stress (Cl R23.2.6). Where more than three forces act on
a 2D nodal zone, some are first resolved into a single equivalent force
before applying the hydrostatic idealisation (Fig. R23.2.2, Cl R23.2.2).

### Strength of struts (Cl 23.3–23.4)

`[code]` Every strut, tie and nodal zone must satisfy `φF_n ≥ F_u`
(Cl 23.3.1), with φ per Chapter 21 (Cl 23.3.2 — see
[[aci318-strength-reduction-factors]]). Nominal strut strength:

**F_ns = f_ce A_cs**  (no longitudinal reinforcement, Eq. 23.4.1a)
**F_ns = f_ce A_cs + A_s′ f_s′**  (with longitudinal compression
reinforcement, Eq. 23.4.1b, evaluated at each end and the lesser taken)

`[code]` Effective concrete strength in the strut:

**f_ce = 0.85 β_c β_s f'c**  (Eq. 23.4.3)

![[aci318-table-23.4.3ab-strut-coefficients.png]]
*Table 23.4.3(a) — strut coefficient `β_s`: 0.4 for any strut in a tension
member/zone, 1.0 for boundary struts, 0.75 for interior struts meeting
Table 23.5.1 reinforcement (or Cl 23.4.4, or in beam-column joints), else
0.4. Table 23.4.3(b) — strut/node confinement factor `β_c`: up to 2.0 where
the strut end or node includes a bearing surface, via `√(A₂/A₁)` (same
frustum-confinement logic as bearing strength, Cl 22.8.3 — see
[[aci318-bearing-and-shear-friction]]) (ACI 318M-19).*

`[derived]` Boundary struts get the maximum `β_s = 1.0` because they are not
subject to transverse tension (comparable to a beam/column compression-zone
stress block); interior struts default to the lowest `β_s = 0.4` **unless**
one of three conditions is met — Table 23.5.1 distributed reinforcement is
provided, a diagonal-tension check (Eq. 23.4.4, same form as the one-way
shear size limit) is satisfied, or the strut is a beam-column joint strut —
each of which independently justifies raising `β_s` to 0.75 (Cl R23.4.3).
The lowest `β_s = 0.4` for struts in a tension member/zone exists because
those struts must transfer compression across a region where perpendicular
tensile stress is also acting, reducing their effective strength
(Cl R23.4.3).

`[code]` Where `β_s = 0.75` is justified via Cl 23.4.4 (line (d) of Table
23.4.3(a)), member dimensions must additionally satisfy:

**V_u ≤ 0.42 φ tan θ λ λ_s √f'c b_w d**  (Eq. 23.4.4)

using the **same** `λ_s` size-effect factor as one-way shear (Cl 22.5.5.1.3,
see [[aci318-one-way-shear-strength]]) — except here, `λ_s = 1.0` is allowed
outright if Table 23.5.1 distributed reinforcement is provided
(Cl 23.4.4.1), independent of the `A_v,min` test used for ordinary one-way
shear.

### Minimum distributed reinforcement (Cl 23.5)

`[code]` Interior struts need minimum reinforcement crossing their axis
unless laterally restrained:

![[aci318-table-23.5.1-minimum-distributed-reinforcement.png]]
*Table 23.5.1 — minimum distributed reinforcement ratio: 0.0025 in each
direction for an orthogonal grid, or `0.0025/sin²α₁` for reinforcement in a
single direction crossing the strut at angle `α₁`; none required if the
strut is laterally restrained (ACI 318M-19).* Spacing ≤ 300 mm and
`α₁ ≥ 40°` (Cl 23.5.2). "Laterally restrained" means restrained
perpendicular to the model plane — by a continuous discontinuity region, by
surrounding concrete extending at least half the strut width beyond each
side face, or by a Cl 15.2.5/15.2.6-restrained joint (Cl 23.5.3).

`[derived]` The method is a lower-bound plasticity solution — this
reinforcement exists to let internal forces redistribute as the member
cracks, to control service-load cracking, and to promote ductile rather than
brittle behaviour (Cl R23.5). Required reinforcement must be developed
beyond the strut per Cl 25.4 (Cl 23.5.4).

### Strength of ties (Cl 23.7) and anchorage (Cl 23.8)

`[code]` Nominal tie strength:

**F_nt = A_ts f_y + A_tp Δf_p**  (Eq. 23.7.2, `A_tp = 0` for nonprestressed)

`Δf_p` may be taken as 420 MPa (bonded) or 70 MPa (unbonded) prestressed
reinforcement, or higher if justified by analysis, capped at `(f_py − f_se)`
(Cl 23.7.2.1).

`[code]` The tie reinforcement's centroidal axis must coincide with the
modelled tie axis (Cl 23.8.1). Anchorage is by mechanical device,
post-tensioning anchorage, standard hook, or straight development
(Cl 23.8.2) — tie force must be fully developed at the point where the
reinforcement centroid **exits the extended nodal zone** (Cl 23.8.3), a
distance `ℓ_anc` back from the node (Cl R23.8.2). `[derived]` The effective
tie width `w_t` for design ranges from "bar diameter plus twice cover" (one
layer) up to a practical maximum set by the hydrostatic-nodal-zone width
`w_t,max = F_nt/(f_ce b_s)` — beyond the one-layer value, reinforcement
should be spread roughly uniformly over the tie's width/thickness rather
than concentrated (Cl R23.8.1).

### Strength of nodal zones (Cl 23.9)

`[code]` Nominal nodal zone strength: `F_nn = f_ce A_nz` (Eq. 23.9.1), with:

**f_ce = 0.85 β_c β_n f'c**  (Eq. 23.9.2, same `β_c` as Table 23.4.3(b))

![[aci318-table-23.9.2-nodal-zone-coefficient.png]]
*Table 23.9.2 — nodal zone coefficient `β_n`: 1.0 where bounded only by
struts/bearing areas (C-C-C), 0.80 anchoring one tie (C-C-T), 0.60 anchoring
two or more ties (C-T-T) (ACI 318M-19).* `[derived]` The declining `β_n`
reflects progressively greater disruption of the nodal zone from
incompatible tensile (tie) and compressive (strut) strains meeting at the
same joint (Cl R23.9.2) — a C-T-T node is the most compromised case.
`A_nz` is the **smaller** of the face area perpendicular to the strut force
line, or a section area perpendicular to the resultant force (Cl 23.9.4);
confining reinforcement with documented test/analysis support may justify a
higher `f_ce` (Cl 23.9.3).

### Curved-bar nodes (Cl 23.10)

`[derived]` A curved-bar node — formed by a continuous bar's bend region,
either anchoring two ties intersected by a strut, or a single tie anchored
by a 180° bend — needs a minimum bend radius `r_b` sized so the bearing
stress inside the bend does not exceed the governing nodal-zone `f_ce`
(Eq. 23.10.2a for bends < 180°, Eq. 23.10.2b for 180° bends, Cl R23.10.2),
increased further if clear cover normal to the bend plane is under `2d_b`
(Cl 23.10.3). Not detailed further here given its narrow applicability —
see Cl 23.10.1–23.10.6 and Figs. R23.10.2/R23.10.4/R23.10.5/R23.10.6 in the
source for the full geometry and the `ℓ_cb` development-of-force-difference
requirement at unequal tie forces.

### Earthquake-resistant design using strut-and-tie (Cl 23.11)

`[code]` For SDC D/E/F seismic-force-resisting-system regions designed by
this method: either follow Chapter 18 directly, or apply Cl 23.11.2–23.11.5
**and** amplify the design earthquake force `E` by an overstrength factor
`Ω_o ≥ 2.5` (unless a smaller value is justified by detailed analysis)
(Cl 23.11.1). Where the reduced-detailing route is taken: strut effective
compressive strength ×0.8 (Cl 23.11.2.1); struts need either individual
column-style confinement (longitudinal + transverse reinforcement per
Cl 23.11.3.2, matching Chapter 18's special-moment-frame-column detailing)
or confinement of the entire member cross-section (Cl 23.11.3.3); tie
development length ×1.25 to account for likely overstrength/strain
hardening (Cl 23.11.4.1, Cl R23.11.4.1); and nodal zone compressive strength
×0.8 to account for tie yielding and reversed cyclic loading
(Cl 23.11.5.1, Cl R23.11.5.1).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-strength-reduction-factors]] — Chapter 21, including Table 21.2.1
  row (g), the φ = 0.75 used for struts/ties/nodal zones/bearing areas here.
- [[aci318-one-way-shear-strength]] — Cl 22.5, source of the `λ_s` size-effect
  factor reused in Eq. 23.4.4 and Cl 23.4.4.1.
- [[aci318-bearing-and-shear-friction]] — Cl 22.8/22.9, the same frustum
  confinement idea behind `β_c` and the shear-friction cross-reference of
  Cl 23.2.11.
- [[concrete-strut-and-tie-modelling]] — the AS 3600 equivalent, for
  structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 23 (Cl 23.1–23.11, pp. 435–454),
  incl. Tables 23.4.3(a)/(b), 23.5.1, 23.9.2 and Figs. R23.2.1, R23.2.6c.
