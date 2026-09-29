---
title: Bolt group analysis methods — instantaneous centre (in-plane), out-of-plane, prying action
category: 1-steelwork
tags: [bolts, bolt-group, instantaneous-centre, in-plane, out-of-plane, prying-action, t-stub, ASI-handbook-1]
standards: [AS 4100:2020 Cl 9.4]
status: draft
reviewed: 2026-09-13
---

# Bolt group analysis methods

> Scope: ASI Design Guide "Handbook 1 — Background and Theory: Design of
> Structural Steel Connections" (T.J. Hogan, first edition 2007) Ch 3.9–3.14
> — the full linear-elastic instantaneous-centre method for a bolt group
> loaded in-plane (AS 4100 Cl 9.4.1), the plastic-distribution method for a
> bolt group loaded out-of-plane (Cl 9.4.2), prying action in a bolted
> T-stub/flange connection, and three fully worked design examples. This is
> the derivation and design-aid material behind the brief clause summary on
> [[steel-bolt-design]] (Cl 9.3 "Assessment of a bolt group").

## Summary

`[practice]` AS 4100 Cl 9.4.1 fixes the *assumptions* for an in-plane-loaded
bolt group (rigid plates, instantaneous centre of rotation, bolt force
proportional to and normal to its radius from that centre) but leaves the
actual solution method to the designer. This handbook adopts the **linear
(elastic) method**, which gives a closed-form solution
(`V*_res = sqrt[(V_bv*/n_b + M_bm* x_max/I_bp)² + (V_bh*/n_b + M_bm* y_max/I_bp)²]`,
Eqn 3.9.13) and is traditionally used because it is amenable to hand
calculation and conservative relative to test results; the plastic and
force/displacement alternatives need iterative/computer solution and are
not developed further here.

`[practice]` For a bolt group loaded **out-of-plane** (Cl 9.4.2), this
handbook uses a plastic bolt-force distribution: neutral axis at the bolt
group centroid, bolts above in tension only, `N*_tm = M*/(n_t y_m)`
(Eqn 3.12.1).

`[practice]` **Prying action** — additional bolt tension from flexure of
the connected plate acting as a T-stub flange against a rigid support — is
either allowed for by a flat percentage increase (0–10% thick plate, 20–40%
thin plate) or calculated from T-stub flange equilibrium
(`N*_tf = N*_t[0.5 + (a'_f/a'_e)(αδ)/(2(1+αδ))]`, Eqn 3.13.8).

## Detail

### In-plane loading — instantaneous centre method (Ch 3.9)

`[code]` AS 4100 Cl 9.4.1 assumptions: (a) connection plates rigid, rotating
about an instantaneous centre; (b) pure couple → centre at bolt-group
centroid; centroidal shear only → centre at infinity, shear uniform across
the group; other cases → superpose the two, or use a recognised method;
(c) each bolt's design shear acts at right angles to, and proportional to,
its radius from the instantaneous centre.

![[asi-h1-fig-8-bolt-group-in-plane-moment.png]]
*Figure 8 — bolt group subject to an in-plane moment only: instantaneous
centre = bolt-group centroid (ASI Handbook 1, 2007).*

`[derived]` For the pure-couple case (Figure 8), equilibrium requires
`ΣV*_n(x_n/r_n) = 0`, `ΣV*_n(y_n/r_n) = 0`, `ΣV*_n r_n = M*_bm`
(Eqns 3.9.1–3.9.3, `r_n` = radius of bolt `n` from the centroid).

![[asi-h1-fig-10-bolt-group-general-load-set.png]]
*Figure 10 — bolt group subject to a general load set: vertical shear
`V*_bv`, horizontal shear `V*_bh`, and `V*_bv` acting at eccentricity `e`
from the centroid, generating an in-plane moment (ASI Handbook 1, 2007).*

