---
title: Weld design — butt welds, fillet welds, plug/slot welds, compound welds and weld groups
category: 0-standards
tags: [welds, butt-weld, fillet-weld, plug-weld, slot-weld, compound-weld, weld-group, throat-thickness, weld-metal-strength]
standards: [AS 4100:2020 Cl 9.6, AS 4100:2020 Cl 9.7, AS 4100:2020 Cl 9.8]
status: draft
reviewed: 2026-09-13
---

# Weld design

> Scope: AS 4100:2020 Cl 9.6 (weld scope/quality, complete/incomplete
> penetration butt welds, fillet welds — size, throat, effective length/
> area, spacing rules, strength, weld-metal strength Table 9.6.3.10(A),
> plug/slot welds, compound welds), Cl 9.7 (weld-group in-plane/out-of-
> plane/combined analysis), Cl 9.8 (packing). General connection provisions
> on [[as4100-connection-design-requirements]].

## Summary

`[code]` Welding to AS/NZS 1554.1, .2, .4 or .5 (Cl 9.6.1.1); weld types are
butt, fillet, slot, plug or compound (Cl 9.6.1.2); weld quality SP or GP per
AS/NZS 1554.1/1554.4, or AS/NZS 1554.5 where Cl 11.1.4 (fatigue) requires
higher quality (Cl 9.6.1.3).

`[code]` Complete penetration butt weld capacity = the weaker joined part's
nominal capacity × the butt-weld `φ` (Table 3.4): 0.90 (SP) / 0.60 (GP)
(Cl 9.6.2.7). Fillet weld: `v_w = 0.6 f_uw t_t k_r` per unit length
(Cl 9.6.3.10), `φ = 0.80` (SP) / `0.60` (GP), or `0.70` for a longitudinal
fillet weld in RHS `t < 3 mm` (Table 3.4).

## Detail

### Complete and incomplete penetration butt welds (Cl 9.6.2)

`[code]` Definitions (9.6.2.1): complete penetration — fusion throughout
the complete joint depth; incomplete penetration — fusion over less than
the complete depth; prequalified preparation — per AS/NZS 1554.1 or 1554.4.

`[code]` Size (9.6.2.2): complete-penetration butt weld (other than T- or
corner-joint) and incomplete-penetration butt weld size = minimum depth the
weld extends from its face into the joint, excluding reinforcement.
Complete-penetration T-/corner-joint size = the thickness of the part whose
end/edge butts the other part's face.

`[code]` Design throat thickness (9.6.2.3):
- Complete penetration: `t_t` = the weld size.
- Incomplete penetration, prequalified preparation: per AS/NZS 1554.1/1554.4
  (except (iii) below).
- Incomplete penetration, non-prequalified preparation: by preparation
  angle `θ` and depth `d` (single V) or `d_3`, `d_4` (double V, each side):

  | Angle | Single V | Double V |
  |---|---|---|
  | `θ ≤ 60°` | `(d − 3) mm` | `[(d_3+d_4) − 6] mm` |
  | `θ > 60°` | `d mm` | `(d_3+d_4) mm` |

- Automatic arc weld with macro-test-verified penetration: `t_t` may be
  increased up to the depth of preparation, or (if the macro test shows
  deeper penetration) up to the value in Figure 9.6.3.4 (deep-penetration
  fillet-weld formula, reused here). Only the required `t_t` need be
  specified — the fabricator determines the welding procedure.

`[code]` Effective length (9.6.2.4) = length of continuous full-size weld.
Effective area (9.6.2.5) = effective length × design throat thickness.

`[code]` Transition of thickness/width (9.6.2.6): tension butt joints
between parts of different thickness or width need a smooth transition —
chamfering the thicker part, sloping the weld surface, or both — transition
slope ≤ 1:1 (Section 11 fatigue detail categories may require a lesser
slope or curved transition).

![[as4100-fig-9.6.2.6-butt-weld-transitions.png]]
*Figure 9.6.2.6 — transitions of thickness or width for butt welds subject to tension (AS 4100:2020).*

`[code]` Strength assessment (9.6.2.7):
- **Complete penetration**: design capacity = nominal capacity of the
  **weaker joined part** × the butt-weld `φ` (Table 3.4), provided welding
  procedures are qualified to AS/NZS 1554.1/1554.4/1554.5 and the
  consumable produces butt tensile test specimens (AS 2205.2.1) with
  strength ≥ Table 2.1 for the parent material.
- **Incomplete penetration**: calculated **as a fillet weld** (Cl 9.6.3.10)
  using the Cl 9.6.2.3(b) design throat thickness.

### Fillet welds (Cl 9.6.3)

`[code]` **Size** (9.6.3.1): specified by leg lengths `t_w1`, `t_w2` of the
triangle inscribed in the weld cross-section (or a single `t_w` if equal);
with a root gap, `t_w` = inscribed-triangle leg length **less the root
gap**. Preferred sizes < 15 mm: 3, 4, 5, 6, 8, 10, 12 mm.

![[as4100-fig-9.6.3.1-fillet-weld-size.png]]
*Figure 9.6.3.1 — fillet weld size: (a) concave, (b) convex, (c) with root gap, (d)/(e) at angled connections (AS 4100:2020).*

