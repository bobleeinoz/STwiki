---
title: Load testing of structures or elements — proof and prototype testing
category: 1-steelwork
tags: [testing, proof-testing, prototype-testing, acceptance-criteria, test-load]
standards: [AS 4100:2020 Section 17]
status: draft
reviewed: 2026-09-13
---

# Load testing of structures or elements

> Scope: AS 4100:2020 Section 17 — the alternative-to-calculation testing
> route referenced from Cl 3.6 (strength/serviceability by load testing),
> Cl 14.1 and Cl 15.1.1 (accepting an otherwise-nonconforming fabricated or
> erected item by test). Covers proof testing (one specific unit) and
> prototype testing (a nominally identical class of units), test load
> determination, and acceptance criteria.

## Summary

`[code]` Structures designed to AS 4100 are **not required** to be tested;
testing is an alternative to calculation, or a way to accept an item that
otherwise fails a fabrication/erection requirement (Cl 17.1.2). **Proof
test**: test load = the Cl 3.2.3 design load for the relevant limit state,
unmodified (Cl 17.4.2). **Prototype test**: test load = the design load ×
a Table 17.5.2 variability factor (1.2–1.5, reducing as more similar units
are tested), unless justified lower by reliability analysis (Cl 17.5.2).

## Detail

### Scope and circumstances (Cl 17.1)

`[code]` Scope (17.1.1): applies to proof tests and prototype tests of
complete structures, sub-structures, individual members or connections.
**Not** applicable to testing of structural models, nor to establishing
general design criteria or data. Circumstances (17.1.2): structures
designed to this Standard need not be tested; tests may replace
calculation or become necessary in special circumstances (e.g. a novel
detail, or accepting a nonconforming fabricated/erected item per Cl 14.1/
15.1.1).

### Definitions (Cl 17.2)

`[code]` **Proof testing**: test loads applied to a structure,
sub-structure, member or connection to ascertain the structural
characteristics of **only that one unit** under test. **Prototype
testing**: test loads applied to one or more units to ascertain the
characteristics of **that class** of nominally identical units.

### Test requirements (Cl 17.3)

`[code]` Test load determined per Cl 17.4.2 (proof) or 17.5.2 (prototype).
Loading devices calibrated; care taken that the loading system applies no
artificial restraint. Test load applied at as uniform a rate as
practicable. Force distribution and duration must represent those the
structure is deemed subject to under Section 3. Deformations recorded at
minimum: (a) before test-load application; (b) after application; (c) after
removal.

### Proof testing (Cl 17.4)

`[code]` Application (17.4.1): determines whether **that particular**
structure/sub-structure/member/connection complies with strength or
serviceability requirements. Test load (17.4.2): equal to the Cl 3.2.3
design load for the relevant limit state (no variability factor).

`[code]` Acceptance criteria (17.4.3): (a) **strength** — sustain the
strength-limit-state test load for **≥ 15 min**; then inspect for damage,
review its effects, and carry out repairs if necessary; (b)
**serviceability** — maximum deformation under the SLS test load stays
within the structure's appropriate serviceability limits.

### Prototype testing (Cl 17.5)

`[code]` Test specimen (17.5.1): materials and fabrication conform to
Sections 2 and 14; any additional manufacturing-specification requirements
are met; erection method simulates production erection.

`[code]` Test load (17.5.2): the Cl 3.2.3 design load for the relevant
limit state, **multiplied by** the Table 17.5.2 factor — unless a
reliability analysis justifies a smaller value.

`[code]` Table 17.5.2 — variability factors:

| No. of similar units tested | Strength limit state | Serviceability limit state |
|---|---|---|
| 1 | 1.5 | 1.2 |
| 2 | 1.4 | 1.2 |
| 3 | 1.3 | 1.2 |
| 4 | 1.3 | 1.1 |
| 5 | 1.3 | 1.1 |
| 10 | 1.2 | 1.1 |

`[derived]` The factor decays with more tested units because testing more
nominally-identical units reduces the statistical uncertainty about the
worst-case unit in the production population — the same logic as a
characteristic-value/confidence-interval argument, applied here as a
simple lookup rather than a full reliability calculation.

`[code]` Acceptance criteria (17.5.3): (a) **strength** — sustain the
strength-limit-state test load for **≥ 5 min** (shorter than the 15 min
proof-test duration, reflecting the higher test load already applied);
(b) **serviceability** — as for proof testing.

`[code]` Acceptance of production units (17.5.4): production-run units must
be similar in **all respects** to the tested unit(s).

### Report of tests (Cl 17.6)

`[code]` The test report must contain, beyond the results themselves: a
clear statement of test conditions (loading method, deflection measurement
method), other relevant data, and an explicit statement of whether the
tested structure/part satisfies the acceptance criteria.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[steel-limit-state-design-basis]] — Cl 3.6 routing to this Section as an
  alternative to Cl 3.4/3.5 calculation.
- [[steel-fabrication-and-erection-requirements]] — Cl 14.1, 15.1.1
  accept-by-test provisions for nonconforming fabricated/erected items.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Section 17
  (pp. 181–183).
