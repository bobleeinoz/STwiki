---
title: Column design basis — design strength, minimum moment, design procedures
category: 0-standards
tags: [columns, design-basis, minimum-moment]
standards: [AS 3600:2018 Cl 10.1, AS 3600:2018 Cl 10.2]
status: draft
reviewed: 2026-09-12
---

# Column design basis

> Scope: AS 3600 Cl 10.1 (general design strength requirement, minimum
> moment, short/slender/braced definitions) and Cl 10.2 (which detailing
> clauses apply depending on which Section 6 analysis method produced the
> column's actions).

## Summary

`[code]` A column's design strength must resist axial force, shear, bending
moment from the analysis, **and** any additional bending moment from
slenderness effects (Cl 10.1.1) — slenderness isn't optional once a column
fails the short-column test (Cl 10.3.1, see
[[as3600-column-slenderness-and-moment-magnification]]).

## Detail

### Minimum bending moment (Cl 10.1.2)

`[code]` At any cross-section, about each principal axis, the design moment
is taken as not less than `N*×0.05D` (D = overall column depth in the
bending plane) — a floor moment representing unavoidable construction
eccentricity/imperfection, applied even to "axial-only" columns.

### Definitions (Cl 10.1.3)

`[code]` **Braced column** — lateral actions at the ends are resisted by
other elements (masonry infill, shear walls, lateral bracing), not by the
column itself. **Short column** — slenderness-induced additional moment can
be taken as zero. **Slender column** — doesn't qualify as short.

### Design procedure by analysis method (Cl 10.2)

`[code]` Which of Cl 10.3–10.7 apply depends on how the actions were
obtained:

- **Linear elastic analysis** (Cl 6.2): short columns use Cl 10.3, 10.6, 10.7;
  slender columns additionally use Cl 10.4 (moment magnification) — see
  [[as3600-column-slenderness-and-moment-magnification]]. `φ` from
  Table 2.2.2.
- **Elastic analysis with secondary bending moments** (Cl 6.3, sway frames):
  Cl 10.6/10.7 apply, and slender-column moments get a further braced-column
  moment magnifier `δb` (Cl 10.4.2) with the *unsupported* length `Lu` used
  in place of the effective length `Le` when calculating the buckling load
  `Nc` — own-words: this stacks a second-order correction on top of the
  frame analysis's own first-order sway-moment result. `φ` from Table 2.2.2.
- **Rigorous (non-linear) analysis** (Cl 6.5/6.6): Cl 10.6/10.7 apply, with
  slenderness effects already captured by the non-linear analysis itself
  rather than by a separate moment magnifier — see
  [[as3600-nonlinear-analysis-methods]].
- **Shear**: always designed per Cl 8.2 (see
  [[as3600-beam-shear-and-torsion-design]]), with shear reinforcement not
  less than required by Cl 10.7.2 and, where applicable, Section 14
  (earthquake).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-column-slenderness-and-moment-magnification]] — Cl 10.3–10.5.
- [[as3600-column-strength-interaction]] — Cl 10.6, the strength
  calculation every procedure above ultimately feeds.
- [[as3600-column-reinforcement-detailing]] — Cl 10.7.
- [[as3600-strength-check-procedures]] — Table 2.2.2 `φ` values.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clauses 10.1, 10.2.
