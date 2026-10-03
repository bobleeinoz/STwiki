---
title: Suggested deflection limits for beams and portal frames
category: 0-standards
tags: [deflection, serviceability, portal-frame, beam-deflection, crane-runway]
standards: [AS 4100:2020 App B]
status: draft
reviewed: 2026-09-13
---

# Suggested deflection limits

> Scope: AS 4100:2020 Appendix B (informative) — suggested vertical
> deflection limits for beams (Table B.1) and suggested horizontal
> deflection limits for industrial portal-frame buildings, including
> gantry-crane cases. Referenced from Cl 3.5.3 as guidance for the
> mandatory (but not itself numerically prescriptive) serviceability
> deflection-limit requirement.

## Summary

`[code]` Appendix B is **informative** — Cl 3.5.3 requires deflection
limits "appropriate to the structure", and this appendix is the suggested
starting point (or, alternatively, AS/NZS 1170.0:2002 Appendix C).

## Detail

### Suggested vertical deflection limits for beams (Cl B.1, Table B.1)

![[as4100-table-B.1-deflection-limits.png]]
*Table B.1 — suggested limits on calculated vertical deflections of beams (AS 4100:2020).*

`[code]`

| Beam type | Deflection considered | Span limit Δ/l | Cantilever limit Δ/l |
|---|---|---|---|
| Beam supporting masonry partitions | Deflection occurring **after** partition addition/attachment | ≤ 1/500 (movement minimised) or ≤ 1/1000 (otherwise) | ≤ 1/250 (movement minimised) or ≤ 1/500 (otherwise) |
| All beams | Total deflection | ≤ 1/250 | ≤ 1/125 |

Suggested limits may not safeguard against **ponding**. For cantilevers,
the `Δ/l` values apply provided the effect of support rotation is included
in calculating `Δ`.

### Suggested horizontal deflection limits — industrial portal frames (Cl B.2)

`[code]` **Relative** deflection between adjacent frames at eaves level,
under the AS/NZS 1170.0 + AS/NZS 1170.2 serviceability wind load:

| Building condition | Limit |
|---|---|
| Steel/aluminium clad, no ceilings, no internal partitions on external walls, no gantry cranes | Frame spacing / 200 |
| As above, **with gantry cranes operating** | Frame spacing / 250 |
| As first case but external masonry walls supported by steelwork instead of sheeting | Frame spacing / 200 |

`[code]` **Absolute** horizontal deflection of a frame, same wind load:

| Building condition | Limit |
|---|---|
| Steel/aluminium clad, no ceilings, no partitions on external walls, no gantry cranes | Eaves height / 150 |
| As above, **with gantry cranes operating** | Crane rail height / 250 |
| As first case but masonry walls on steelwork instead of sheeting | Eaves height / 250 |

Alternatively, AS/NZS 1170.0:2002 Appendix C guidance may be used where
appropriate.

`[derived]` The gantry-crane rows are the ones most directly relevant to
mining/material-handling steelwork: an overhead-crane-served workshop or
maintenance bay, or a conveyor transfer building with a travelling gantry,
should be checked against the **crane rail height/250** absolute limit and
the **frame spacing/250** relative limit, not the more relaxed no-crane
values — excess frame sway under wind can bind or derail the crane
independent of the crane's own AS 1418 design.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as4100-limit-state-design-basis]] — Cl 3.5.3 deflection-limit
  requirement this Appendix supports.
- [[as4100-structural-analysis-methods]] — SLS deflection is calculated by
  the Cl 4.4.2.1 first-order method with amplification factors = 1.0.
- [[as3600-limit-state-design-basis]] — AS 3600 serviceability
  counterpart.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Appendix B
  (pp. 185–186). Table B.1 reproduced in `wiki/0-standards/assets/`.
