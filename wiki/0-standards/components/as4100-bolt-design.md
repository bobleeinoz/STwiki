---
title: Bolt design — strength limit states, slip resistance and bolt groups
category: 0-standards
tags: [bolts, bolting-category, shear, tension, prying, slip-factor, friction-connection, bolt-group, instantaneous-centre]
standards: [AS 4100:2020 Cl 9.2, AS 4100:2020 Cl 9.3]
status: draft
reviewed: 2026-09-13
---

# Bolt design

> Scope: AS 4100:2020 Cl 9.2 (bolting categories, Table 9.2.1; bolt shear,
> tension, combined shear+tension strength limit states; ply bearing;
> filler plates; bolt slip/SLS design) and Cl 9.3 (bolt-group analysis:
> in-plane, out-of-plane, combined). Pins and detailing limits are on
> [[as4100-bolt-and-pin-detailing]]; general connection provisions on
> [[as4100-connection-design-requirements]].

## Summary

`[code]` `φ = 0.80` for bolt shear, tension and combined; `φ = 0.90` for
ply bearing; `φ = 0.80` for a bolt group (Table 3.4); `φ = 0.7` for the
friction-connection SLS check (Cl 3.5.5).

`[code]` `V_f = 0.62 f_uf k_rd k_r (n_n A_c + n_x A_o)` (shear, Cl 9.2.2.1);
`N_tf = A_s f_uf` (tension, Cl 9.2.2.2); combined shear+tension:
`(V*_f/φV_f)² + (N*_tf/φN_tf)² ≤ 1.0` (Cl 9.2.2.3); ply bearing:
`V_b = min(3.2 d_f t_p f_up, a_e t_p f_up)` (Cl 9.2.2.4).

## Detail

### Bolting categories (Cl 9.2.1, Table 9.2.1)

`[code]`

| Category | Bolt Standard | Grade | Tensioning | Min. tensile strength f_uf |
|---|---|---|---|---|
| 4.6/S | AS 1111, AS 1110 (series) | 4.6 | Snug tight | 400 MPa |
| 8.8/S | AS/NZS 1252.1, AS 1110 (series) | 8.8 | Snug tight | 830 MPa |
| 8.8/TB | AS/NZS 1252.1 | 8.8 | Full tensioning | 830 MPa |
| 8.8/TF | AS/NZS 1252.1 | 8.8 | Full tensioning | 830 MPa |
| 10.9/S | AS/NZS 1252.1 | 10.9 | Snug tight | 1040 MPa |
| 10.9/TB | AS/NZS 1252.1 | 10.9 | Full tensioning | 1040 MPa |
| 10.9/TF | AS/NZS 1252.1 | 10.9 | Full tensioning | 1040 MPa |

`f_uf` is per AS 4291.1:2015 except grade 8.8 bolts < 16 mm diameter
(`f_uf = 800 MPa`). Bolts to AS 1110/AS 1111 series are **not suitable for
full tensioning**. Post-manufacture treatment of high-strength bolts may
adversely affect material properties. Other property classes to AS 1110,
AS 1111 and AS/NZS 1559 may also be designed per this Clause and Cl 9.3.
`TF` = friction-type (slip-critical); `TB` = bearing-type, fully tensioned
(no slip control assumed); `S` = snug-tight bearing-type.

`[practice]` The ASI *Design Capacity Tables for Structural Steel, Vol 1:
Open Sections* (DCT/V1/03-1999, Table T9.1) lists the same four category
names in common use at the time — 4.6/S (commercial, AS/NZS 1111, min.
tensile 400 MPa), 8.8/S, 8.8/TF and 8.8/TB (high-strength structural,
AS/NZS 1252, min. tensile 830 MPa, min. yield 660 MPa) — consistent with
the table above; it predates the 10.9 categories and the AS/NZS 1252.1:2016
alignment noted in [[as-4100-2020-steel-structures]]. It also tabulates
`V_b = 3.2 d_f t_p f_up` (local bearing failure) and `V_b = a_e t_p f_up`
(end-plate tearout failure) as the ply-bearing checks, matching the current
Cl 9.2.2 bearing provisions on this page. See
[[asi-design-capacity-tables-vol1-open-sections]] for the source register.