`[practice]` Solving the linear-method equation `V*_n = (r_n/r_max)V*_mb`
(Eqn 3.9.9 — bolt force proportional to radius) together with the
equilibrium equations gives the extreme-bolt design shear:

`V*_mb = M*_bm r_max / I_bp` (Eqn 3.9.10)

where `I_bp = Σr_n² = Σ(x_n² + y_n²)` is the **polar moment of area of the
bolt group** (an analogy to the polar second moment of area, not a true
elastic property). Resolved into components (Figure 12) and superposed with
the centroidal shear terms (principle of superposition, Cl 9.4.1(b)):

`V*_mh = M*_bm y_max / I_bp`, `V*_mv = M*_bm x_max / I_bp` (Eqns 3.9.11–3.9.12)

`V*_res = sqrt{[V*_bv/n_b + M*_bm x_max/I_bp]² + [V*_bh/n_b + M*_bm y_max/I_bp]²}` (Eqn 3.9.13)

— checked against `φV_f` (single-bolt shear capacity, [[steel-bolt-design]]
Cl 9.2.2.1) with the bolt-group `φ = 0.80`.

![[asi-h1-fig-12-horizontal-vertical-bolt-forces.png]]
*Figure 12 — resolving the extreme-bolt force `V*_mb` into horizontal/
vertical components (a), and vectorially combining with the centroidal
shear components (b) (ASI Handbook 1, 2007).*

`[derived]` Eqn 3.9.13 is the single general-purpose formula for any
in-plane bolt-group problem — it collapses to uniform shear when
`M*_bm = 0`, and to the pure-couple case when `V*_bv = V*_bh = 0`.

#### Closed-form design aids — single and double bolt columns (Tables 16–20)

`[practice]` For the common case `V*_bh = 0`, `M*_bm = V*_bv e` (an
eccentric vertical shear — most simple connections), Eqn 3.9.13 reduces to
`V*_bv ≤ Z_b(φV_f)` (Eqn 3.9.15/3.9.18), where `Z_b` is a closed-form
function of the eccentricity `e`, pitch `s_p` and bolt count/geometry only
— pre-tabulated for rapid design (Table 17 for a single column, Table 19
for a double column, both at `s_p = 70 mm` in the source).

![[asi-h1-fig-13-single-bolt-column.png]]
*Figure 13 — single bolt column loaded in-plane: `n_b = n_p` bolts,
`Z_b = n_p / sqrt{1 + [6e/(s_p(n_p+1))]²}` (Eqn 3.9.16) (ASI Handbook 1,
2007).*

![[asi-h1-fig-15-double-bolt-column.png]]
*Figure 15 — double bolt column loaded in-plane: `n_b = 2n_p` bolts,
gauge `s_g`, `Z_b = 2n_p / sqrt{[1+Z_1]² + [Z_1/s_pg]²}` (Eqn 3.9.19),
a more elaborate closed form accounting for both pitch and gauge
(ASI Handbook 1, 2007).*

`[practice]` The same closed-form approach gives **end-plate tear-out/
bearing** design aids (`Z_e`, `Z_ev`, `Z_eh` — Figures 14 and 16): the
resultant force at the extreme bolt is checked against ply bearing
(`φV_bf = φ3.2 d_f t_p f_up`) and against vertical/horizontal tear-out
(`φV_ev/φV_eh = φ a_ev/a_eh t_p f_up`) using the same `e`, `s_p`, `s_g`
geometry — see [[steel-bolt-design]] for the underlying tear-out mechanics
(Figures 4–6).

![[asi-h1-fig-14-single-bolt-column-tearout.png]]
*Figure 14 — single bolt column: extreme-bolt forces and edge distances
for end-plate tear-out or bearing failure (ASI Handbook 1, 2007).*

