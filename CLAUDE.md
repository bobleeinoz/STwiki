# CLAUDE.md — LLM Wiki Schema

Based on 
Operating contract for this wiki. Read this file in full before any ingest, query,
or maintenance action. If an instruction here conflicts with a request, raise the
conflict rather than silently deviating.

Domain: structural engineering — mining, material handling
Region: Australia. Primary code family: AS / AS-NZS.

---

## 1. Layers

| Layer | Path | Owner | Rule |
|---|---|---|---|
| Raw sources | `raw/` | Human | **Immutable.** Read, cite, never edit, never delete. |
| Wiki | `wiki/` | Claude | Compiled knowledge pages. Claude owns and maintains these. |
| Schema | `CLAUDE.md` | Human | This file. Claude proposes changes, human approves. |
| Log | `log.md` | Claude | Append-only record of every ingest and structural edit. |

`raw/` mirrors the `wiki/` folder numbering so a source and its compiled pages
sit under the same category.

---

## 2. Folder map

| Folder                    | Scope                                                                                                                                                                                             |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `0-standards`             | Standard register and clause maps. Which standard governs what, current edition, amendment status. **No verbatim standard text.**                                                                 |
| `1-steelwork`             | Steel members, connections, sections, fabrication, corrosion protection, erection.                                                                                                                |
| `2-concrete`              | Reinforced and prestressed concrete, reinforcement detailing, durability, crack control.                                                                                                          |
| `3-foundation-geotech`    | Footings, piles, retaining structures, soil parameters, bearing and settlement.                                                                                                                   |
| `4-loads-mechanics-maths` | Load cases and combinations, wind, seismic, thermal, dynamics, statics, section properties, numerical methods.                                                                                    |
| `5-software-fea`          | Tool-specific method pages: STAAD, SAP2000, RAM, ANSYS, AutoCAD, Revit, Civil 3D. Modelling patterns, conventions, known traps.                                                                   |
| `6-mining-structures`     | Material handling, mining and oil-and-gas structures: conveyor gantries, transfer towers, chutes, bins and silos, stackers and reclaimers, crushers, pipe racks, vessel supports, blast and fire. |
| `7-practice`              | Repeatable procedures: model QA checklists, calculation sheet layouts, review workflows, deliverable conventions.                                                                                 |
| `8-projects`              | Project-specific context. One folder or page per job. Archive on close; never let project facts leak into general pages.                                                                          |

Maximum nesting inside a category is one level. If a category needs a third
level, it should be split or the pages merged.

---

## 3. Page rules

- One page = one concept, member type, procedure or tool behaviour.
- Filename: kebab-case, descriptive, no dates. `conveyor-gantry-truss-layout.md`
- Cross-reference with `[[wiki-links]]`. Every new page must be linked from at
  least one existing page and from `wiki/index.md`.
- Never create a second page for a concept that already has one. Extend the
  existing page.

### Source summary pages — mandatory, one per ingested source

Every raw source gets exactly one summary/register page, filed in the folder
matching the source's primary category (standards go in `0-standards`; a
manufacturer catalogue, textbook or other non-standard source goes in the
category folder its content belongs to). Model it on
`wiki/0-standards/as-3600-2018-concrete-structures.md`. Required sections:

- **Front-matter** as per section above, `standards:` populated where the
  source is a standard.
- **Summary** — `[code]`/`[practice]`/`[derived]`-tagged overview: what the
  source is, edition/version, what it supersedes or relates to, key scope and
  applicability limits.
- **Detail** — section/chapter-level map of the source in own words (no
  verbatim reproduction), major changes from a prior edition if applicable,
  and cross-references to other standards/sources it invokes.
- **Worked reference** — pointer to any concept page that exercises the
  source with a numeric worked example, once one exists.
- **Contradictions** — per section 4 workflow, or "None recorded."
- **Related** — the running list of concept pages ingested from this source
  so far, grouped by section/chapter, kept current on every ingest pass.
  Note any sections/chapters not yet ingested.
- **Sources** — the exact `raw/` path(s) and edition/amendment status.

One summary page per source; extend it on later ingest passes over the same
source rather than creating a second one.

### Front-matter (required on every wiki page)

```yaml
---
title:
category:          # folder name
tags: []
standards: []      # e.g. [AS 4100:2020 Cl 5.6, AS/NZS 1170.2:2021]
status:            # draft | verified
reviewed:          # YYYY-MM-DD
---
```

`status: verified` may only be set by the human, never by Claude.

---

## 4. Provenance tagging — mandatory

Every substantive statement carries one tag. This is the single most important
rule in this wiki. Engineering content that mixes these three is unusable.

| Tag          | Meaning                                                       | Use in a calculation |
| ------------ | ------------------------------------------------------------- | -------------------- |
| `[code]`     | Clause-backed. Must cite standard, edition and clause number. | Yes                  |
| `[practice]` | Personal or company convention. No code basis.                | Yes, with judgement  |
| `[derived]`  | Claude's synthesis, inference or interpolation. Unverified.   | **No**               |

Rules:
- Never promote `[derived]` to `[code]` or `[practice]`. Only the human does that.
- If a clause number cannot be cited, the statement is not `[code]`.
- If uncertain between `[practice]` and `[derived]`, use `[derived]`.
- Never present a `[derived]` statement as a design requirement.

---

## 5. Workflows


### Ingest

1. Human places a source in the matching `raw/<category>/` folder.
2. Read it. Do not modify it.
3. Identify which existing wiki pages the source touches. Update them first.
4. Create new pages only for concepts with no existing home.
5. Create the source's summary page (section 3, "Source summary pages") if it
   doesn't exist yet; otherwise update its `## Related` list and `## Detail`
   with what this ingest pass covered.
6. Tag every added statement per section 4.
7. Update `[[wiki-links]]` in both directions and update `wiki/index.md`,
   including a link to the source summary page.
8. Where the source contradicts an existing page, record both positions on the
   page under a `## Contradictions` heading with sources. Do not silently
   overwrite. Flag it to the human.
9. Append an entry to `log.md`.

### Query

1. Answer from `wiki/` first. Read `wiki/index.md` to route.
2. Cite the wiki pages used. If a statement is `[derived]`, say so in the answer.
3. If the wiki cannot answer, say so plainly rather than improvising. Then either
   answer from general knowledge — labelled as outside the wiki — or propose a
   source to ingest.
4. Never fabricate a clause number. An uncited clause reference is a defect.

### Maintenance 

1. Contradiction sweep across all pages.
2. Amendment check on `0-standards`; flag pages whose cited edition is superseded.
3. Terminology normalisation.
4. List `[derived]` statements older than 90 days for human verification or removal.
5. List orphan pages (no inbound links) and stale pages (`reviewed` > 12 months).
6. Report findings; do not delete pages without approval.

---

## 6. Claude's standing constraints

- Do not edit anything in `raw/`.
- Do not set `status: verified`.
- Do not delete a wiki page without explicit approval.
- Do not state a design requirement without a clause citation or a `[practice]`
  or `[derived]` tag.
- Prefer flagging uncertainty over producing a confident, unsourced answer.
