---
title: Connection classification and design philosophy — forms of construction, design models, moment-rotation behaviour
category: 1-steelwork
tags: [connections, rigid-construction, simple-construction, semi-rigid-construction, moment-rotation, connection-design-model, ASI-handbook-1]
standards: [AS 4100:2020 Cl 9.1.3, AS 4100:2020 Cl 4.2, AS 4100:2020 Cl 4.3.4]
status: draft
reviewed: 2026-09-13
---

# Connection classification and design philosophy

> Scope: background theory behind connection design, from ASI Design Guide
> "Handbook 1 — Background and Theory: Design of Structural Steel
> Connections" (T.J. Hogan, first edition 2007) Sections 1–2: the concept
> of the ASI Connections Series design-guide approach, the three AS 4100
> forms of construction (rigid/semi-rigid/simple), the four elements a
> connection design model must capture, and real moment-rotation behaviour
> of common connection types. This is industry design-guide commentary,
> not AS 4100 text itself — see [[as4100-connection-design-requirements]]
> for the code clauses it explains.

## Summary

`[practice]` The ASI Connections Series (of which this handbook is the
background/theory volume) provides recognised, experimentally-supported
design models for connections, since AS 4100 itself specifies fastener and
member design but deliberately leaves connection-specific design procedures
to the designer (Cl 9.1.3). `[code]` Any connection design model must,
per Cl 9.1.3: keep distributed design action effects in equilibrium with
the actions on the connection; keep deformations within element deformation
capacities; ensure every element and adjacent member area resists the
effects acting on it; and remain stable under the actions and deformations
— on the basis of a recognised method supported by experimental evidence.

`[code]` AS 4100 Cl 4.2 defines three forms of construction — **rigid**,
**semi-rigid**, **simple** — and requires connection design consistent with
whichever form is assumed in the structural analysis.

## Detail

### Why a design-guide series exists (Ch 1)

`[practice]` No structural steel code specifies a detailed design procedure
for any particular connection type — codes cover member design and give only
basic fastener design rules, leaving the designer to assess connection
behaviour case by case. The ASI Connections Series (this handbook plus
individual connection-type design guides) exists to reduce that burden by
providing pre-researched design models, calibrated against test evidence,
for the connection types in common use in Australia (originally those
covered by the earlier AISC "Standardized Structural Connections").
`[derived]` Because a given connection's true behaviour can be modelled more
than one valid way, a design guide's recommended model is **a** reasonable
model, not **the** only one — an engineer may adopt a different recognised,
experimentally-supported model and still satisfy Cl 9.1.3.

### The three forms of construction (Cl 4.2, discussed Ch 2.2)

`[code]`
- **Rigid construction**: connections assumed to hold the original angles
  between members unchanged; joint deformations must not significantly
  affect the frame's action-effect distribution or overall deformation.
  Typical rigid connections (Figure 1): welded moment connection (shop- or
  field-welded, including erection web side plates and web copes for butt-
  weld access), bolted moment end plate, moment splice (bolted or welded),
  moment-transmitting base plate.
- **Semi-rigid construction**: connections need not hold the original
  angles unchanged, but must furnish a dependable, known degree of flexural
  restraint; the moment-rotation relationship must be established by methods
  based on test results.
- **Simple construction**: end connections assumed not to develop bending
  moments; must be able to deform to provide the required rotation without
  developing a restraining moment that adversely affects the structure;
  rotation capacity must be demonstrated experimentally; the connection is
  then treated as subject to reaction shear at an eccentricity appropriate
  to its detailing. Typical simple connections (Figure 2): angle seat,
  bearing pad, flexible end plate, angle cleat, web side plate (fin plate).

![[asi-h1-fig-1-rigid-connections.png]]
*Figure 1 — rigid connections: (a) field welded moment connection, (b) shop
welded stub girder plus bolted field splice, (c) bolted moment end plate
(ASI Handbook 1, 2007).*

![[asi-h1-fig-2-simple-connections.png]]
*Figure 2 — simple connections: (a) angle seat, (b) bearing pad,
(c) flexible end plate, (d) angle cleat, (e) web side plate (ASI Handbook 1,
2007).*

`[code]` AS 4100 only explicitly corrects for the gap between assumed and
real behaviour in the case of **simple** construction: real simple
connections do transmit some bending moment as well as shear. This moment is
conservatively neglected when proportioning the **beam**, but is accounted
for when proportioning the **column** via Cl 4.3.4 — the line of action of a
beam reaction is taken at 100 mm from the column face towards the span, or
at the centre of bearing, whichever is greater. `[derived]` Consequently
every column in a simple-construction frame is, in effect, designed as a
beam-column for at least this minimum eccentricity moment, even though the
beam itself is designed as if the connection carried no moment.

`[derived]` Loss of rigidity in a real "rigid" connection likewise causes a
redistribution of bending moments through the frame, which can adversely
affect some members — a reason rigid-connection design models are
calibrated to be genuinely stiff rather than merely nominally "rigid".

### Connection design models (Ch 2.3)

`[code]` Per Cl 9.1.3, a design model must: (a) keep the distributed design
action effects in equilibrium with the actions on the connection; (b) keep
deformations within the connection elements' deformation capacities;
(c) ensure every connection element and adjacent member area is capable of
resisting the effects acting on it; (d) keep the connection elements stable
under the actions and deformations — on the basis of a recognised method
supported by experimental evidence. Bolt-installation residual actions need
not be considered.

