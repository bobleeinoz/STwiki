---
title: AS 3774 eccentric discharge flow loads (Cl 6.5)
category: 0-standards
tags: [as3774, silo, eccentric-flow, wall-pressure]
standards: [AS 3774:1996 Cl 6.5]
status: draft
reviewed: 2026-10-02
---

# AS 3774 eccentric discharge flow loads

> Scope: AS 3774:1996 Cl 6.5 — unsymmetrical wall pressures from eccentric
> outlets, feeders with non-uniform draw-off, internal features and eccentric
> filling. Eccentric *filling* initial pressures (Cl 6.4) are on
> [[as3774-silo-wall-pressures-initial-and-flow]].

## Summary

`[code]` Eccentric flow always gives non-uniform circumferential pressure
(Cl 6.5.1). An outlet eccentricity e_o < 0.1 d_c is treated as no effective
eccentricity. The eccentricity axis is the horizontal line through the
container axis and the eccentric outlet; the side with the outlet is the
**near side**, the remote side the **far side**. The extra pressures are
added to / subtracted from the Cl 6.3 flow pressures (Cl 6.5.2.1).
Geometries not covered need a rational analysis.

## Detail

### Pressure increase on the far side (Cl 6.5.2.2)

`[code]` Centred at height h_D = (0.5 d_c + e_o) tan φ_i (upper φ_i) above the
outlet and extending over height d_c: maximum increase
p_ef,max = p_nf (e_o/d_c − 0.1) ≥ 0 (Eq 6.5.2.2(2)). Circular containers: over
half the circumference, p_ef = p_ef,max (−cos β) for β 90°-270° (origin on the
near-side eccentricity axis) and zero for −90° to 90°. Rectangular: constant
p_ef,max over the far wall.

### Pressure reduction on the near side (Cl 6.5.2.3)

`[code]` Over height d_c from the outlet level, the reduction is
p_ef,red = 1.5 p_nf (e_o/d_c − 0.1) (Eq 6.5.2.3(2)). For circular containers it is
constant over a distance d_e/2 either side of the near-side axis, with
d_e = 1.83 d_c (1 − 1.43 e_o/d_c) (Eq 6.5.2.3(1)), or equivalently an angular
range β_e = 105 − 150 e_o/d_c degrees (Eq 6.5.2.3(3)).

![[as3774-fig-6.12-eccentric-flow-pressure-distribution.png]]
*Figure 6.12 — eccentric flow pressure distribution: (a) flow zones, (b) circumferential variation (decreased/increased pressure, β_e), (c) height variation (reduced near side, increased far side, h_D, d_c/2).*

`[derived]` Both increase and reduction apply together on a circular wall; the
design check should use the combination that is adverse for the member (e.g.
increase for hoop/bending of the far wall, reduction paired with the increase
for the net out-of-balance on shell buckling and the supporting structure).

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as-3774-1996-loads-on-bulk-solids-containers]]
- [[as3774-silo-wall-pressures-initial-and-flow]]
- [[as3774-container-classification-and-bulk-solid-properties]] — outlet types H3/H4 and flow modes B5.

## Sources

- `raw/0-standards/AS 3774-reprint.pdf` — AS 3774—1996 incl. Amdt 1, 2 (1998), Cl 6.5.