`[derived]` These `Z_b`/`Z_e` tables (Tables 17–20 in the source) are a
1980s–2000s hand-calculation design aid; a spreadsheet or connection-design
software applying Eqn 3.9.13/3.9.14/3.9.17 directly supersedes them for
routine use, but the closed forms remain useful for spot-checking software
output or for a quick manual bound.

### Worked example 1 — bolts in a lap splice connection (Ch 3.10)

`[derived]` A 180×20 mm Grade 250 plate spliced by two 10 mm cover plates
and 8 M20/8.8/S bolts each side (Figure 17) is checked to transmit the
plate's full design tension capacity (`φN_t = 810 kN`, AS 4100 Cl 7.2). With
`L_j = 70 mm` (`k_r = 1.0`), bolt shear (two shear planes, one through
threads/one through shank) governs at `4 × 218 kN = 872 kN > 810 kN` —
satisfactory. Ply bearing/tear-out on both the spliced plate and the thinner
splice plates is checked separately and does not control.

![[asi-h1-fig-17-bolted-plate-splice-example.png]]
*Figure 17 — bolted plate splice, worked example 1 geometry (ASI Handbook 1,
2007).*

### Worked example 2 — bolt group loaded in-plane (Ch 3.11)

`[derived]` An 8-M20/8.8/S bolt group (2 columns × 4 rows, Figure 18)
connects a channel bracket to a column flange, with a vertical load `V*`
applied 500 mm from the bolt group. Both the first-principles approach
(Eqns 3.9.10–3.9.13) and the closed-form Table 18/`Z_b` approach are carried
through side by side and reconciled to the same answer:
`V*_res = 0.932V* ≤ φV_f`, giving a governing capacity `V* ≤ 99.4 kN`
(bolt shear governs; end-plate tear-out in the 8 mm channel web does not).

![[asi-h1-fig-18-bolt-group-in-plane-example.png]]
*Figure 18 — bolt group loaded in-plane, worked example 2 geometry
(ASI Handbook 1, 2007).*

`[derived]` This example is a direct, numeric illustration of how
[[steel-bolt-design]]'s brief Cl 9.3.1 clause summary and the full Eqn
3.9.13 above translate into a hand calculation — useful as a template for
checking a bracket/bolt-group connection by hand or auditing software
output.

### Out-of-plane loading (Ch 3.12)

`[code]` AS 4100 Cl 9.4.2 refers a bolt group loaded out-of-plane back to
the general Cl 9.1.3 design-model requirements (equilibrium, deformation
capacity, element capacity, stability — see
[[steel-connection-classification-and-design-philosophy]]); it does not
mandate a specific distribution.

`[practice]` This handbook's method (after Ref. 9, "Case II" — neutral axis
at centre of gravity): (1) neutral axis at the bolt-group centroid;
(2) bolts above the neutral axis are all in tension; bolts below are
notionally in "compression" (usually not critical, Eqn 3.12.5); (3) a
**plastic** (uniform) distribution of tension is assumed among the bolts
above the axis, unlike the **linear** distribution used for in-plane shear.

![[asi-h1-fig-19-bolt-group-out-of-plane-actions.png]]
*Figure 19 — bolt group loaded out-of-plane: design moment `M*` normal to
the mating surface produces uniform tension `N*_tm` in the bolts above the
centroidal neutral axis, lever arm `y_m` (ASI Handbook 1, 2007).*

`[practice]` `N*_tm = M*/(n_t y_m)` (Eqn 3.12.1, `n_t` = number of bolts
above the neutral axis). For a double bolt column (`n_p` rows per column):
`n_p` odd → `n_t = n_p − 1`, `y_m = (n_p+1)s_p/2` (Eqn 3.12.2); `n_p` even →
`n_t = n_p`, `y_m = n_p s_p/2` (Eqn 3.12.3). Combined with any coincident
vertical shear `V*_v = V*/n_b` and horizontal tension `N*_t/n_b`, the
tension-side bolts satisfy the Cl 9.2.2.3 interaction
(`[V*_v/φV_f]² + [(N*_tn+N*_tm)/φN_tf]² ≤ 1.0`, Eqn 3.12.4); compression-side
bolts satisfy the same form without `N*_tm` (Eqn 3.12.5, rarely critical).

