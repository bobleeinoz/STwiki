---
title: Tendon properties and loss of prestress
category: 2-concrete
tags: [material-properties, tendons, prestress, prestress-losses]
standards: [AS 3600:2018 Cl 3.3, AS 3600:2018 Cl 3.4]
status: draft
reviewed: 2026-09-12
---

# Tendon properties and loss of prestress

> Scope: strength, elastic modulus, stress-strain behaviour and relaxation of
> prestressing tendons (Cl 3.3), and the immediate and time-dependent loss of
> prestress calculation (Cl 3.4).

## Summary

`[code]` Tendon properties (Cl 3.3) mirror the concrete/reinforcement
pattern: a standard value or table entry, or determine by test to
AS/NZS 4672.1/.2. Prestress loss (Cl 3.4) is the sum of immediate losses
(elastic shortening, friction, anchoring, other) plus time-dependent losses
(shrinkage, creep, relaxation, other) of the concrete/tendon system.

## Detail

### Tendon strength and stiffness (Cl 3.3.1–3.3.3)

`[code]` Characteristic minimum breaking strength `fpb` for common tendon
types (as-drawn wire, stress-relieved wire, ordinary/compacted strand,
hot-rolled bar) is given in Table 3.3.1 — a materials data
table by nominal diameter, area and breaking load. For dimensions outside
the table, refer to AS/NZS 4672.1 directly.

![[as3600-table-3.3.1-tensile-strength-wire-strand-bar-1.png]]
![[as3600-table-3.3.1-tensile-strength-wire-strand-bar-2.png]]
*Table 3.3.1 — tensile strength of commonly used wire, strand and bar, by
nominal diameter/area and breaking load (AS 3600:2018).* Yield strength `fpy` is the 0.1%
proof stress per AS/NZS 4672.1, or by test; absent test data, AS 3600 gives
a fixed fraction of `fpb` per tendon type (as-drawn wire, stress-relieved
wire, strand, hot-rolled super-grade bar, hot-rolled ribbed bar — five
different fractions). `[derived]` Treat the exact fractions as needing direct
clause confirmation; they read as a short list rather than a large table but
weren't independently re-verified digit-by-digit here.

`[code]` Elastic modulus `Ep` is either a fixed value per tendon type (each
with its own tolerance band, e.g. wire vs. strand have different nominal `Ep`
and scatter), or by test. The clause explicitly warns modulus can vary ~10%
and more again when multiple wires/strands are stressed as a single cable —
relevant to elongation-based stressing checks on site. Stress-strain curve:
by test only (no default form offered here, unlike concrete/reinforcement).

### Relaxation (Cl 3.3.4)

`[code]` Basic relaxation `Rb` (after 1000 hours at 20°C, from a stated
initial force fraction of `fpb`) is determined per AS/NZS 4672.1. Design
relaxation `R = k7·k8·k9·Rb`, where `k7` depends on time since prestressing
(a log-time form), `k8` depends on tendon stress as a proportion of `fpb`
(read from Figure 3.3.4.3, reproduced below — it's a chart, not a formula),
and `k9` depends on average annual temperature (linear in `T/20`, floored at
1.0). Elevated-temperature curing effects must be considered separately.

![[as3600-fig-3.3.4.3-relaxation-k8-coefficient.png]]
*Figure 3.3.4.3 — relaxation coefficient `k8` vs. tendon stress as a
proportion of `fpb` (AS 3600:2018).*

### Loss of prestress (Cl 3.4)

`[code]` Cl 3.4.1: total loss = immediate loss (Cl 3.4.2) + time-dependent
loss (Cl 3.4.3), each estimated by summing applicable sub-causes. Above 40°C
sustained operating temperature, losses must be established from test data —
the standard model doesn't cover that regime (Note: elevated-temperature
tendon losses are significantly higher; specialist literature recommended).

**Immediate losses (Cl 3.4.2):**
- Curing conditions (3.4.2.2) — ambient-cured members use the Cl 3.3.4.3
  design relaxation directly; elevated-temperature (e.g. steam) curing shifts
  some or all of that relaxation into the *immediate* loss category instead
  of time-dependent.
- Elastic deformation of concrete (3.4.2.3) — based on `Ec` at the age of
  transfer.
- Friction (3.4.2.4) — stress at distance `a` from the jacking end follows an
  exponential decay `σpa = σpj·e^(−μ·α_tot − β·Lpa)`, where `μ` is a
  friction-curvature coefficient (own-words: ranges by duct/sheathing type —
  greased-and-wrapped vs. bright/zinc-coated metal sheathing vs. flat metal
  duct, each with its own value or range) and `β` is a wobble coefficient
  banded by duct internal diameter and whether it contains bars or
  strand/wire. `[derived]` The exact μ/β numeric ranges are short enumerated
  lists in the clause rather than a table format, but are still empirical
  code-specific constants — confirm the specific figure against Cl 3.4.2.4
  before using it in a stressing calc rather than relying on this summary.
  Friction losses must be verified on site during stressing.
- Anchoring (3.4.2.5) — seating/draw-in loss at transfer of force from jack to
  anchorage; must be checked on site with adjustment as required.
- Other (3.4.2.6) — formwork deformation (precast), temperature differentials
  during heat treatment or between stressing and casting, joint deformation
  in segmental precast, and sustained temperatures above 40°C.

**Time-dependent losses (Cl 3.4.3):**
- Shrinkage (3.4.3.2) — loss = `Ep·εcs`, modified for reinforcement
  restraint; where reinforcement is distributed so its restraint effect is
  mainly axial, the loss is reduced by a factor depending on the
  reinforcement-to-gross-area ratio (`1 + 15·As/Ag` in the denominator).
  `εcs` from [[concrete-properties-of-concrete]] Cl 3.1.7.2.
- Creep (3.4.3.3) — loss = `Ep·φcc`, with `φcc = 0.8·φcc·σci/Ec` (own-words:
  scaled by the sustained concrete stress at the tendon centroid under
  initial prestress plus sustained service loads), valid provided sustained
  stress at the tendon level never exceeds 0.5×`f'c`.
- Relaxation (3.4.3.4) — the *design* relaxation (Cl 3.3.4.3) is modified to
  account for the interaction with shrinkage and creep loss, since relaxation
  reduces as the tendon stress itself drops from those other losses.
- Other (3.4.3.5) — segmental-joint deformation, and increased creep from
  frequently repeated loads.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[concrete-properties-of-concrete]] — `εcs`, `φcc`, `Ec` feeding the loss
  calculations here.
- [[concrete-limit-state-design-basis]] — Cl 2.5.2.2 prestress load
  combinations at transfer.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clauses 3.3, 3.4 (Table
  3.3.1 and Figure 3.3.4.3 reproduced as image assets above).
