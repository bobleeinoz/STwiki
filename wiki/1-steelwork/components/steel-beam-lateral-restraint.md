---
title: Beam lateral restraint — full lateral restraint, restraint types, critical flange, restraint forces
category: 1-steelwork
tags: [bending, lateral-restraint, full-lateral-restraint, critical-flange, restraint-forces, fly-brace, segments]
standards: [AS 4100:2020 Cl 5.3, AS 4100:2020 Cl 5.4, AS 4100:2020 Cl 5.5, AS 4100:2020 Cl 5.8]
status: draft
reviewed: 2026-09-13
---

# Beam lateral restraint

> Scope: AS 4100:2020 Cl 5.3 (segments, full lateral restraint and the
> deemed-to-comply segment length limits), Cl 5.4 (fully / partially /
> rotationally / laterally restrained cross-sections, restraint design
> forces), Cl 5.5 (critical flange), Cl 5.8 (separators and diaphragms).
> Feeds the F/P/L/U end-condition codes used for effective length on
> [[steel-beam-member-moment-capacity]].

## Summary

`[code]` A **segment** is the length between adjacent fully or partially
restrained cross-sections, or between an unrestrained end and the next
fully/partially restrained section (Cl 5.3.1, 1.3.64). A segment with **full
lateral restraint** has `M_b = M_s` at its critical section (Cl 5.3.1).

`[code]` A cross-section that satisfies none of Cl 5.4.2.1–5.4.2.4 is
**unrestrained** (Cl 5.4.1), unless the member is designed by buckling
analysis (Cl 5.6.4).

`[code]` Restraint elements are designed for **2.5 % of the critical flange
force** (Cl 5.4.3.1), with the parallel-member reduction of Cl 5.4.3.3.

## Detail

### When a segment has full lateral restraint (Cl 5.3.2)

`[code]` Any one of:

1. **Continuous lateral restraint** at the critical flange with both ends
   fully or partially restrained (Cl 5.3.2.2).
2. **Intermediate lateral restraints** at the critical flange dividing the
   segment into sub-segments, each sub-segment length satisfying
   Cl 5.3.2.4, ends fully or partially restrained (Cl 5.3.2.3).
3. **Full or partial restraint at both ends** with segment length `l`
   within the Cl 5.3.2.4 limit (below).
4. `M_b` from Cl 5.6 ≥ `M_s` at the critical section (Cl 5.3.2.1).

`[code]` **Cl 5.3.2.4 length limits** (segment with F or P at both ends):

| Section type | Limit |
|---|---|
| Equal-flanged I-section | `l/r_y ≤ (80 + 50β_m) · sqrt(250/f_y)` |
| Equal-flanged channel | `l/r_y ≤ (60 + 40β_m) · sqrt(250/f_y)` |
| I-section with unequal flanges | `l/r_y ≤ (80 + 50β_m) · sqrt(2ρ A d_f / (2.5 Z_ex)) · sqrt(250/f_y)` |
| RHS / SHS | `l/r_y ≤ (1800 + 1500β_m) · (b_f/b_w) · (250/f_y)` |
| Angle section | `l/t ≤ (210 + 175β_m) · sqrt(b_2/b_1) · (250/f_y)` |

with `ρ = I_cy/I_y`, `d_f` = distance between flange centroids, `b_f`, `b_w`
= flange width and web depth, `b_1`, `b_2` = greater and lesser leg lengths,
`t` = angle thickness. `β_m` is taken as: (a) −1.0; (b) −0.8 for segments
with transverse loads; or (c) the ratio of smaller to larger end moment
(positive in reverse curvature) for segments without transverse loads.

`[derived]` Worked feel: Grade 300 UB with `β_m = −1` → `l/r_y ≤ 30·0.913 =
27.4`. For a 410UB54 (`r_y = 38.6 mm`) that is only ~1.06 m — the
deemed-to-comply limit is short; most practical beams need the Cl 5.6
calculation or continuous restraint from a deck. With `β_m = +1` (reverse
curvature) the limit is `130·0.913 = 119` → ~4.6 m.

### Restraint classification at a cross-section (Cl 5.4.2)

![[as4100-fig-5.4.1-unrestrained-cross-sections.png]]
*Figure 5.4.1 — unrestrained cross-sections: no critical-flange restraint, no twist restraint (AS 4100:2020).*

`[code]` **Fully restrained (F)** — Cl 5.4.2.1: either (a) lateral deflection
of the critical flange is effectively prevented **and** twist rotation is
effectively or partially prevented; or (b) lateral deflection of some other
point is effectively prevented **and** twist rotation is effectively
prevented.

![[as4100-fig-5.4.2.1-fully-restrained-cross-sections.png]]
*Figure 5.4.2.1 — fully restrained cross-sections: (a) critical flange restraint + effective twist restraint; (b) critical flange restraint + partial twist restraint; (c) non-critical flange restraint + effective twist restraint (AS 4100:2020).*

`[code]` **Partially restrained (P)** — Cl 5.4.2.2: lateral deflection of a
point other than the critical flange is effectively prevented, and twist
rotation is partially prevented.

