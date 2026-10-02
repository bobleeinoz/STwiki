---
title: Simplified design method for walls under vertical compression
category: 2-concrete
tags: [walls, simplified-method, axial-strength]
standards: [AS 3600:2018 Cl 11.5]
status: draft
reviewed: 2026-09-12
---

# Simplified design method for walls under vertical compression

> Scope: AS 3600 Cl 11.5 — the segment-based simplified axial-strength
> method for braced walls in compression, as an alternative to the full
> column-interaction-diagram method (Section 10).

## Summary

`[code]` Where a wall is subject to in-plane bending under vertical
compression, it's divided into design segments, each checked at its own
highest stress (Cl 11.5.1) — a simplification that avoids running a full
interaction-diagram check across the whole wall length.

## Detail

### Applicability limits (Cl 11.5.2)

`[code]` This simplified method may only be used where: design axial stress
≤3 MPa, *unless* vertical and horizontal reinforcement is provided on both
faces (split equally between faces); the site isn't classified De/Ee per
AS 1170.4 in a structure subject to earthquake design actions; and effective
height-to-thickness ratio `Hwe/tw` ≤20 for singly-reinforced walls or ≤30 for
doubly-reinforced walls. Outside these limits, the wall must be designed as
a column under Section 10 instead — see
[[concrete-column-strength-interaction]].

### Design axial strength (Cl 11.5.3)

`[code]` Provided `Hwe/tw ≤ 30`: `φNu` per unit length, with `φ = 0.65` and
`Nu = tw·(1.2 − 2e − 2ea)/0.6 × f'c`... `[derived]` — the OCR extraction of
this specific equation was garbled (bracket/operator placement uncertain);
the governing variables are clear (wall thickness `tw`, an eccentricity
term, an additional slenderness-related eccentricity `ea`, and `f'c`), and
own-words the formula reduces axial capacity as either the applied
eccentricity or the additional slenderness eccentricity grows — but **the
exact arithmetic form should be read directly from Cl 11.5.3** rather than
relied on from this page. The additional eccentricity
`ea = (Hwe)²/(2500·tw)` is a slenderness-induced allowance (a P-delta-style
lever-arm addition, analogous in purpose to the Cl 10.4 moment magnifier but
expressed directly as an eccentricity rather than a moment multiplier).

`[code]` **Load eccentricity** (Cl 11.5.4): eccentricity from a
floor/roof load applied at the wall top — a third of the bearing-area depth
from the wall's span face for a discontinuous floor, or zero for a cast-in-
situ floor continuous over the wall. Eccentricity from the aggregated load
of all floors above may be taken as zero. The resultant eccentricity from
combining these is floored at `0.05·tw` — i.e. even a nominally
concentric/continuous-floor wall is designed for a minimum practical
eccentricity, not true zero.

## Worked reference

None yet — a strong candidate for the wiki's first human-verified worked
example, given the flagged uncertainty in the `Nu` formula above.

## Contradictions

None recorded.

## Related

- [[concrete-wall-design-basis-and-classification]] — Cl 11.2 routing logic
  that leads here.
- [[concrete-column-strength-interaction]] — the full method this
  simplification substitutes for, and the fallback where this method's
  limits are exceeded.
- [[concrete-column-slenderness-and-moment-magnification]] — the conceptual
  parallel between this clause's `ea` and Section 10's moment magnifier.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clause 11.5. **Note**: the
  Cl 11.5.3 `Nu` equation's exact arithmetic form was not reliably extracted
  from the source PDF — verify directly against the clause before use.
