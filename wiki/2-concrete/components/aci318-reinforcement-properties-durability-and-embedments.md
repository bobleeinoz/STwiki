---
title: ACI 318M-19 steel reinforcement properties, cover, corrosion protection and embedments
category: 2-concrete
tags: [aci, reinforcement, prestressing, cover, corrosion-protection, embedments]
standards: [ACI 318M-19 Cl 20.1, ACI 318M-19 Cl 20.2, ACI 318M-19 Cl 20.3, ACI 318M-19 Cl 20.4, ACI 318M-19 Cl 20.5, ACI 318M-19 Cl 20.6]
status: draft
reviewed: 2026-10-02
---

# ACI 318M-19 steel reinforcement properties, cover, corrosion protection and embedments

> Scope: ACI 318M-19 Chapter 20 in full — nonprestressed bar and wire material
> and design properties, maximum design yield strengths by application,
> seismic reinforcement restrictions, prestressing steel properties and
> stresses, headed shear studs, specified cover, coated reinforcement,
> tendon corrosion protection, and embedments. **ACI 318M-19 page, kept
> separate from the AS 3600:2018 pages** (see [[aci-318m-19-building-code-concrete]]).
> AS 3600 counterparts: [[concrete-durability-and-cover]],
> [[concrete-properties-of-concrete]]. ACI bar designations (No. 10–No. 57, metric)
> and grades (280/420/550/690) do not match AS/NZS 4671 bar grades.

## Summary

`[code]` Chapter 20 governs material properties, properties used in design, and
durability (incl. minimum cover) of steel reinforcement (Cl 20.1.1), and
embedments (Cl 20.1.2). Concrete durability and exposure classes are in
[[aci318-concrete-design-properties-and-durability]]; development, splices
and hooks in Chapter 25.

## Detail

### Nonprestressed bars and wires (Cl 20.2.1)

`[code]` Bars and wires are deformed, except plain bars/wires allowed for spirals
(Cl 20.2.1.1). Yield strength is by the 0.2 % offset method (ASTM A370) or
half-of-force yield point for sharp-kneed steel (Cl 20.2.1.2). Permitted deformed
bar specifications (max **No. 57**) (Cl 20.2.1.3): ASTM A615 carbon steel; A706
low-alloy; A996 axle/rail (rail Type R); A955 stainless; A1035 low-carbon chromium.
Other items: plain spiral bars to A615/A706/A955/A1035 (Cl 20.2.1.4); welded
deformed bar mats A184 (Cl 20.2.1.5); headed bars A970 Class HA (Cl 20.2.1.6);
wire and welded wire reinforcement A1064 or A1022 (Cl 20.2.1.7), deformed wire
MD25–MD200 (larger sizes in welded wire reinforcement treated as plain for
development/splice), welded-intersection spacing ≤ **400 mm** deformed /
**300 mm** plain in the stress direction (Cl 20.2.1.7.1–20.2.1.7.3).
A706 additionally requires base radius of deformations ≥ 1.5× deformation height,
assessed on new rolls (Cl 20.2.1.3(b)(iii)).

![[aci318-table-20.2.1.3a-a615-tensile-requirements.png]]
*Table 20.2.1.3(a) — A615 modified minimum tensile strength: Gr 280 → 420 MPa; Gr 420 →
550; Gr 550 → 690; Gr 690 → 790; actual tensile/yield ratio ≥ 1.10 for all grades
(ACI 318M-19).*

![[aci318-table-20.2.1.3b-a706-grade690-tensile.png]]
*Table 20.2.1.3(b) — A706 Grade 690: tensile ≥ 807 MPa, tensile/yield ≥ 1.17, yield
690–814 MPa, fracture elongation in 200 mm ≥ 10 % (ACI 318M-19).*

![[aci318-table-20.2.1.3c-a706-uniform-elongation.png]]
*Table 20.2.1.3(c) — A706 minimum uniform elongation: Nos. 10–32 → 9 % (Gr 420), 7 %
(Gr 550), 6 % (Gr 690); Nos. 36, 43, 57 → 6 % for all grades (ACI 318M-19).*

### Design properties (Cl 20.2.2)

`[code]` Stress = `E_s` × strain below `f_y`, constant at `f_y` beyond (elastic–
perfectly-plastic) (Cl 20.2.2.1); `E_s` may be taken as **200,000 MPa**
(Cl 20.2.2.2). Design `f_y` follows the specified grade and does not exceed the
Table 20.2.2.4 maxima for the application (Cl 20.2.2.3–20.2.2.4):

![[aci318-table-20.2.2.4a-nonprestressed-deformed-reinforcement.png]]
*Table 20.2.2.4(a) — deformed reinforcement: maximum `f_y`/`f_yt` and permitted ASTM
types by application. Highlights: special moment frames 550 MPa, special structural walls
690 MPa for flexure/axial/shrinkage-temperature (A706, or A615 Gr 420 under
Cl 20.2.2.5(b)); spirals 690 (confinement) and 420 (shear/torsion); stirrups, ties and
hoops 420 (550 permitted in listed cases); shear friction 420; strut-and-tie ties 550 for
longitudinal ties otherwise 420. The footnotes restrict A1064/A1022 welded wire in special
seismic systems and cap longitudinal `f_y` at 550 MPa for intermediate and ordinary moment
frames resisting earthquake demands (ACI 318M-19).*