`[code]` **Minimum size** (9.6.3.2), other than a butt-weld reinforcing
fillet, by thickness of the **thickest** part `t`:

| t (mm) | Min. t_w (mm) |
|---|---|
| ≤ 7 | 3 |
| 7 < t ≤ 10 | 4 |
| 10 < t ≤ 15 | 5 |
| > 15 | 6 |

(need not exceed the thickness of the thinner part joined.)

`[code]` **Maximum size along an edge** (9.6.3.3): material `< 6 mm` —
`t_w = t` (material thickness); material `≥ 6 mm` — `t_w ≤ t − 1 mm`,
unless built out to obtain the full design throat thickness, in which case
`t_w = t` is permitted.

`[code]` **Design throat thickness** (9.6.3.4): per Figure 9.6.3.1
(perpendicular distance, root to face, of the inscribed triangle). For an
automatic-arc deep-penetration weld with a macro-test-verified production
weld: `t_t = t_t1 + 0.85 t_t2` (Figure 9.6.3.4 — `t_t1` fusion-face throat,
`t_t2` additional penetration beyond the nominal root).

`[code]` **Effective length** (9.6.3.5) = overall length of full-size
fillet including end returns; minimum effective length = `4 t_w`, else the
design size is taken as `0.25 ×` the effective length (also applies to lap
joints). Intermittent-weld segments: effective length ≥ greater of 40 mm
and `4 t_w`.

`[code]` **Effective area** (9.6.3.6) = effective length × design throat
thickness.

`[code]` **Transverse spacing** (9.6.3.7): two parallel fillet welds
forming a built-up member in the load direction — transverse spacing
≤ `32 t_p`, except intermittent fillet welds at the ends of a **tension**
member — ≤ lesser of `16 t_p` and 200 mm (`t_p` = thinner connected
component). Fillet welds in slots/holes may be used to satisfy this.

`[code]` **Intermittent fillet welds** (9.6.3.8), except at built-up-member
ends: clear spacing between consecutive collinear segments ≤ lesser of —
(a) compression elements: `16 t_p` and 300 mm; (b) tension elements:
`24 t_p` and 300 mm.

`[code]` **Built-up members — intermittent fillet welds at ends**
(9.6.3.9): (a) at the ends of a tension/compression beam component or a
tension member, side fillets alone need a length along each joint line
≥ the connected component's width (tapered component: greater of the
widest-part width and the taper length); (b) at a compression member's cap
or base plate, welds along each joint line ≥ the member's maximum width at
the contact face; (c) where a beam connects to the face of a compression
member, the welds joining the compression member's components must extend
between the beam's top and bottom levels, plus a distance `d` (max.
cross-sectional dimension of the compression member) below the beam
(unrestrained connection) or above **and** below the beam (restrained
connection).

`[code]` **Strength limit state** (9.6.3.10): `v*_w ≤ φv_w` (vectorial sum
of design forces per unit length on the effective area), `v_w = 0.6 f_uw
t_t k_r`.

- `f_uw` = nominal tensile strength of weld metal (Table 9.6.3.10(A)).
- `k_r` = welded-lap-connection length reduction (Table 9.6.3.10(B)), else
  1.0.

`[code]` Table 9.6.3.10(A) — nominal tensile strength of weld metal `f_uw`
(selected rows; consumable classification by process — see the source for
the full electrode-classification cross-reference):

| f_uw (MPa) | Typical consumable class (MMAW) | Applies to steel type |
|---|---|---|
| 430 | E43XX / W40X | Types 1–8C (AS/NZS 1554.1/.5) and 8Q–10Q (AS/NZS 1554.4) |
| 490 | E49XX / W50X | as above |
| 550 | E55XX / W55X | as above |
| 620 | E62XX / W62X | Types 8Q–10Q only |
| 690 | E69XX / W69X | Types 8Q–10Q only |
| 760 | E76XX / W76X | Types 8Q–10Q only |
| 830 | E83XX / W83X | Types 8Q–10Q only |

`[derived]` `f_uw` must be matched (or exceed, per Cl 9.6.2.7) the parent
Table 2.1 `f_u`. For Grade 350 (`f_u = 450–450`) an E49XX/W50X consumable
(`f_uw = 490`) is the common minimum choice; for Grade 450 plate an
E55XX/W55X (`f_uw = 550`) is typically specified.

`[code]` Table 9.6.3.10(B) — welded lap connection reduction `k_r`:

| Weld length l_w (m) | k_r |
|---|---|
| ≤ 1.7 | 1.00 |
| 1.7 < l_w ≤ 8.0 | `1.10 − 0.06 l_w` |
| > 8.0 | 0.62 |

### Plug and slot welds (Cl 9.6.4)

`[code]`
- **Fillet welds around the hole/slot circumference** (9.6.4.1): treated as
  a fillet weld — effective length per Cl 9.6.3.5, capacity per Cl 9.6.3.10,
  minimum size per Cl 9.6.3.2.
