---
title: Crack control of slabs (flexure, shrinkage and temperature)
category: 0-standards
tags: [slabs, crack-control, shrinkage, temperature]
standards: [AS 3600:2018 Cl 9.5]
status: draft
reviewed: 2026-09-12
---

# Crack control of slabs

> Scope: AS 3600 Cl 9.5 — flexural crack control (reusing the beam method),
> plus slab-specific shrinkage/temperature crack control, restraint zones and
> openings.

## Summary

`[code]` Flexural crack control mirrors [[as3600-beam-crack-control]]
almost exactly (same structure: baseline detailing → steel-stress limit
tables → direct crack-width calculation → prestressed-slab variant). What's
genuinely slab-specific is Cl 9.5.3: shrinkage/temperature reinforcement,
because slabs have a secondary direction that beams don't.

## Detail

### General requirements (Cl 9.5.1)

`[code]` Same philosophy as beams: control cracking to protect durability/
serviceability/appearance, with a chosen `wmax` per surface. For slabs fully
enclosed in a building (bar brief construction exposure) where cracking
won't impair function: minimum reinforcement per Cl 9.1.1 (see
[[as3600-slab-strength-in-bending]]), plus a bar-spacing cap (the lesser of
`2.0Ds` or 300 mm, ignoring bars under half the largest bar's diameter).
Otherwise, add either the Cl 9.5.2.2 crack-width calculation or the Cl 9.5.2.1
steel-stress-limit shortcut. Unbonded-tendon prestressed elements follow the
reinforced-concrete rules; bonded-tendon elements use Cl 9.5.2.3 instead.

### Flexural crack control (Cl 9.5.2)

`[code]` **Without direct calculation** (9.5.2.1): calculated steel stress
`σscr` must not exceed the *larger* of the Table 9.5.2.1(A) limit (by bar
diameter, itself split by slab depth above/below 300 mm) and the Table
9.5.2.1(B) limit (by bar spacing) — plus the same `σscr.1 ≤ 0.8fsy`
direct-loading cap as beams.

![[as3600-table-9.5.2.1a-max-steel-stress-slabs-bar-diameter.png]]
*Table 9.5.2.1(A) — maximum steel stress for flexure in reinforced slabs, by
nominal bar diameter and slab depth (AS 3600:2018).*

![[as3600-table-9.5.2.1b-max-steel-stress-slabs-spacing.png]]
*Table 9.5.2.1(B) — maximum steel stress for flexure in reinforced slabs, by
centre-to-centre bar spacing (AS 3600:2018).*

**By calculation** (9.5.2.2): identical formula
to Cl 8.6.2.3 — see [[as3600-beam-crack-control]]. **Prestressed slabs**
(9.5.2.3): deemed controlled if max tensile stress under short-term service
load stays within `0.25√f'c`; otherwise add reinforcement/bonded tendons
near the tensile face (spacing ≤ lesser of 300 mm/`2.0Ds`) and satisfy one of:
limiting stress to `0.6√f'c`, limiting the steel-stress increment per Table
9.5.2.3 (same structure as the beam Table 8.6.3), or a direct
crack-width calculation.

![[as3600-table-9.5.2.3-max-stress-increment-prestressed-slabs.png]]
*Table 9.5.2.3 — maximum increment of steel stress for flexure in prestressed
slabs (AS 3600:2018).*

### Shrinkage and temperature crack control (Cl 9.5.3)

`[code]` Required reinforcement area accounts for flexural action, restraint
against in-plane movement, and exposure classification (Cl 9.5.3.2–9.5.3.5).
For members >500 mm thick, reinforcement near each surface may be calculated
using 250 mm as the effective `D`.

- **Primary direction** (9.5.3.2): no *additional* shrinkage/temperature
  reinforcement needed if the flexural reinforcement already meets Cl 9.1.1
  **and** 75% of whichever secondary-direction requirement below would
  otherwise apply.
- **Secondary direction, unrestrained** (9.5.3.3): minimum area scales
  linearly with slab cross-sectional area (`b·D`), reduced by a term in
  average effective prestress `σcp` — own-words: prestress compression
  directly offsets the shrinkage/temperature reinforcement demand.
- **Secondary direction, restrained** (9.5.3.4): three tiers of required
  reinforcement (minor / moderate / strong crack-control), each a fixed
  coefficient times `b·D` minus the same prestress offset — which tier
  applies depends on whether the slab is fully enclosed (allows the lowest
  tier) versus other exposure classifications, with B1/B2/C1/C2 exposure
  always requiring the strongest tier regardless of enclosure. Bar spacing
  in this case is capped at the lesser of `1.5Ds` or 200 mm.
- **Secondary direction, partially restrained** (9.5.3.5): assessed between
  the unrestrained and restrained values by engineering judgement.

### Restraints, openings and discontinuities (Cl 9.5.4–9.5.5)

`[code]` Near restraints, internal forces/cracks induced by prestress,
shrinkage or temperature need special attention (no formula — a flag to
assess). Openings/discontinuities need additional properly-anchored
reinforcement where necessary, same engineering-judgement framing as the
beam equivalent (Cl 8.6.5).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-beam-crack-control]] — Cl 8.6.2.3 crack-width formula reused
  directly by Cl 9.5.2.2.
- [[as3600-slab-strength-in-bending]] — Cl 9.1.1 minimum reinforcement
  baseline; Cl 9.2.3 load-distribution reinforcement (a distinct requirement
  from shrinkage/temperature steel).
- [[as3600-durability-and-cover]] — exposure classification driving the
  Cl 9.5.3.4 restrained-slab tier.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clause 9.5 (Tables
  9.5.2.1(A), 9.5.2.1(B), 9.5.2.3 reproduced as image assets above).
