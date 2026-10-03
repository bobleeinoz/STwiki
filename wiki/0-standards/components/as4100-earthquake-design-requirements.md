---
title: Earthquake design and detailing requirements
category: 0-standards
tags: [earthquake, seismic, ductility, structural-performance-factor, moment-resisting-frame, braced-frame, plastic-hinge]
standards: [AS 4100:2020 Section 13, AS 1170.4]
status: draft
reviewed: 2026-09-13
---

# Earthquake design and detailing requirements

> Scope: AS 4100:2020 Section 13 — additional minimum design/detailing
> requirements for steel structures subject to AS 1170.4 earthquake
> forces: stiff and non-structural elements, structural ductility factor
> `μ` and structural performance factor `S_p` (Table 13.3.4), and detailing
> for limited-ductile, moderately-ductile and fully-ductile structures.
> AS 4100 itself supplies no seismic hazard/load magnitudes — those come
> from AS 1170.4.

## Summary

`[code]` Design/detailing requirements follow the **earthquake design
category and structural system** assigned under AS 1170.4 (Cl 13.3.1).
Three ductility tiers, each with its own detailing clause: **limited
ductile** (`μ = 2`, Cl 13.3.5), **moderately ductile** (`μ = 3`,
Cl 13.3.6), **fully ductile** (`μ > 3`, Cl 13.3.7 — routes to NZS
1170.5/NZS 3404, outside AS 4100's own scope).

## Detail

### Definitions (Cl 13.2)

`[code]` This Section adopts the AS 1170.4—2007 Cl 1.3 definitions for:
bearing wall system, braced frame, braced frame (concentric), braced frame
(eccentric), ductility (of a structure), moment-resisting frame (and its
ordinary/intermediate/special sub-types), seismic-force-resisting system,
space frame, structural ductility factor, structural performance factor.

### Stiff and non-structural elements (Cl 13.3.2–13.3.3)

`[code]` **Stiff elements** (13.3.2) not part of the seismic-force-resisting
system may still be incorporated, provided their effect on that system's
behaviour is considered and provided for in analysis and design (i.e. an
"non-structural" stiff infill or attachment can still attract seismic load
and must not be ignored).

`[code]` **Non-structural elements** (13.3.3) attached to or enclosing a
steel structure's exterior must accommodate earthquake-induced movement:
(a) connections/panel joints permit relative inter-storey movement ≥ the
AS 1170.4 design storey deflection, or 6 mm, whichever is greater; (b)
connections are ductile with rotation capacity to preclude brittle failure;
(c) in-plane panel movement connections use slotted/oversize-hole sliding
connections, bending-permitting details, or other test-demonstrated
adequate details.

### Structural ductility factor and structural performance factor (Cl 13.3.4, Table 13.3.4)

`[code]`

| Structural system | μ | S_p |
|---|---|---|
| Special moment-resisting frames (fully ductile) — see Note | 4 | 0.67 |
| Intermediate moment-resisting frames (moderately ductile) | 3 | 0.67 |
| Ordinary moment-resisting frames (limited ductile) | 2 | 0.77 |
| Moderately ductile concentrically braced frames | 3 | 0.67 |
| Limited ductile concentrically braced frames | 2 | 0.77 |
| Fully ductile eccentrically braced frames — see Note | 4 | 0.67 |
| Other steel structures not defined above | 2 | 0.77 |

Note: design of structures with `μ > 3` is **outside the scope of AS
4100** (Cl 13.3.7).

`[derived]` Note the inverse relationship visible in the table: higher `μ`
(more ductility credit taken in the AS 1170.4 seismic load reduction) pairs
with **lower** `S_p` (0.67) — i.e. a more ductile system is assumed to
absorb energy more reliably and gets a smaller performance-factor penalty,
but the corresponding AS 4100 detailing burden (Cl 13.3.6, plastic-hinge
member rules) increases sharply. A structure with `μ = 2` largely escapes
special seismic detailing (Cl 13.3.5(c): "no additional requirements" for
ordinary moment-resisting frames) at the cost of a smaller load-reduction
credit in AS 1170.4.

### Requirements for "limited ductile" structures, μ = 2 (Cl 13.3.5)

`[code]` (a) Minimum specified yield stress ≤ **350 MPa**. (b)
**Concentrically braced frames**: connections of diagonal brace members
expected to yield are designed for the **full member design capacity**.
(c) **Ordinary moment-resisting frames**: no additional requirements.

### Requirements for "moderately ductile" structures, μ = 3 (Cl 13.3.6)

`[code]` General (13.3.6.1): minimum specified `f_y ≤ 350 MPa`.

`[code]` **Bearing wall and building frame systems** (13.3.6.2) —
concentrically braced frames: (a) design axial force for each diagonal
**tension** brace member limited to **0.85 ×** its design tensile
capacity; connections of each diagonal brace designed for the **full**
member design capacity; (b) web stiffeners in beam-column connections
extend the full depth between flanges and are butt welded to both flanges;
(c) all welds are **SP category** (AS/NZS 1554.1), NDE per Table 13.3.6.2
(all to AS/NZS 1554.1):

| Weld type | Visual scanning | Visual examination | MPI or dye penetrant | Ultrasonic or radiography |
|---|---|---|---|---|
| Butt welds in members/connections in tension | 100% | 100% | 100% | 10% |
| Butt welds in members/connections, other than tension | 100% | 50% | 10% | 2% |
| All other welds in members/connections | 100% | 20% | 5% | 2% |

`[code]` **Intermediate moment-resisting frames** (13.3.6.3): (a) min.
`f_y ≤ 350 MPa`; (b) web stiffeners in beam-column connections full depth
between flanges, butt welded to both flanges; (c) members expected to form
plastic hinges under inelastic frame displacement conform to the Cl 4.5
plastic-analysis member requirements.

`[code]` **Fabrication in areas of plastic deformation** (13.3.6.4), for
**both** the bearing-wall/building-frame and intermediate-moment-frame
cases: (a) **edges** — a sheared edge is not permitted in a plastic-
deformation zone unless sheared oversize and machined to remove all
sheared-edge signs; a gas-cut edge in such a zone needs surface roughness
≤ **12 μm** (CLA); (b) **punching** — fastener holes in plastic-deformation
zones must not be punched full size — punch undersize and ream, or drill,
to remove the entire sheared surface.

### Requirements for "fully ductile" structures, μ > 3 (Cl 13.3.7)

`[code]` A fully ductile steel structure (`μ > 3`) is, under AS 1170.4,
required to be designed to **NZS 1170.5**, with members and connections
designed and detailed to **NZS 3404** — i.e. AS 4100 explicitly hands off
fully-ductile seismic design to the New Zealand standard suite rather than
providing its own provisions.

`[derived]` For Australian mining/material-handling structures — which
sit in generally lower seismic hazard regions than NZ and are rarely
designed for `μ > 3` — Cl 13.3.5 (limited ductile, `μ = 2`) is the most
commonly applicable tier in practice, particularly for lightly braced
industrial platforms, pipe racks and equipment support structures where
AS 1170.4 assigns a low earthquake design category. Confirm the AS 1170.4
category and structural system classification before assuming this,
though — a site in a higher hazard zone or an essential/high-importance
structure may still require `μ = 3` detailing.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as4100-limit-state-design-basis]] — Cl 3.11 routing to this Section and
  to AS 1170.4.
- [[as4100-structural-analysis-methods]] — Cl 4.5 plastic analysis member
  requirements referenced by Cl 13.3.6.3(c).
- [[as4100-weld-design]] — SP/GP weld category (Cl 9.6.1.3) tightened to SP
  by Cl 13.3.6.2(c) for moderately ductile braced frames.
- [[as4100-connection-design-requirements]] — Cl 9.1.3 earthquake load
  combination connection design, ductility requirement.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Section 13
  (pp. 171–173).