![[as4100-fig-5.4.2.2-partially-restrained-cross-sections.png]]
*Figure 5.4.2.2 — partially restrained cross-sections (AS 4100:2020).*

`[code]` **Rotationally restrained** — Cl 5.4.2.3: an F or P section whose
restraint also provides significant restraint against lateral rotation of
the critical flange out of the bending plane (used for `k_r`).

![[as4100-fig-5.4.2.3-rotationally-restrained-cross-sections.png]]
*Figure 5.4.2.3 — rotationally restrained cross-sections (AS 4100:2020).*

`[code]` **Laterally restrained (L)** — Cl 5.4.2.4: within a segment whose
ends are F or P, a section where the restraint prevents lateral deflection
of the critical flange but not twist. Sections in a segment with one end
unrestrained cannot be taken as L.

![[as4100-fig-5.4.2.4-laterally-restrained-cross-section.png]]
*Figure 5.4.2.4 — laterally restrained cross-section (AS 4100:2020).*

`[derived]` Reading the figures for common industrial details:

| Detail | Classification (typical) |
|---|---|
| Beam bearing on a stiff support with web stiffener, or bolted to a stiff column flange at both flanges | F |
| Purlin/girt bolted to the critical (top) flange with flexible cleat, no fly brace | F if twist partially prevented via a moment-capable cleat; otherwise L |
| Fly brace from purlin to bottom (critical) flange of a rafter in hogging | F (critical flange restrained, partial twist) |
| Purlin on top flange while the bottom flange is critical (hogging near haunch), no fly brace | P at best (non-critical flange restraint + partial twist) |
| Beam on a slotted/pinned seat with no twist restraint | Unrestrained |

Confirm against Figures 5.4.2.1–5.4.2.4 for each actual detail.

### Restraining elements — design forces (Cl 5.4.3)

`[code]`
- **Lateral deflection restraint** (5.4.3.1): design for a transverse force
  at the critical flange of **0.025 × the maximum critical-flange force** in
  the adjacent segments/sub-segments. Where restraints are more closely
  spaced than needed to make `M* = φM_b`, group actual restraints into
  equivalent restraints that just achieve `M* = φM_b` and design each
  group for 2.5 % of the equivalent adjacent segment flange force.
- **Twist restraint** (5.4.3.2): effective if designed to transfer 0.025 ×
  the maximum critical-flange force from any unrestrained flange to the
  lateral restraint; partial if it provides elastic restraint without
  rotational slip. Unstiffened webs may form part of the restraint if
  connected to prevent rotational slip. Any restraint permitting rotational
  slip is ineffective. Stiffness effects: App H, Cl H.5.1.
- **Parallel restrained members** (5.4.3.3): a line of restraints across
  parallel members — each element designed for 0.025 × flange force of the
  connected member + 0.0125 × the sum of flange forces of the members
  beyond, considering no more than seven members.
- **Lateral rotation restraint** (5.4.3.4): deemed effective if the
  restraining element's in-plane flexural stiffness is comparable to the
  restrained member's. A segment with full lateral restraint may provide
  rotational restraint to a laterally continuous adjacent segment; a segment
  without full lateral restraint cannot (unless designed by buckling
  analysis). Stiffness effects: App H, Cl H.5.2.

`[derived]` Critical flange force for the 2.5 % rule is usually taken as
`M*/d_f` (moment over distance between flange centroids) at the restraint,
or conservatively `φM_b/d_f`; the standard says "maximum force in the
critical flanges of the adjacent segments", so take the larger of the two
adjacent segments.

### Critical flange (Cl 5.5)

`[code]` The flange that would deflect farthest during buckling with no
restraint at that section (5.5.1). Segments restrained at both ends: the
**compression flange** (5.5.2). Segments with one end unrestrained
(cantilevers): the **top flange** when gravity dominates; under dominant
wind, the **exterior** flange for external pressure or internal suction and
the **interior** flange for internal pressure or external suction (5.5.3).

### Separators and diaphragms (Cl 5.8)

`[code]` Where two or more I-sections or channels side by side act as a
unit: separators (spacers + through bolts) transmit only transverse forces
and a design transverse force `Q* ≥ 0.025 ×` the maximum design compression
flange force of any member in the unit, shared equally between separators;
diaphragms are required where vertical as well as transverse forces are to
be transferred, proportioned for the applied forces plus `Q*` and resulting
shears.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[steel-beam-member-moment-capacity]] — `k_t`, `k_l`, `k_r` and the
  F/P/L/U end codes derived from this page.
- [[steel-beam-section-moment-capacity]] — `M_s`, critical section.
- [[steel-compression-member-capacity]] — Cl 6.6 restraint rules for
  compression members (2.5 % rule analogue).
- [[steel-connection-design-requirements]] — Cl 9.1.4 minimum design
  actions for restraint connections.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Cl 5.3–5.5, 5.8
  (pp. 56–62, 69–70). Figures 5.4.1, 5.4.2.1–5.4.2.4 reproduced in
  `wiki/1-steelwork/assets/`.