`[derived]` Prying action may increase the tension-side bolt force above
`N*_tm` — see below; Section 3.12 explicitly defers this to Section 3.13.

### Prying action (Ch 3.13)

`[practice]` A bolt group loaded out-of-plane or in direct tension through a
flexible connected plate develops **prying**: as the plate flexes, its tip
bears against the support and generates a reaction (the prying force
`N*_q`) that *adds to* the applied load in the bolt. The mechanism is
classically visualised via a T-stub flange bolted to a rigid support.

![[asi-h1-fig-21-prying-mechanism-t-stub.png]]
*Figure 21 — prying mechanism in a T-stub connection: applied force,
prying forces at the flange tips, and the resulting bolt force
(ASI Handbook 1, 2007).*

`[derived]` Measured prying levels vary 0–40% of the applied load depending
on test setup; a **stiff** ("thick") flange bends in single curvature with
little separation at the bolt line and develops little prying (bolt force
≈ half the applied load, plus small increase); a **flexible** ("thin")
flange bends further, separates at the bolt line, and develops
significant additional prying force that only grows until bolt failure.
Where more than one line of bolts sits either side of the load point, the
outer line is largely ineffective unless the plate is thick or stiffened
— not further developed in this Guide.

`[practice]` **Simple allowance**: increase the calculated bolt tension by
0–10% for a thick plate to a rigid support, or 20–40% for a thin plate.

`[practice]` **Analytical method** (after Ref. 10, also used in AISC and
Thornton's approach, Ref. 12) — T-stub geometry (Figure 24: `a_e` bolt-line
to web face, `a_f` bolt-line to flange tip, `t_f` flange thickness):

![[asi-h1-fig-24-t-stub-critical-dimensions.png]]
*Figure 24 — T-stub critical dimensions `a_e`, `a_f`, `t_f` and design
actions `N*_t` (a) undeformed, (b) with prying force `N*_q` and bolt
tension `N*_tf` shown (ASI Handbook 1, 2007).*

Force and moment equilibrium of half the T-stub (Figure 25) give:

`N*_t + 2N*_q = 2N*_tf` (Eqn 3.13.1) and `M*_1 + M*_2 = 0.5 N*_t a_f`
(Eqn 3.13.2)

![[asi-h1-fig-25-t-stub-parameters.png]]
*Figure 25 — T-stub free bodies used to derive the prying equilibrium
equations: bending moment diagram (left), bolt-line free body (right)
(ASI Handbook 1, 2007).*

`[derived]` With `δ` = (net section area at the bolt line)/(gross section
area at the web face) and `α = M*_2/M*_1` (the designer's choice of how
moment is shared between the flange-tip and web-face sections), solving
gives `M*_1(1+αδ) = 0.5 N*_t a_f` (Eqn 3.13.4), and hence the total bolt
tension including prying:

`N*_tf = N*_t[0.5 + a'_f/a'_e · αδ/(2(1+αδ))]` (Eqn 3.13.8),
`M*_1 = N*_t a'_f / [2(1+αδ)]` (Eqn 3.13.9)

using modified dimensions `a'_e = a_e + 0.5d_h`, `a'_f = a_f − 0.5d_h`
(`d_h` = bolt hole diameter) that better fit observed flange-flexure
behaviour.

`[practice]` Three design choices for `α` (per Thornton, Ref. 12):
- **Option 1 (`α = 0`)**: single-curvature bending, **zero prying**
  (`N*_tf = 0.5N*_t`), but requires a **thicker** flange satisfying
  `M*_1 = 0.5N*_t a'_f ≤ φM_s`.