`[derived]` This is a lower-bound (static/equilibrium) design philosophy:
the model only has to find **an** equilibrium distribution of forces that
every element can carry — it does not have to reproduce the actual elastic
distribution (compatibility is "unlikely to be satisfied"), provided the
elements are ductile enough to redistribute to the assumed path. This is the
same philosophy as classical lower-bound plastic design of connections
(Ref. 4 in the handbook), stated in Ch 2.4 as: (i) take into account overall
connection behaviour and carry out an analysis giving a realistic force
distribution; (ii) ensure every component/fastener in every action path has
sufficient capacity for the applied action; (iii) recognise the procedure
only guarantees equilibrium, not compatibility, so connection elements must
be capable of ductile behaviour to redistribute as assumed.

`[code]` A connection is considered (Cl 9.1.1/Ch 2.3) to consist of four
elements, all of which must have their design capacity evaluated:
(A) fasteners (bolts or welds); (B) components (plates, gussets, cleats);
(C) the supported member (in the vicinity of the connection); (D) the
supporting member (in the vicinity of the connection). See
[[steel-bolt-group-analysis-methods]] and
[[steel-weld-group-analysis-methods]] for (A);
[[steel-connection-component-capacity]] for (B);
[[steel-coped-beam-capacity]] for (C); [[steel-connection-standard-detailing-dimensions]]
for (D).

`[practice]` The design models in the ASI Connections Series are intended
for **statically loaded** connections only; connections subject to dynamic
loads, earthquake loads or fatigue may need additional considerations
beyond this series — see [[as4100-fatigue-design]] and
[[as4100-earthquake-design-requirements]].

### Real moment-rotation behaviour (Ch 2.4)

`[practice]` No real connection is either fully rigid (infinite initial
stiffness) or a true pin (zero moment at any rotation); whether a given
connection behaves as "rigid" or "simple" can depend on the rotation
demanded of it. Figure 3 plots typical moment-rotation curves: rigid
end-plate connections show high initial stiffness with a "rigid" branch
merging into a flatter "semi-rigid" branch at higher rotation; the nominally
simple connections (web side plate, flexible end plate, bolted angle cleat,
angle seat) all show a much lower, near-constant moment plateau consistent
with simple-construction design.

![[asi-h1-fig-3-moment-rotation-characteristics.png]]
*Figure 3 — moment-rotation characteristics of typical connections
(ASI Handbook 1, 2007).*

`[practice]` A connection joins a "member" to a "support"; supports may be
idealised as **flexible** (all beam-end rotation is accommodated by
movement/flexibility of the support) or **stiff** (all rotation accommodated
by deformation within the connection), but in practice lie somewhere between
these extremes. In a genuinely flexible-support case, statics require the
bolt/weld groups and connection components to resist the *full* moment and
shear at the connection. With a stiff support, two design extremes are
possible: (a) maintain significant stiffness and strength through every
connection element; or (b) deliberately make one element rotationally
flexible without impairing its load-carrying capacity.

`[practice]` The angle seat, bearing pad, flexible end plate and angle cleat
are generally detailed to option (b) — but the "flexible" component must be
made *only as flexible as necessary*; over-stiffening it imposes unwanted
rotation demand and bending moment onto the other components and the
support. The web side plate connection nominally falls under option (a):
the weld is stiff with little ductile rotation capacity, but the plate can
form a plastic hinge, and the bolt group itself has significant rotation
capacity — test evidence suggests most of the rotation in a web side plate
connection actually occurs in the bolt group. `[derived]` Where rotation
capacity is provided *directly adjacent to the support* (flexible end
plate, flexible angle cleat) versus *at a distance from the support* (angle
seat, web side plate), the latter case requires the support and the
intervening components to always be checked for bending moment as well as
shear — the recommended design models in the individual connection-type
design guides account for either a stiff or a flexible support without
distinguishing between them.

`[derived]` Because connection detailing practice, tolerances and component
design capacities differ between countries, a design model calibrated
against test data from one country's practice may not transfer directly to
another — and comparing reported connection failure loads against the
design capacities standing at the time of the test (rather than against the
measured strength of the individual components) can distort interpretation
of older research data. Virtually all reported simple-connection testing has
been done under a **stiff**-support condition, which is part of why the
Series' recommended models do not distinguish stiff from flexible supports.

## Worked reference

None — this page is background theory; worked examples are on
[[steel-bolt-group-analysis-methods]] and [[steel-weld-group-analysis-methods]].

## Contradictions

None recorded.

## Related

- [[as4100-connection-design-requirements]] — AS 4100 Cl 9.1 code text this
  handbook explains (classification, minimum design actions, block shear).
- [[as4100-structural-analysis-methods]] — Cl 4.2 forms of construction as
  used in frame analysis.
- [[steel-bolt-group-analysis-methods]] — bolt-group design models used to
  realise the connection design philosophy above.
- [[steel-weld-group-analysis-methods]] — weld-group design models.

## Sources

- `raw/1-steelwork/ASI - Handbook 1 - Background and Theory - Design of
  Structural Steel Connections.pdf`, Sections 1–2 (pp. 1–9). Figures 1, 2, 3
  reproduced in `wiki/1-steelwork/assets/`.