![[aci318-table-20.2.2.4b-nonprestressed-plain-spiral-reinforcement.png]]
*Table 20.2.2.4(b) — plain spiral reinforcement: 690 MPa for seismic-system, confinement
and lateral-support spirals; 420 MPa for shear and torsion spirals (ACI 318M-19).*

**Seismic reinforcement (Cl 20.2.2.5).** `[code]` Deformed longitudinal bars resisting
earthquake moment/axial force in special seismic systems, and anchor reinforcement in
SDC C–F, are either (a) A706 Gr 420/550/690 for special walls (420/550 for special
moment frames), or (b) A615 Gr 420 provided (i) mill-test actual yield ≤ `f_y` + 125 MPa,
(ii) actual tensile/yield ≥ 1.25, (iii) fracture elongation in 200 mm ≥ 14 % (Nos. 10–19),
12 % (Nos. 22–36), 10 % (Nos. 43–57), and (iv) uniform elongation ≥ 9 % (Nos. 10–32),
6 % (Nos. 36, 43, 57). A615 Gr 550/690 is not permitted in special seismic systems. See
[[aci318-special-moment-frames]], [[aci318-special-structural-walls]].

### Prestressing steel (Cl 20.3)

`[code]` Permitted: ASTM A416 strand; A421 wire (or low-relaxation wire with S1); A722
high-strength bar; other products accepted if they meet those specifications' minimum
requirements and tests/analysis show no impairment (Cl 20.3.1.1–20.3.1.2). Precast
prestressing resisting earthquake effects in special moment frames and special walls
(incl. coupling beams, piers) is A416 or A722 only (Cl 20.3.1.3). `E_p` from tests or the
manufacturer (Cl 20.3.2.1).

![[aci318-table-20.3.2.2-prestressing-strands-wires-bars.png]]
*Table 20.3.2.2 — maximum `f_pu` for design: strand 1860 MPa (A416); wire 1725 MPa
(A421); high-strength bar 1035 MPa (A722) (ACI 318M-19).*

**`f_ps` at nominal flexural strength — bonded tendons (Cl 20.3.2.3).** `[code]` In place
of strain compatibility, Eq. 20.3.2.3.1 gives `f_ps` when all prestressed reinforcement is
in the tension zone and `f_se ≥ 0.5 f_pu`: `f_ps = f_pu[1 − (γ_p/β₁)(ρ_p f_pu/f'c +
(d/d_p)(ω − ω'))]` with ω terms from the nonprestressed steel. If compression steel is
included and `d' > 0.15 d_p` it is neglected; if included, the bracketed term is not
taken below **0.17**. (Equation reconstructed from the garbled text extraction;
**check against the printed Eq. 20.3.2.3.1 before using in a calculation.**)
Pretensioned strand stress within `ℓ_d` of the free end is limited per Cl 25.4.8.3
(Cl 20.3.2.3.2).

![[aci318-table-20.3.2.3.1-gamma-p.png]]
*Table 20.3.2.3.1 — γ_p: 0.55 for `f_py/f_pu ≥ 0.80`; 0.40 for ≥ 0.85; 0.28 for ≥ 0.90
(ACI 318M-19).*

**`f_ps` — unbonded tendons (Cl 20.3.2.4).** `[code]` Approximate `f_ps` permitted if
`f_se ≥ 0.5 f_pu`:

![[aci318-table-20.3.2.4.1-fps-unbonded-tendons.png]]
*Table 20.3.2.4.1 — `ℓ_n/h ≤ 35`: least of `f_se + 70 + f'c/(100ρ_p)`, `f_se + 420`, `f_py`;
`ℓ_n/h > 35`: least of `f_se + 70 + f'c/(300ρ_p)`, `f_se + 210`, `f_py` (MPa) (ACI 318M-19).*

**Permissible stresses and losses (Cl 20.3.2.5–20.3.2.6).**

![[aci318-table-20.3.2.5.1-max-tensile-stress-prestressing.png]]
*Table 20.3.2.5.1 — during stressing at the jacking end: least of 0.94 `f_py`, 0.80 `f_pu`
and the anchorage supplier's maximum jacking force; immediately after transfer at
post-tensioning anchorages and couplers: 0.70 `f_pu` (ACI 318M-19).*

`[code]` `f_se` accounts for seating at transfer, elastic shortening, creep, shrinkage,
steel relaxation and friction (wobble and curvature, from experimentally determined
coefficients), plus any loss through connection to adjoining construction
(Cl 20.3.2.6.1–20.3.2.6.3).

### Headed shear stud reinforcement (Cl 20.4)

`[code]` Headed shear stud reinforcement and stud assemblies conform to ASTM A1044
(Cl 20.4.1). Design use: [[aci318-two-way-shear-strength]],
[[aci318-two-way-slab-reinforcement-and-shear-detailing]].