![[dct-table-t9.1-bolt-types-and-categories.png]]
*DCT Vol 1 Table T9.1 — bolt types and bolting categories (source:
DCT/V1/03-1999, p. 9-3).*

### Bolt strength limit states (Cl 9.2.2)

`[code]` **Shear** (9.2.2.1): `V*_f ≤ φV_f`, `φ = 0.80`,

`V_f = 0.62 f_uf k_rd k_r (n_n A_c + n_x A_o)`

- `k_rd` (ductility reduction for Grade 10.9 threads in the shear plane):
  1.0 for Grade 4.6/8.8, or Grade 10.9 with threads excluded from the shear
  plane; **0.83** for Grade 10.9 with threads intercepting the shear plane.
- `k_r` — bolted lap connection length reduction (Table 9.2.2.1), else 1.0.
- `n_n`, `n_x` = number of shear planes with / without threads intercepting
  the plane; `A_c` = minor diameter area (AS 1275); `A_o` = nominal plain
  shank area.

`[code]` Table 9.2.2.1 — lap connection reduction `k_r`:

| Lap length l_j (mm) | k_r |
|---|---|
| < 300 | 1.0 |
| 300 ≤ l_j ≤ 1300 | `1.075 − l_j/4000` |
| > 1300 | 0.75 |

`[code]` **Tension** (9.2.2.2): `N*_tf ≤ φN_tf`, `φ = 0.80`,
`N_tf = A_s f_uf` (`A_s` = tensile stress area, AS 1275).

`[code]` **Combined shear and tension** (9.2.2.3):
`(V*_f/φV_f)² + (N*_tf/φN_tf)² ≤ 1.0`.

`[code]` **Ply in bearing** (9.2.2.4): `V*_b ≤ φV_b`, `φ = 0.90`,

`V_b = 3.2 d_f t_p f_up` — Eq 9.2.2.4(1)

and, for a ply component of force acting towards an edge, the **lesser**
of that and

`V_b = a_e t_p f_up` — Eq 9.2.2.4(2)

`d_f` = bolt diameter, `t_p` = ply thickness, `f_up` = ply tensile strength,
`a_e` = distance from the hole edge to the ply edge (measured in the force
direction) plus half the bolt diameter — an adjacent bolt hole counts as
the "edge".

`[code]` **Filler plates** (9.2.2.5): for fillers > 6 mm and < 20 mm thick,
reduce `V_f` (Cl 9.2.2.1) by `[1 − 0.0154(t − 6)]`, `t` = total filler
thickness (incl. paint film) up to 20 mm. Fillers must extend beyond the
connection with enough bolts to distribute the design force over the
combined connected-element + filler cross-section. Multi-shear-plane
connections with more than one filler: use the maximum filler thickness on
any shear plane the bolt passes through.

### Bolt serviceability limit state — friction connections (Cl 9.2.3)

`[code]` For 8.8/TF or 10.9/TF bolts where SLS slip must be limited, a bolt
subject only to shear in the plane of the interfaces: `V*_sf ≤ φV_sf`,
`φ = 0.7` (Cl 3.5.5),

`V_sf = μ n_ei N_ti k_h` — Eq 9.2.3.1

- `μ` = slip factor (9.2.3.2): **0.35** for clean "as-rolled" surfaces;
  otherwise from test evidence (the [[as4100-slip-factor-test-procedure]]
  Appendix J test is deemed satisfactory; EN 1090-2:2018 tabulates common
  surface conditions; the Galvanizers Association of Australia has further
  data).
- `n_ei` = number of effective interfaces.
- `N_ti` = minimum bolt tension at installation (Table 15.2.2.2).
- `k_h` = hole-type factor (Cl 14.3.2): 1.0 standard holes; 0.85 short
  slotted/oversize; 0.70 long slotted.
