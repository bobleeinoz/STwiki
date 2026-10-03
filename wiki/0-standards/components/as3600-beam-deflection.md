---
title: Deflection of beams
category: 0-standards
tags: [beams, deflection, serviceability, effective-inertia]
standards: [AS 3600:2018 Cl 8.5]
status: draft
reviewed: 2026-09-12
---

# Deflection of beams

> Scope: AS 3600 Cl 8.5 — refined calculation of beam deflection (short-term
> + long-term), and the deemed-to-comply span-to-depth ratio shortcut.

## Summary

`[code]` Three routes (Cl 8.5.1): refined calculation (Cl 8.5.2 lists what
must be allowed for), the short-term/long-term component method (Cl 8.5.3,
the standard's own worked-out version of "refined calculation"), or —
reinforced beams only — a deemed-to-comply span-to-depth ratio (Cl 8.5.4)
that avoids calculating a deflection at all.

## Detail

### What refined calculation must allow for (Cl 8.5.2)

`[code]` Cracking and tension stiffening; shrinkage and creep properties;
expected load history; expected construction procedure; and formwork
deflection/prop settlement during construction — particularly where beam
formwork is itself supported on suspended floors/beams below.

### Short-term deflection (Cl 8.5.3.1)

`[code]` Uses `Ecj` (Cl 3.1.2, see [[as3600-properties-of-concrete]]) and an
effective second moment of area `Ief`, either by rational calculation or at
nominated cross-sections: midspan value for a simply-supported span; for a
continuous beam, half the midspan value plus a quarter of each support value
(interior span) or half the midspan value plus half the continuous-support
value (end span); the support value for a cantilever. At each nominated
section, `Ief` interpolates between the gross/maximum value `Ief.max` and a
fully-cracked value `Icr`, weighted by the ratio of cracking moment to
in-service moment (a Branson-type equation) — `Ief.max` itself is the full
transformed gross inertia for prestressed sections, and for reinforced
sections is either the full gross inertia or 60% of it depending on whether
the tensile reinforcement ratio is above or below 0.005. The cracking moment
term nets out a shrinkage-induced tensile stress contribution, calculated
(absent refined analysis) from web tensile/compressive reinforcement ratios
— for the short-term portion of a long-term deflection, the final long-term
shrinkage strain is used instead, with indeterminate members additionally
accounting for restraint-induced redundant tension. `[practice]` A direct
alternative formula for `Ief` (skipping the `Icr`/`Ief.max` interpolation
entirely) is offered for reinforced members, split by whether the
reinforcement ratio is above or below a strength-dependent threshold.

### Long-term deflection (Cl 8.5.3.2)

`[code]` The long-term increment beyond short-term deflection is the sum of
a shrinkage component (from design shrinkage strain `εcs`, Cl 3.1.7) and a
creep component (from design creep coefficient `φcc`, Cl 3.1.8), by
mechanics — see [[as3600-properties-of-concrete]]. Absent more accurate
calculation, the combined creep+shrinkage increment for a reinforced beam
may be estimated by multiplying the short-term sustained-load deflection by
a multiplier `kcs` that **reduces** as the compression-reinforcement-to-
tension-reinforcement ratio `Asc/Ast` (at midspan, or at the support for a
cantilever) increases — own-words: compression steel measurably restrains
long-term creep/shrinkage deflection, which is exactly why Cl 8.5.3.1 also
uses `Asc/Ast` in its own formula for `kcs`.

### Deemed-to-comply span-to-depth ratio (Cl 8.5.4)

`[code]` Applies only to uniform-cross-section reinforced beams, fully
propped during construction, under uniformly distributed load, with imposed
action ≤ permanent action. If `Lef/d` satisfies a formula combining an
effective-inertia coefficient `k1` (the same reinforced-member formula as
Cl 8.5.3.1's alternative `Ief`), a support-condition coefficient `k2` (fixed
values for simply-supported vs. end-span vs. interior-span continuous
beams, the latter two conditional on adjacent-span-ratio and end-span-length
limits matching [[as3600-simplified-flexural-analysis]]'s Cl 6.10.2 gate),
`Ec`, and an effective design load `Fd.ef` (built from `kcs`-scaled dead load
plus short/long-term-factored live load per AS/NZS 1170.0), the beam is
deemed to satisfy the Cl 2.3.2 deflection limits without a direct deflection
calculation.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-serviceability-design]] — Cl 2.3.2 deflection limits this
  clause satisfies.
- [[as3600-properties-of-concrete]] — `εcs`, `φcc`, `Ec` inputs.
- [[as3600-slab-deflection]] — the equivalent slab clause (Cl 9.4), which
  reuses this clause's short-term/long-term method directly.
- [[as3600-simplified-flexural-analysis]] — shares the Cl 6.10.2
  applicability gate with the deemed-to-comply route here.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint.pdf`, Clause 8.5.