- **Hole filled with weld metal** (9.6.4.2): effective shear area `A_w` =
  the hole/slot's nominal cross-sectional area in the plane of the faying
  surface; `V*_w ≤ φV_w`, `V_w = 0.60 f_uw A_w`.
- **Limitations** (9.6.4.3): only to transmit shear in lap joints, to
  prevent buckling of lapped parts, or to join built-up-member components.

### Compound weld (Cl 9.6.5)

`[code]` A fillet weld superimposed on a butt weld, per AS 1101.3
(9.6.5.1). Design throat thickness (9.6.5.2): (a) complete-penetration
component — the butt weld size without reinforcement; (b) incomplete-
penetration component — the shortest distance from the incomplete-
penetration weld's root to the fillet weld's face, via the largest inscribed
triangle in the total cross-section, capped at the thickness of the part
whose end/edge butts the other part.

![[as4100-fig-9.6.5.2-compound-weld-throat-thickness.png]]
*Figure 9.6.5.2 — design throat thicknesses of compound welds (AS 4100:2020).*

`[code]` Strength limit state (9.6.5.3): per Cl 9.6.2.7.

### Assessment of a weld group (Cl 9.7)

`[code]` **In-plane loading** (9.7.1) — same rigid-plate / instantaneous-
centre method as a bolt group (Cl 9.3.1): general method (9.7.1.1) —
connection plates rigid, rotate about an instantaneous centre; pure couple
→ centre at group centroid; centroidal shear only → centre at infinity,
`v*_w` uniform across the group; other cases → superpose or use a
recognised method; `v*_w` at any point acts at right angles to, and
proportional to, its radius from the instantaneous centre. Check Cl 9.6.3.10
at all points (constant-throat groups: only the point of maximum radius
need be checked), with the weld-group `φ` (Table 3.4). **Alternative
analysis** (9.7.1.2): treat the weld group as an extension of the connected
member and distribute `v*_w` to satisfy equilibrium with the connected
member's elements; still check Cl 9.6.3.10 with the weld-group `φ`.

`[code]` **Out-of-plane loading** (9.7.2) — general method (9.7.2.1): weld
group analysed in isolation from the connected element; `v*_w` from a
design moment varies **linearly** with distance from the relevant
centroidal axis; `v*_w` from shear or axial force is **uniform** along the
group length. Check Cl 9.6.3.10 with the weld-group `φ`. **Alternative
analysis** (9.7.2.2): as an extension of the connected member, distributed
by equilibrium; same check.

`[code]` **Combined in-plane and out-of-plane** (9.7.3): general method
(9.7.3.1) combines Cl 9.7.1.1 and 9.7.2.1; alternative (9.7.3.2) combines
Cl 9.7.1.2 and 9.7.2.2. Both checked to Cl 9.6.3.10 with the weld-group `φ`.

### Combination of weld types (Cl 9.7.4)

`[code]` Where two or more weld types are combined in one connection, the
connection's design capacity = the **sum** of each type's design capacity
per this Section.

`[derived]` This differs from the AISC/older-practice assumption (still
common outside Australia) that a fillet weld combined with a butt weld
shares load in proportion to relative stiffness — AS 4100 instead permits
simple summation of capacities, provided each weld type's own strength
requirements are independently satisfied.

### Packing in construction (Cl 9.8)

`[code]` Packing welded between two members, if `< 6 mm` thick or too thin
for adequate welds / to prevent buckling: trim flush with the loaded
element's edges and increase the edge weld size by the packing thickness.
Otherwise: extend the packing beyond the edges and weld it to the piece it
is fitted to.

## Worked reference

None yet.

## Contradictions

None recorded.

## Related

- [[as4100-connection-design-requirements]] — general connection provisions,
  minimum design actions, choice of fasteners.
- [[as4100-bolt-design]] — the analogous bolt-group instantaneous-centre
  method (Cl 9.3), combined connections (Cl 9.1.7).
- [[as4100-materials-and-design-strengths]] — Table 2.1 parent-metal
  strengths that `f_uw` must match or exceed.
- [[as4100-fatigue-design]] — Section 11 weld-quality and geometry demands
  that can exceed these baseline rules.
- [[steel-weld-group-analysis-methods]] — full instantaneous-centre
  in-plane/out-of-plane weld-group design method, properties of common
  weld-group shapes, worked examples (ASI Handbook 1 Ch 4).
- [[steel-connection-classification-and-design-philosophy]] — background
  on connection design models generally.

## Sources

- `raw/0-standards/AS_4100-2020-Reprinted-Cut.pdf`, Cl 9.6–9.8
  (pp. 125–138). Figures 9.6.2.6, 9.6.3.1, 9.6.5.2 reproduced in
  `wiki/0-standards/assets/`; Table 9.6.3.10(A) summarised (full
  electrode-classification cross-reference in the source).
- `raw/1-steelwork/ASI - Handbook 1 - Background and Theory - Design of
  Structural Steel Connections.pdf`, Ch 4.1–4.5 (pp. 52–61) — weld types/
  symbols, GP/SP category rationale, fillet weld throat thickness and
  design-capacity reference tables. Figures 28–32 and Tables 23–24
  reproduced in `wiki/0-standards/assets/`.