### Specified cover (Cl 20.5.1)

`[code]` Minimums apply unless the general building code needs more for fire protection
(Cl 20.5.1.1); concrete floor finishes may count toward cover for nonstructural purposes
(Cl 20.5.1.2).

![[aci318-table-20.5.1.3.1-cover-cast-in-place-nonprestressed.png]]
*Table 20.5.1.3.1 — cast-in-place nonprestressed: 75 mm against ground; 50 mm (Nos. 19–57)
and 40 mm (No. 16/MW200/MD200 and smaller) exposed to weather or ground; 40 mm
beams/columns/pedestals/tension ties (primary steel, stirrups, ties, spirals, hoops) and
20 mm slabs/joists/walls (No. 36 and smaller; 40 mm for Nos. 43 and 57) when not exposed
(ACI 318M-19).*

![[aci318-table-20.5.1.3.2-cover-cast-in-place-prestressed.png]]
*Table 20.5.1.3.2 — cast-in-place prestressed: 75 mm against ground; weather/ground 25 mm
slabs/joists/walls, 40 mm other; not exposed 20 mm slabs/joists/walls, 40 mm primary
steel in beams/columns, 25 mm stirrups/ties/spirals/hoops (ACI 318M-19).*

![[aci318-table-20.5.1.3.3-cover-precast.png]]
*Table 20.5.1.3.3 — precast (plant conditions), nonprestressed or prestressed, by member,
exposure and bar/tendon size (e.g. walls exposed to weather 20–40 mm; other members 30–50
mm; not exposed 10–40 mm) (ACI 318M-19).*

![[aci318-table-20.5.1.3.4-cover-deep-foundations.png]]
*Table 20.5.1.3.4 — deep foundations: cast-in-place 75 mm not enclosed, 40 mm enclosed by
pipe/casing/rock socket; precast in ground 40 mm; in seawater 65 mm nonprestressed,
50 mm prestressed (ACI 318M-19).*

`[code]` Bundled bars: cover ≥ the smaller of the bundle's equivalent diameter and 50 mm
(75 mm against ground) (Cl 20.5.1.3.5). Headed stud heads and base rails: cover not less
than that for the member's reinforcement (Cl 20.5.1.3.6). Corrosive environments: increase
cover as needed and meet the Chapter 19 exposure-class requirements or provide other
protection (Cl 20.5.1.4.1); prestressed Class T or C members in corrosive/severe exposure
have prestressing cover ≥ **1.5×** the Cl 20.5.1.3.2 (cast-in-place) or 20.5.1.3.3 (precast)
values, unless the precompressed tension zone isn't in tension under sustained load
(Cl 20.5.1.4.2–20.5.1.4.3).

### Coated reinforcement and tendon protection (Cl 20.5.2–20.5.6)

![[aci318-table-20.5.2.1-coated-reinforcement.png]]
*Table 20.5.2.1 — coated bars: zinc A767; epoxy A775 or A934; dual zinc+epoxy A1055. Wire:
epoxy A884 only. Welded wire: zinc A1060, epoxy A884 (ACI 318M-19).*

`[code]` Coated bars conform to Cl 20.2.1.3(a)–(c); epoxy-coated wire and welded wire to
A1064 (Cl 20.5.2.2–20.5.2.3). **Unbonded tendons:** encased in watertight, continuous
sheathing, space filled with corrosion-inhibiting material, sheathing watertight at all
anchorages; single-strand tendons per ACI 423.7 (Cl 20.5.3). **Grouted tendons:** ducts
grout-tight, non-reactive, kept free of water; internal diameter ≥ 6 mm larger than a
single wire/strand/bar, or area ≥ 2× the steel area for multiple-element tendons
(Cl 20.5.4). Anchorages, couplers, end fittings and external tendons are protected for
long-term corrosion resistance (Cl 20.5.5–20.5.6).

### Embedments (Cl 20.6)

`[code]` Embedments must not significantly impair strength or fire protection and must not
harm concrete or reinforcement (Cl 20.6.1–20.6.2). Aluminium is coated or covered to
prevent aluminium–concrete reaction and electrolytic action with steel (Cl 20.6.3).
Reinforcement ≥ **0.002** × concrete section area is placed perpendicular to pipe
embedments (Cl 20.6.4). Pipe cover ≥ 40 mm exposed to earth/weather, ≥ 20 mm otherwise
(Cl 20.6.5).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[aci-318m-19-building-code-concrete]] — source register.
- [[aci318-concrete-design-properties-and-durability]] — Chapter 19.
- [[aci318-strength-reduction-factors]], [[aci318-sectional-strength-flexure-and-axial]],
  [[aci318-beam-reinforcement-limits-and-detailing]] — use these properties.
- [[aci318-special-moment-frames]], [[aci318-special-structural-walls]] — Cl 20.2.2.5 use.
- [[concrete-durability-and-cover]] — AS 3600 cover, for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 20 Cl 20.1–20.6 (pp. 371–389).