- 8.8/TF or 10.9/TF connections must be identified on drawings, with the
  required surface treatment and whether masking during painting is needed.
- **Combined shear and tension, friction connection** (9.2.3.3):
  `(V*_sf/φV_sf) + (N*_tf/φN_tf) ≤ 1.0`, `N_tf = N_ti` (not `A_s f_uf` —
  the friction check limits tension to the installed pretension, since
  extra applied tension reduces clamping force and hence slip resistance).
  The strength limit state is separately assessed per Cl 9.2.2.3.

`[derived]` Note the SLS friction check uses a **linear** interaction
(sum ≤ 1.0), unlike the **quadratic** strength-limit-state interaction in
Cl 9.2.2.3 — the two are separate checks with different physical bases
(loss of clamping force vs combined stress at fracture) and both must be
satisfied for a TF bolt carrying both shear and tension.

### Assessment of a bolt group (Cl 9.3)

`[code]` **In-plane loading** (9.3.1) — rigid-plate (instantaneous-centre)
method:
- Connection plates assumed rigid, rotating about an **instantaneous
  centre** of the bolt group.
- Pure couple only: instantaneous centre = bolt-group centroid.
- In-plane shear at the centroid only: instantaneous centre at infinity →
  shear distributed **uniformly** across the group.
- Combined case: superpose the pure-couple and centroidal-shear analyses,
  or use a recognised (rigorous instantaneous-centre) method.
- Each bolt's design shear acts at right angles to, and proportional to,
  its radius from the instantaneous centre.
- Each bolt satisfies Cl 9.2.2.1 with the **bolt-group** `φ` (Table 3.4,
  0.80); ply bearing satisfies Cl 9.2.2.4.

`[code]` **Out-of-plane loading** (9.3.2): design actions per Cl 9.1.3
(equilibrium-based distribution — e.g. a triangular/neutral-axis tension
distribution for a bolted moment end plate); each bolt conforms to
Cl 9.2.2.1, 9.2.2.2, 9.2.2.3 with the bolt-group `φ`; ply bearing per
Cl 9.2.2.4.

`[code]` **Combined in-plane and out-of-plane** (9.3.3): combine Cl 9.3.1
and 9.3.2; each bolt still checked to Cl 9.2.2.1–9.2.2.3 with the
bolt-group `φ`, ply bearing per Cl 9.2.2.4.

`[derived]` The bolt-group `φ = 0.80` (vs `0.80` for an individual bolt in
shear/tension anyway) means, in practice, the group check uses the same
capacity factor as the individual-bolt check — the distinction in Table 3.4
mainly separates "bolt group" from "ply in bearing" (`0.90`), not from a
single bolt.

### Tear-out failure mechanics (ASI Handbook 1 Ch 3.5)

`[practice]` A bolted-ply failure occurs one of two ways: **local bearing**
(ply material piles up in front of the hole around the bolt shank) or
**tear-out** (the ply shears out behind the bolt, towards a free edge or
adjacent hole). Tear-out governs where the end distance `a_e` falls below
about `3.2 d_f` — the length of ply that must shear for the tear-out mode to
control. AS 4100 defines the end distance from the **hole edge**, plus half
the hole diameter, to the ply edge in the direction of the force component
— which is why an adjacent bolt hole can itself act as the "edge" for a
staggered or multi-directional bolt pattern.

![[asi-h1-fig-4-end-plate-tearout-edge-distances.png]]
*Figure 4 — end plate tear-out failure edge distances: `a_e1 = a_e − 1 mm`,
`a_e2 = s_p − 0.5d_h − 1 mm` (ASI Handbook 1, 2007).*

`[practice]` Where a bolt group is loaded by an in-plane moment, the force
on an individual bolt can act in any direction, so the relevant `a_e` must
be resolved into components along each nearby edge (Figure 5); the simple
case of a bolt line loaded straight towards one edge (Figure 6) is the
common design check for, e.g., a web side plate's bottom bolt row.

![[asi-h1-fig-5-6-tearout-force-components.png]]
*Figure 5 (left) — general tear-out force components at an angle `θ` to
the edges; Figure 6 (right) — the simple, single-direction tear-out case
(ASI Handbook 1, 2007).*

