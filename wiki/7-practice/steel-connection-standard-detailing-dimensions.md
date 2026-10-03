---
title: Standard connection detailing dimensions — rationalised setbacks and gauge lines
category: 7-practice
tags: [detailing, rationalised-dimensions, gauge-lines, connections, ASI-handbook-1]
standards: []
status: draft
reviewed: 2026-09-13
---

# Standard connection detailing dimensions

> Scope: ASI Design Guide "Handbook 1 — Background and Theory: Design of
> Structural Steel Connections" (T.J. Hogan, first edition 2007) Ch 7 —
> rationalised (standardised) supporting-member setback dimensions and
> gauge lines used across the ASI Connections Series, so different
> connection design guides detail consistently against the same section
> designations. Reference/detailing data, not code-derived design theory.

## Summary

`[practice]` To keep connection detailing consistent across different
design guides and projects, the ASI Connections Series standardises two
kinds of dimension against each rolled/welded section designation:
(1) **rationalised setback dimensions** (`a`, `w`, `k`, `m`, `r` — flange/
web clearances used for connection component sizing) and (2) **gauge
lines** (`s_gf` flange, `s_gw` web — standard bolt-line spacing) by bolt
diameter (M16/M20/M24), each with a numbered **preference order** (1 =
first choice) so detailers default to a common pattern unless a specific
project constraint forces a different gauge.

## Detail

### Rationalised setback dimensions (Ch 7.1)

`[practice]` Tables 35–39 tabulate `a`, `w`, `k`, `m`, `r` (see figure
below for definitions) for every standard Australian rolled/welded section:
Table 35 (universal beams), Table 36 (universal columns), Table 37 (welded
beams), Table 38 (welded columns), Table 39 (parallel flange channels).
These feed directly into connection component sizing (e.g. angle-cleat
length, end-plate depth) so that a component detailed against the
handbook's dimensions fits the section's actual fillet/root radius and
flange geometry without a fresh measurement each time.

![[asi-h1-table-35-ub-rationalised-dimensions.png]]
*Table 35 — universal beams, rationalised dimensions for detailing:
depth `d`, flange width `b_f`/thickness `t_f`, web thickness `t_w`, and
setbacks `a` (root radius clearance), `w`, `k` (flange-to-fillet-toe), `m`
(overall minus corner allowance), `r` (root radius) (ASI Handbook 1,
2007).*

`[derived]` Tables 36–39 (universal columns, welded beams, welded columns,
parallel flange channels) follow the identical column structure — see the
source PDF pp. 110–112 for the full tables; not reproduced individually
here since the format and use are the same as Table 35.

### Gauge lines (Ch 7.2)

`[practice]` Tables 40–43 give standard bolt gauge lines (`s_gf` in the
flange, `s_gw` in the web, or `s_gw1`/`s_gw2` for a double gauge line) for
M16/M20/M24 bolts, each dimension ranked by **preference** (1 = default) so
multiple lines of bolts land on consistent, previously-tabulated centres:
Table 40 (universal beams/columns), Table 41 (welded section flanges),
Table 42 (welded section webs), Table 43 (parallel flange channels). A "b"
entry means the flange is too narrow for that bolt size; a "c" entry means
the web cannot fit two bolt lines ≥ 50 mm apart.

![[asi-h1-table-40-gauge-lines-universal-sections.png]]
*Table 40 — gauge lines for universal beams/columns: flange gauge `s_gf`
and web gauge `s_gw` (single or double line) by bolt size, with preference
ranking (ASI Handbook 1, 2007).*

![[asi-h1-table-43-gauge-lines-pfc.png]]
*Table 43 — gauge lines for parallel flange channels (ASI Handbook 1,
2007).*

`[derived]` Tables 41–42 (welded beam/column flanges and webs) follow the
same structure as Table 40 but for welded (plate) sections, which can carry
a **triple** flange gauge line (`s_gf1`, `s_gf2`) on wider flanges — see
the source PDF p. 114.

## Worked reference

None — reference tables only.

## Contradictions

None recorded.

## Related

- [[as4100-bolt-and-pin-detailing]] — AS 4100 Cl 9.5 minimum/maximum pitch
  and edge distance limits these rationalised dimensions must still satisfy.
- [[steel-connection-component-capacity]] — rectangular component sizing
  that uses these setback dimensions.
- [[steel-coped-beam-capacity]] — supported-member (Section 6) companion
  to this supporting-member (Section 7) reference material.
- [[steel-documentation-and-construction-category]] — general drawing/
  detailing documentation requirements.
- [[asi-design-capacity-tables-vol1-open-sections]] — Part 10 rationalised
  fabrication dimensions (setbacks `a`, `w`, `k`, `m`) and gauge lines per
  section type (1999 design aid, an earlier/parallel source to ASI
  Handbook 1 Ch 7 above — not cross-checked value-by-value in this ingest).

## Sources

- `raw/1-steelwork/ASI - Handbook 1 - Background and Theory - Design of
  Structural Steel Connections.pdf`, Ch 7.1–7.2 (pp. 110–115). Tables 35,
  40, 43 reproduced in `wiki/1-steelwork/assets/`; Tables 36, 37, 38, 39,
  41, 42 described in text but not individually reproduced — see the
  source PDF.
