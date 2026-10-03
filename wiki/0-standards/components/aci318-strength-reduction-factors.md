---
title: ACI 318M-19 strength reduction factors — φ table, tension/compression-controlled classification
category: 0-standards
tags: [aci, phi-factor, ductility, strength-design]
standards: [ACI 318M-19 Cl 21.2.1, ACI 318M-19 Cl 21.2.2, ACI 318M-19 Cl 21.2.3, ACI 318M-19 Cl 21.2.4]
status: draft
reviewed: 2026-10-01
---

# ACI 318M-19 strength reduction factors (φ)

> Scope: ACI 318M-19 Chapter 21 — the φ-factor table by action/element type
> (Cl 21.2.1), the net-tensile-strain-based classification of sections as
> compression-controlled/transition/tension-controlled that sets φ for
> moment and axial force (Cl 21.2.2), the reduced φ for pretensioned
> sections near the end of a member (Cl 21.2.3), and the seismic shear-φ
> modifications (Cl 21.2.4). This is an **ACI 318M-19 page, kept separate
> from the AS 3600:2018 concept pages** elsewhere in `2-concrete` — see
> [[aci-318m-19-building-code-concrete]] for why.

## Summary

`[code]` Design strength at a section is always `φS_n`, where `S_n` is
nominal strength and `φ` is the applicable strength reduction factor
(Cl 22.1.3). Chapter 21 is the single source for every `φ` value used
elsewhere in the Code; most are fixed constants by action/element type
(Table 21.2.1), but `φ` for moment/axial/combined moment-and-axial force is
not fixed — it varies continuously with how ductile the section's failure
mode is, measured by the net tensile strain `ε_t` in the extreme tension
reinforcement at nominal strength (Cl 21.2.2, Table 21.2.2).

## Detail

### Table 21.2.1 — φ by action or element (Cl 21.2.1)

![[aci318-table-21.2.1-strength-reduction-factors.png]]
*Table 21.2.1 — strength reduction factors φ by action or structural
element (ACI 318M-19).*

`[code]` Notable values: shear and torsion both 0.75; bearing 0.65; plain
concrete elements 0.60 (same value for every plain-concrete failure mode,
since both flexural tension and shear strength of plain concrete depend on
the same unreinforced concrete tensile strength, Cl R21.2.1); post-tensioned
anchorage zones 0.85; brackets/corbels 0.75 (a single value covering every
potential failure mode, Cl R21.2.1); strut-and-tie struts/ties/nodal
zones/bearing areas 0.75 (Chapter 23); precast-connection components
controlled by steel yielding in tension 0.90; anchors in concrete 0.45–0.75
per Chapter 17. Moment/axial/combined force is the one row that routes to
its own table (21.2.2) rather than a fixed value.

### Tension-controlled / compression-controlled classification (Cl 21.2.2)

`[code]` At nominal strength, the extreme compression fibre strain is taken
as `ε_cu = 0.003` and strain is assumed linear across the section
(Cl 22.2.1.2). The **net tensile strain `ε_t`** is the strain in the extreme
tension reinforcement at that same condition, excluding prestress/creep/
shrinkage/temperature strain:

![[aci318-fig-r21.2.2a-strain-distribution-net-tensile-strain.png]]
*Fig. R21.2.2a — strain distribution and net tensile strain in a
nonprestressed member; `c` is neutral-axis depth, `d_t` is depth to the
extreme tension reinforcement (ACI 318M-19).*

`[code]` `ε_ty` (the "compression-controlled strain limit") is the
reinforcement's own yield strain: `ε_ty = f_y / E_s` for deformed bars
(taken as 0.002 for Grade 420 as a permitted simplification, Cl 21.2.2.1),
or 0.002 for all prestressed reinforcement (Cl 21.2.2.2). Table 21.2.2 then
sets φ for moment/axial/combined force by where `ε_t` falls relative to
`ε_ty`:

![[aci318-table-21.2.2-phi-moment-axial-by-net-tensile-strain.png]]
*Table 21.2.2 — φ for moment, axial force, or combined moment and axial
force, by net tensile strain `ε_t` and transverse reinforcement type
(ACI 318M-19).*

- **Compression-controlled** (`ε_t ≤ ε_ty`): φ = 0.75 for spiral transverse
  reinforcement (Cl 25.7.3), 0.65 otherwise. `[code]` Spiral columns get the
  higher value because spiral confinement gives them more post-peak
  ductility and toughness than tied columns (Cl R21.2.2).
- **Transition** (`ε_ty < ε_t < ε_ty + 0.003`): φ interpolates linearly
  between the compression-controlled and tension-controlled values — the
  spiral and "other" interpolation lines have different slopes (0.15 vs
  0.25 per 0.003 strain), so they do **not** meet at the same intermediate
  φ for a given `ε_t`. It is always permitted to conservatively use the
  compression-controlled φ instead of interpolating (Table 21.2.2 footnote
  [1]).