### Lap-splice length effect on `k_r` (ASI Handbook 1 Ch 3.6)

`[practice]` The AS 4100 Cl 9.2.2.1 lap-connection reduction factor `k_r`
exists because, while a connection is still elastic, a **longer** bolted lap
splice or brace/gusset connection (Figure 7) distributes shear less
uniformly among its bolts than rigid-plate theory assumes — end bolts carry
more load than interior ones. Ductile yielding of the plies/bolts can
redistribute this towards uniformity, but only if premature bolt or ply
failure doesn't intervene first — for a sufficiently long joint,
redistribution may never fully occur, which is why `k_r` reduces capacity
for `l_j > 300 mm` (Table 9.2.2.1 above). In practice this mainly affects
unusually long bracing cleats and bolted flange splices; `k_r = 1.0` for
most other connections.

![[asi-h1-fig-7-lap-joint-brace-gusset.png]]
*Figure 7 — lap joint and brace/gusset connection geometry defining the
joint length `L_j` used in Table 9.2.2.1 (ASI Handbook 1, 2007).*

### Design capacity reference tables (ASI Handbook 1 Ch 3.6–3.7)

`[practice]` Pre-calculated single-shear/tension design capacities per bolt
designation, for quick reference (values assume `f_uf`/`f_up` as noted;
recalculate for other grades):

![[asi-h1-table-9-commercial-bolt-capacities.png]]
*Table 9 — 4.6/S commercial bolt strength-limit-state capacities: axial
tension `φN_tf`, single-shear `φV_fn` (threads included) and `φV_fx`
(threads excluded) (ASI Handbook 1, 2007). Ply bearing/tear-out capacity
exceeds these shear values for all reasonable ply thickness/end-distance
combinations and does not govern.*

![[asi-h1-table-10-hs-structural-bolt-capacities.png]]
*Table 10 — 8.8/S, 8.8/TB, 8.8/TF high-strength structural bolt
strength-limit-state capacities, plus ply tear-out/bearing capacity for
Grade 250 (`f_up = 410 MPa`) plate at `t_p = 6/8/10/12 mm` and `a_e = 35/
40/45 mm` — scale by `f_up/410` for other ply grades (ASI Handbook 1, 2007).*

`[derived]` These two tables are a convenience only — for a governing
design case, cross-check against the AS 4100 Cl 9.2.2 formulas above rather
than relying on the tabulated `a_e`/`t_p` combinations, which cover only a
sample grid.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as4100-bolt-and-pin-detailing]] — pin capacities, pitch/edge-distance
  limits, hole standards.
- [[as4100-connection-design-requirements]] — minimum design actions, choice
  of fasteners (Cl 9.1.6), combined connections (Cl 9.1.7).
- [[as4100-materials-and-design-strengths]] — bolt/nut/washer product
  standards (Cl 2.3.1).
- [[as4100-fabrication-and-erection-requirements]] — Table 15.2.2.2 minimum
  bolt tension, hole sizes (Cl 14.3.2).
- [[steel-bolt-group-analysis-methods]] — full instantaneous-centre
  in-plane/out-of-plane bolt-group design method, prying action, worked
  examples (ASI Handbook 1 Ch 3.9–3.14).
- [[steel-connection-classification-and-design-philosophy]] — background
  on why AS 4100 leaves connection design models to the designer.
- [[asi-design-capacity-tables-vol1-open-sections]] — Table T9.1 bolting
  category cross-check and pre-computed bolt design capacity tables.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Cl 9.2–9.3
  (pp. 117–123).
- `raw/1-steelwork/ASI - Handbook 1 - Background and Theory - Design of
  Structural Steel Connections.pdf`, Ch 3.5–3.7 (pp. 15–25) — tear-out
  mechanics, lap-splice `k_r` rationale, design capacity reference tables.
  Figures 4, 5, 6, 7 and Tables 9, 10 reproduced in
  `wiki/0-standards/assets/`.
