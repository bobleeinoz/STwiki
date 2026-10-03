---
title: Stress development of tendons and coupling
category: 0-standards
tags: [tendons, transmission-length, development-length, anchorages, coupling]
standards: [AS 3600:2018 Cl 13.3, AS 3600:2018 Cl 13.4]
status: draft
reviewed: 2026-09-16
---

# Stress development of tendons and coupling

> Scope: AS 3600 Cl 13.3 (transmission and development length of
> pretensioned tendons, post-tensioned anchorage development) and Cl 13.4
> (coupling of tendons).

## Summary

`[code]` Cl 13.3.1 models a pretensioned tendon's force build-up as
bi-linear: a **transmission length** (`Lpt`, Cl 13.3.2.1) over which
effective prestress is developed, followed by a **total development length**
(`Lp`, Cl 13.3.2.2) over which the additional stress up to ultimate is
developed — in the absence of substantiated test data.

## Detail

### Transmission length of pretensioned tendons (Cl 13.3.2.1)

`[code]` `Lpt` is read from Table 13.3.2 by tendon type and concrete strength
at transfer (`f'cp`), independent of the tendon's effective prestress. A
fully unstressed zone of length `0.1 Lpt` is assumed to develop at the tendon
end with time, without shifting the inner end of the transmission length.

![[as3600-table-13.3.2-transmission-length-pretensioned-tendons.png]]
*Table 13.3.2 — minimum transmission length for pretensioned tendons, by
tendon type and concrete strength at transfer (AS 3600:2018).*

| Tendon type | `Lpt`, `f'cp ≥ 32 MPa` | `Lpt`, `f'cp < 32 MPa` |
| --- | --- | --- |
| Indented wire | `100 db` | `175 db` |
| Crimped wire | `70 db` | `100 db` |
| Ordinary/compact strand | `60 db` | `60 db` |

### Development length of pretensioned strand and wire (Cl 13.3.2.2–13.3.2.4)

`[code]` Seven-wire pretensioned strand at ultimate: `Lp = 0.145(σpu −
0.67σp.ef) db ≥ 60 db` (stresses in MPa, `σp.ef` = effective stress after all
losses). Embedment shorter than `Lp` is permitted provided the design stress
at that section stays within the bi-linear relationship defined by this
clause and Cl 13.3.2.1. De-bonded strand carrying tension per Cl 8.6.2/9.4.2
in its development length uses `2 Lp`.

`[code]` Pretensioned indented/crimped wire: bonded length ≥`2.25×` the
Table 13.3.2 transmission length. Untensioned strand or wire: development
length ≥`2.5×` the transmission length of a tendon stressed to `fpb`
(Table 3.3.1).

### Post-tensioned anchorages and coupling (Cl 13.3.3, Cl 13.4)

`[code]` Anchorages for post-tensioned tendons must be capable of developing
`fpb` in the tendon; anchorages for **unbonded** tendons must additionally
sustain cyclic loading.

`[code]` Couplers (Cl 13.4) must develop ≥95% of the tendon's characteristic
minimum breaking force, and must be enclosed in grout-tight housings to
permit duct grouting.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as3600-properties-of-tendons-and-prestress-losses]] — Cl 3.3/3.4,
  `fpb`, `Table 3.3.1` and the prestress-loss calculations feeding `σp.ef`.
- [[as3600-development-length-of-reinforcement]] — Cl 13.1, the parallel
  bar-development framework.
- [[as3600-construction-reinforcement-and-tendons]] — Cl 17.3, fixing,
  tensioning and grouting requirements for the ducts/anchorages/tendons this
  clause assumes.
- [[as3600-diaphragm-design]] — Cl 15.4.3, applies Section 13 development
  rules (including this page) to diaphragm reinforcement/tendons.

## Sources

- `raw/0-standards/AS_3600-2018-Reprint-Cut.pdf`, Clauses 13.3–13.4.
