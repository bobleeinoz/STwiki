---
title: ACI 318M-19 structural system requirements — materials, load paths, strength/serviceability basis
category: 2-concrete
tags: [aci, structural-system, design-basis, structural-integrity]
standards: [ACI 318M-19 Cl 4.1, ACI 318M-19 Cl 4.4, ACI 318M-19 Cl 4.6, ACI 318M-19 Cl 4.10, ACI 318M-19 Cl 4.12]
status: draft
reviewed: 2026-09-30
---

# ACI 318M-19 structural system requirements

> Scope: ACI 318M-19 Chapter 4 — the "utility" chapter setting out what a
> structural system must include, how strength/serviceability/durability
> compliance is framed, structural integrity, and requirements specific to
> precast, prestressed, composite and plain-concrete construction. This is
> an **ACI 318M-19 page, kept separate from the AS 3600:2018 concept pages**
> elsewhere in `2-concrete` — see [[aci-318m-19-building-code-concrete]] for
> why.

## Summary

`[code]` Chapter 4 (added in the 2014 reorganisation) is the framework
chapter: it names the structural system components a design must account
for, points each to its governing member chapter, and states the top-level
strength/serviceability/durability/integrity requirements that every member
chapter then satisfies in detail (Cl R4.1).

## Detail

### Materials and design loads (Cl 4.2–4.3)

`[code]` Design properties of concrete (incl. shotcrete, which is treated as
concrete unless modified) come from Chapter 19; reinforcement properties from
Chapter 20; loads and load combinations from Chapter 5, based on ASCE/SEI 7
(Cl R4.3.1).

### Structural system and load paths (Cl 4.4)

`[code]` A structural system is built from: (a) one-way/two-way floor and
roof slabs, (b) beams and joists, (c) columns, (d) walls, (e) diaphragms,
(f) foundations, and (g) joints/connections/anchors transmitting force
between the above (Cl 4.4.1) — each governed by its own chapter (Ch 7–18,
Cl 4.4.2). A non-conforming structural arrangement is permitted only via the
Cl 1.10.1 special-system approval route (Cl 4.4.3).

`[code]` The system must be designed to resist factored loads without
exceeding member design strengths, via **one or more continuous load paths**
from the point of load application to the final point of resistance
(Cl 4.4.4) — and to accommodate anticipated volume change and differential
settlement (Cl 4.4.5).

`[code]` **Seismic-force-resisting system** (Cl 4.4.6): every structure is
assigned a Seismic Design Category (SDC) by the general building code (via
ASCE/SEI 7) or the building official. SDC A structures need only satisfy the
Code's general requirements — Chapter 18 (earthquake-resistant structures)
does not apply. SDC B–F structures must additionally satisfy Chapter 18.
Members deliberately excluded from the seismic-force-resisting system are
still permitted, but their effect on system response and the consequences of
damage to them must be considered (Cl 4.4.6.5); in SDC D–F, such members
must also meet Chapter 18's requirements for non-seismic-system members
(Cl 4.4.6.5.3, Cl 18.14). Nonlinear response history verification, where
used, follows Appendix A (Cl 4.4.6.7).