- **Tension-controlled** (`ε_t ≥ ε_ty + 0.003`): φ = 0.90 regardless of
  transverse reinforcement type.

![[aci318-fig-r21.2.2b-phi-variation-with-net-tensile-strain.png]]
*Fig. R21.2.2b — variation of φ with net tensile strain `ε_t` in the
extreme tension reinforcement, spiral vs other transverse reinforcement
(ACI 318M-19).*

`[code]` Members under axial compression only are compression-controlled by
definition; members under axial tension only are tension-controlled by
definition (Cl R21.2.2). Beams and slabs are ordinarily tension-controlled;
columns may be compression-controlled; members with small axial force and
large moment often land in the transition zone (Cl R21.2.2).

`[code]` **2019 Code change**: the tension-controlled limit on `ε_t` used to
be a fixed 0.005 (calibrated to Grade 420 reinforcement). From the 2019
edition it is `ε_ty + 0.003`, so it scales with the reinforcement's own
yield strain — this accommodates nonprestressed reinforcement grades above
420 (Cl R21.2.2). A page citing the old fixed-0.005 limit is citing a
pre-2019 edition.

`[derived]` `[derived]` Moment redistribution per Cl 6.6.5 requires a higher
ductility than plain tension-controlled classification — redistribution is
limited to sections with `ε_t ≥ 0.0075` specifically (Cl R21.2.2), not
merely `ε_t ≥ ε_ty + 0.003`.

`[derived]` This net-tensile-strain-based sliding scale has no direct AS
3600 counterpart — AS 3600's Table 2.2.2 instead sets a single fixed φ per
action/ductility-class combination (see
[[as3600-strength-check-procedures]]). The two φ-factor systems are not
numerically comparable term-for-term; do not substitute one code's φ into
the other's strength equation.

### φ near the end of pretensioned members (Cl 21.2.3)

`[code]` Where a pretensioned flexural member's strands are not yet fully
developed at the section under consideration (i.e. within the strand
development length of the member end), using the full Table 21.2.2 φ would
be unconservative — bond-slip there is a brittle failure mode resembling
shear. Table 21.2.3 instead steps φ from 0.75 at the transfer length `ℓ_tr`
(Eq. 21.2.3: `ℓ_tr = (f_se/21) d_b`) up to `φ_p` (the Table 21.2.2 value at
the section where all strands are fully developed) over the development
length `ℓ_d` (Cl 25.4.8.1), by linear interpolation — separately tabulated
for fully-bonded strands and for one-or-more debonded strands (with or
without calculated tension at the section). `[derived]` Not reproduced here
as a figure/table given its narrow applicability (pretensioned members with
underdeveloped strand only) — see Table 21.2.3 and Cl R21.2.3 Figs
R21.2.3a/R21.2.3b in the source for the full stepped-φ diagrams.

### Seismic shear-φ modifications (Cl 21.2.4)

`[code]` For elements relied on to resist earthquake effects `E` — special
moment frames, special structural walls, or intermediate precast structural
walls in Seismic Design Category D/E/F — the shear φ of 0.75 is modified:

- **φ = 0.60** for any such member where nominal shear strength is less than
  the shear corresponding to development of the member's nominal moment
  strength (i.e. a shear-controlled member that would fail in shear before
  reaching its flexural capacity) (Cl 21.2.4.1).
- **Diaphragms** and **foundation elements supporting the primary
  seismic-force-resisting system**: shear φ capped at the least shear-φ used
  for the vertical seismic-system elements they support/connect to
  (Cl 21.2.4.2–21.2.4.3) — intended to give the diaphragm/foundation extra
  reserve relative to a wall designed down at φ = 0.60 (Cl R21.2.4.2).
- **φ = 0.85** for beam-column joints of special moment frames and for
  diagonally-reinforced coupling beams (Cl 21.2.4.4).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[aci318-sectional-strength-flexure-and-axial]] — Cl 22.2–22.4, which uses the
  `ε_t` classification from this page to set φ for every flexural/axial
  design check.
- [[aci318-one-way-slab-design]], [[aci318-two-way-slab-design-basis]] —
  Chapters 7–8, which both require the Table 21.2.2 tension-controlled
  strain limit for nonprestressed slabs.
- [[as3600-strength-check-procedures]] — the AS 3600 equivalent (Table
  2.2.2 fixed-φ-by-ductility-class), for structural comparison only.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 21 (Cl 21.1–21.2.4, pp. 391–396),
  incl. Tables 21.2.1–21.2.3 and Figs. R21.2.2a, R21.2.2b.