- **Option 2 (`α = 1`)**: double-curvature bending; Eqns 3.13.8/3.13.9
  apply directly, both `M*_1 ≤ φM_s` and `N*_tf ≤ φN_tf` must be satisfied.
- **Option 3 (any `α`)**: a family of solutions trading flange thickness
  against bolt tension — thicker flange/less prying vs thinner flange/more
  prying.

`[derived]` This is a genuine design trade-off, not a fixed rule: a thinner,
cheaper flange plate shifts load onto the bolts (which must then be checked
for the higher `N*_tf`), while a thicker flange keeps bolt tension near
`0.5N*_t` but costs more material and requires `M_s` (connection-component
bending capacity, [[steel-connection-component-capacity]]) to be checked
against the higher `M*_1`.

### Worked example 3 — bolt group loaded out-of-plane, with prying (Ch 3.14)

`[derived]` An 8-M20/8.8/S bolt bracket connection (2 columns × 4 rows,
25 mm end plate, Figure 26) resists `R* = 250 kN` at 250 mm eccentricity
from the plate face (`M* = 62 500 kNmm`).

![[asi-h1-fig-26-bolt-group-out-of-plane-example.png]]
*Figure 26 — bolt group loaded out-of-plane, worked example 3 geometry
(ASI Handbook 1, 2007).*

Design actions: `V*_v = 31.3 kN`/bolt, `N*_tf = M*/(n_t y_m) = 111.6 kN`/bolt
(no prying). **Option 1** (`α = 0`, no prying): the Cl 9.2.2.3 interaction
is satisfied (0.53 < 1.0), but checking the 25 mm plate as a T-stub
(treating the top two bolts as a T-stub flange, Figure 27) against
`φM_s = 2460 kNmm` fails against the no-prying demand `M*_1 = 4352 kNmm` —
**the 25 mm plate is too thin for zero prying to be valid**. **Option 2**
(`α = 1`): recalculating with prying gives `N*_tf = 146 kN` (31% prying),
interaction = 0.86 < 1.0 (satisfactory), and `M*_1 = 2580 kNmm ≈ φM_s =
2460 kNmm` (satisfactory, "just"). **Conclusion**: the 25 mm plate is
adequate *only* if 31% prying is accounted for; a 36 mm plate would be
needed to eliminate prying entirely (`φM_s = 5130 kNmm > 4352 kNmm`).

`[derived]` This example is the clearest illustration in the handbook of
why prying **cannot** be ignored by default — a plate that looks adequate
under a naive "half the tension, no prying" check can fail the flange
bending check, and the corrected (`α=1`) bolt tension is 31% higher than
the naive value.

## Worked reference

See the three worked examples above (Ch 3.10, 3.11, 3.14) — fully
transcribed with source figures.

## Contradictions

None recorded.

## Related

- [[steel-bolt-design]] — AS 4100 Cl 9.2–9.3 code clauses this page's
  methods implement; tear-out mechanics (Figures 4–6).
- [[steel-connection-classification-and-design-philosophy]] — Cl 9.1.3
  design-model requirements referenced by Cl 9.4.2.
- [[steel-connection-component-capacity]] — `φM_s` connection-component
  (T-stub flange, end plate) bending capacity used in the prying check.
- [[steel-weld-group-analysis-methods]] — the analogous in-plane/
  out-of-plane elastic method for weld groups.

## Sources

- `raw/1-steelwork/ASI - Handbook 1 - Background and Theory - Design of
  Structural Steel Connections.pdf`, Ch 3.9–3.14 (pp. 28–51). Figures 8,
  10, 12, 13, 14, 15, 17, 18, 19, 21, 24, 25, 26 reproduced in
  `wiki/1-steelwork/assets/`; Figures 9, 11, 16, 20, 22, 23, 27 and Tables
  16–20 (dense numeric `Z_b`/`Z_e` design-aid tables) described in text but
  not reproduced — see the source PDF for the full tables.