`[code]` **Diaphragms** (Cl 4.4.7) resist out-of-plane gravity load and
in-plane lateral force simultaneously; must transfer force to/from framing
members and provide lateral support to vertical/horizontal/inclined
elements; collectors are required wherever needed to complete the in-plane
load path (Cl 4.4.7.5, Cl R4.4.7.5 — "all structural systems must have a
complete load path... includ[ing] collectors where required"). SDC D–F
diaphragms that are part of the seismic system follow Chapter 18.

### Structural analysis (Cl 4.5)

`[code]` Any analytical procedure used must satisfy compatibility of
deformations and equilibrium of forces; the methods given in Chapter 6 are
permitted (which include the strut-and-tie method for discontinuity
regions, Cl R4.5).

### Strength (Cl 4.6)

`[code]` Core strength-design inequality: **φS_n ≥ U**, i.e. design strength
(nominal strength `S_n` × strength reduction factor `φ`) must be greater
than or equal to the required strength `U` from the governing factored-load
combination (Cl 4.6.1–4.6.2). `φ` accounts for under-strength probability
from material/dimensional variation, simplifying assumptions in the design
equations, ductility, failure mode, required reliability and redundancy
(Cl R4.6). `[derived]` This is the same general limit-state format as
AS 3600's `φR_u ≥ E*` (see [[concrete-strength-check-procedures]]), but the
`φ` values themselves and the load-combination basis are not interchangeable
between the two codes — do not substitute one code's `φ`/load factors into
the other's strength equation.

`[code]` Commentary note (Cl R4.6, non-mandatory): more strength than
required is not automatically safer — e.g. increasing flexural reinforcement
without a matching increase in shear reinforcement can shift the governing
failure mode from ductile flexure to brittle shear.

### Serviceability, durability, sustainability (Cl 4.7–4.9)

`[code]` Serviceability performance (reactions, moments, shears, torsions
and axial forces from prestress, creep, shrinkage, temperature, axial
deformation, restraint and settlement) is deemed satisfied if a member is
designed per its own chapter's provisions (Cl 4.7). Durability requires
concrete mixtures per Cl 19.3.2/26.4 for the relevant exposure, and
reinforcement corrosion protection per Cl 20.5 (Cl 4.8). Sustainability
requirements may be specified in addition to, but never in place of,
strength/serviceability/durability requirements (Cl 4.9).

### Structural integrity (Cl 4.10)

`[code]` Reinforcement and connections must be detailed to tie the structure
together and improve redundancy/ductility, so that damage to a major
supporting element stays localised rather than causing progressive collapse
(Cl 4.10.1.1, Cl R4.10.1.1). Cl 4.10.2.1 requires specific minimum
integrity detailing (bottom-bar continuity/anchorage at supports, etc.,
detailed on each member's own page) for the member types in Table 4.10.2.1:

![[aci318-table-4.10.2.1-structural-integrity-requirements.png]]
*Table 4.10.2.1 — minimum structural-integrity requirements by member type,
each pointing to its detailing clause (ACI 318M-19).*

`[derived]` Member types not listed in Table 4.10.2.1 (e.g. columns, walls)
are not exempt from structural integrity — Cl R4.10.2 notes their own
chapters address integrity indirectly through ordinary detailing
requirements, rather than through a dedicated integrity clause.

### Fire resistance (Cl 4.11)

`[code]` Members must satisfy the general building code's fire-protection
requirements; where the general building code demands more cover for fire
than Cl 20.5.1 requires structurally, the greater cover governs (Cl 4.11.1–
4.11.2). ACI 216.1M is cited as further guidance (Cl R4.11).

### Requirements for specific types of construction (Cl 4.12)

`[code]` **Precast concrete systems** (Cl 4.12.1): design must cover every
loading/restraint stage from fabrication through storage, transport and
erection to final use, including the effects of dimensional tolerances
(Cl 4.12.1.1–4.12.1.2). Where in-plane forces must transfer between members
of a precast floor/wall system, the load path must be continuous through
both members and connections, with a steel/reinforcement tension path where
tension occurs (Cl 4.12.1.4). Out-of-plane force distribution between
precast members is established by analysis or test (Cl 4.12.1.5).

`[code]` **Prestressed concrete systems** (Cl 4.12.2): design covers strength
and service-condition behaviour at all critical stages from first
application of prestress, including effects on adjoining construction from
elastic/plastic deformation, restraint, settlement, creep and shrinkage
(Cl 4.12.2.1–4.12.2.2). Loss of section from open ducts must be considered
before post-tensioning grout reaches design strength (Cl 4.12.2.4); external
post-tensioning tendons are permitted, evaluated with the same
strength/serviceability provisions (Cl 4.12.2.5).

`[code]` **Composite concrete flexural members** (Cl 4.12.3): members cast at
different times, designed as composite once the later-cast concrete has set,
are designed for every critical loading stage including any load applied
before the composite section reaches full design strength, with
reinforcement detailed to control cracking and prevent component separation
(Cl 4.12.3.1–4.12.3.4).

`[code]` **Structural plain concrete systems** (Cl 4.12.4): follow Chapter
14, both cast-in-place and precast.

### Construction/inspection and existing-structure evaluation (Cl 4.13–4.14)

`[code]` Construction specifications and inspection follow Chapter 26
(Cl 4.13). Strength evaluation of an existing structure follows Chapter 27,
covering both physical load testing (gravity loads only) and analytical
evaluation (any load type, including earthquake or wind) (Cl 4.14,
Cl R4.14).

## Worked reference

None yet.

## Contradictions

None recorded — see [[aci-318m-19-building-code-concrete]] for why this
source is not compared clause-by-clause against AS 3600.

## Related

- [[aci-318m-19-building-code-concrete]] — source register, chapter map, and
  the policy for keeping ACI pages separate from AS 3600 pages.
- [[concrete-limit-state-design-basis]] — the AS 3600 equivalent design-basis
  page (φR_u ≥ E* framing), for structural comparison only, not for mixing
  code provisions.

## Sources

- `raw/0-standards/ACI-318M-19.pdf`, Chapter 4 (Cl 4.1–4.14, pp. 51–60),
  incl. Table 4.10.2.1.
