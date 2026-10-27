# Biohybrid Nanostructures — LLM Wiki Schema

This repository is an **LLM-maintained wiki** about **biohybrid nanostructures**, built from the
handwritten lecture summaries of the Biohybrid Nanostructures module at Universität Hamburg (UHH).

You (the LLM) **own and write the entire `wiki/` directory**. The human curates sources, asks
questions, and corrects you. The human does not write wiki pages.

---

## 1. Layers

| Layer | Path | Who owns it | Rules |
|---|---|---|---|
| Raw sources | `raw/` | Human | **Immutable.** Read only. Never edit, move, or rename. |
| Wiki | `wiki/` | LLM | Fully LLM-generated and maintained markdown. |
| Schema | `CLAUDE.md` | Both | Co-evolved. Update when conventions change. |

### Sources

`raw/` contains scanned **handwritten lecture summaries**, grouped by lecture number:

- `biohybrid_nanostructures_1_2_3.pdf` → lectures 1–3
- `biohybrid_nanostructures_4_5_6.pdf` → lectures 4–6
- `biohybrid_nanostructures_7_8_9_10.pdf` → lectures 7–10
- `biohybrid_nanostructures_11_12_13.pdf` → lectures 11–13

Because these are **handwritten scans**, read them page-by-page as images. Treat them as the
primary source of truth for what the module covers.

**Handwriting rules:**
- If a word, symbol, or number is illegible, write `[illegible: best-guess?]` — never invent content.
- If a hand-drawn figure, graph, or reaction scheme appears, **redraw it** as a Mermaid diagram,
  a LaTeX equation, or a markdown table. Describe the axes, labels, and the point it makes.
- Record the page range for every claim so it can be re-checked: `[L7, p.3]`.

---

## 2. Directory structure

```
raw/                      # immutable PDFs
wiki/
  index.md                # catalog of every page (content-oriented)
  log.md                  # append-only chronological record
  overview.md             # the big picture: what the module is about, how topics connect
  synthesis.md            # evolving conceptual thesis; the "so what" across lectures
  open-questions.md       # unresolved points, exam-relevant gaps, things to ask the lecturer
  glossary.md             # term → one-line definition → link to its page
  lectures/               # one page per lecture: L01.md … L13.md
  concepts/               # physical/chemical principles (e.g. dlvo-theory.md)
  materials/              # nanomaterials & biomolecules (e.g. gold-nanoparticles.md, dna-origami.md)
  methods/                # synthesis & characterisation (e.g. tem.md, spr.md)
  applications/           # drug-delivery.md, biosensing.md, …
  topics/                 # cross-cutting syntheses and comparisons you or the human generate
```

File names: lowercase `kebab-case.md`. Lecture pages: `L01.md`–`L13.md` (zero-padded).

---

## 3. Page format

Every page starts with YAML frontmatter (Dataview-compatible):

```yaml
---
title: Gold Nanoparticles
type: material          # lecture | concept | material | method | application | topic
tags: [plasmonics, colloid, au]
lectures: [L02, L05]    # which lectures touch this
updated: 2026-10-19
status: stub            # stub | draft | solid
---
```

Then the body. Use `[[wiki-links]]` (Obsidian style) for all internal references.

### Lecture page template (`wiki/lectures/L07.md`)

```markdown
# Lecture 7 — <Title>

> Source: `raw/biohybrid_nanostructures_7_8_9_10.pdf`, pp. X–Y

## In one paragraph
## Key concepts
   - bulleted, each linking to its own page
## The chemistry / physics
   - equations in LaTeX, derivations spelled out, every symbol defined
## Diagrams
   - Mermaid, redrawn from the handwritten figures
## Worked numbers / orders of magnitude
## Connections
   - builds on [[L05]]; extended in [[L09]]
## Uncertain or illegible
```

---

## 4. Visualisation — the house style

**This wiki is visual.** The human explicitly wants the chemistry and physics *drawn*, not just
described. Default to adding a diagram; only skip it if the content is genuinely non-structural.

Use **Mermaid** wherever it fits:

- `flowchart` — synthesis routes, functionalisation workflows, assembly pathways, decision logic
- `sequenceDiagram` — multi-step binding / signal-transduction / sensing events over time
- `stateDiagram-v2` — conformational states, aggregated ↔ dispersed, folded ↔ unfolded
- `classDiagram` — taxonomies (nanoparticle classes, linker chemistries, conjugation strategies)
- `graph LR` — energy-level and interaction schematics, structure hierarchies
- `xychart-beta` — plots where the *shape* matters (DLVO energy vs. distance, LSPR spectra,
  binding isotherms, size distributions). Values may be illustrative — label them `schematic`.
- `gitGraph` / `timeline` — historical development of a technique

Rules:
1. Every diagram gets a one-line caption beneath it stating the takeaway.
2. Label axes, nodes, and edges with real quantities and units.
3. Keep diagrams under ~15 nodes; split larger ones.
4. Mermaid labels containing `()`, `[]`, or `+`/`-` must be quoted: `A["Au NP (15 nm)"]`.
5. If Mermaid genuinely cannot express it (molecular structures, real spectra), use an ASCII/
   markdown table, a LaTeX diagram-in-words, or note `TODO: needs a hand-drawn figure`.

**Chemistry & physics must be explicit:**
- Write reactions as balanced equations with conditions over the arrow.
- Every formula in LaTeX (`$...$` inline, `$$...$$` block), with **every symbol defined** in a
  table right after it, including units.
- State assumptions and validity limits of each model (e.g. "DLVO assumes a continuum solvent").
- Give typical magnitudes: sizes in nm, energies in kT and kJ/mol, rates, concentrations, ζ-potentials.
- Prefer intuition first, then the math: *what does the equation physically say?*

---

## 5. Operations

### Ingest
Triggered by: "ingest lecture N" (or a page range).

1. Read the relevant PDF pages as images. Do not skim — transcribe carefully.
2. Report key takeaways to the human **before writing**, and flag illegible passages.
3. Write/update `wiki/lectures/LNN.md` using the template above.
4. Create or update every entity page the lecture touches (`concepts/`, `materials/`,
   `methods/`, `applications/`). A single lecture typically touches 8–15 pages.
5. Add backlinks both ways — a new page must be linked from at least one existing page.
6. Update `index.md`, `glossary.md`, and `overview.md`.
7. Revise `synthesis.md` if the lecture changes the big picture; add to `open-questions.md`.
8. Append to `log.md`.

Default to **one lecture at a time** with the human in the loop.

### Query
1. Read `index.md` first, then drill into the relevant pages. Grep as a fallback.
2. Answer with citations to wiki pages **and** the underlying lecture + page range.
3. If the answer is not in the wiki, say so explicitly — do not fill gaps from general knowledge
   without labelling it `(outside the lecture material)`.
4. If the answer is substantive, **file it back** as a page in `wiki/topics/`, then update
   `index.md` and `log.md`.

### Lint
Triggered by: "lint the wiki".

Check for and report (do not silently fix structural problems):
- Contradictions between pages, and between pages and the lecture scans
- Orphan pages (no inbound `[[links]]`)
- Concepts mentioned ≥2 times with no page of their own
- Pages still `status: stub`
- Equations with undefined symbols or missing units
- Pages with no diagram that clearly warrant one
- Broken `[[links]]`, stale `updated:` dates, index/filesystem drift
- Suggest the next questions worth investigating

---

## 6. index.md and log.md

`wiki/index.md` — content catalog, grouped by directory, newest-first within group:

```markdown
## Lectures
- [[L01]] — Introduction to biohybrid nanostructures — *scale, definitions, why hybrids* (L01)
## Concepts
- [[dlvo-theory]] — Balance of vdW attraction and electrostatic repulsion — *(L02, L04)*
```

`wiki/log.md` — append-only, one `##` heading per event, consistent prefix so it stays greppable:

```markdown
## [2026-10-19] ingest | Lecture 1 — Introduction
- Pages touched: lectures/L01.md, concepts/nanoscale.md, index.md
- Notes: 2 illegible passages on p.4

## [2026-10-19] query | Why do Au NPs redshift on aggregation?
- Filed as topics/lspr-aggregation-shift.md

## [2026-10-19] lint | 3 orphans, 1 contradiction (L03 vs materials/liposomes.md)
```

Never rewrite past log entries.

---

## 7. Working rules

- **Never modify `raw/`.**
- **Never invent chemistry.** Unreadable handwriting stays marked, not guessed.
- Distinguish lecture content from your own additions: label the latter
  `(outside the lecture material)`.
- Prefer updating an existing page over creating a near-duplicate.
- Keep German technical terms the lecturer used, with the English term in parentheses.
- Every edit session ends with: `index.md` current, `log.md` appended, no broken links.
- This wiki is a git repo — commit after each ingest with a message like
  `ingest: lecture 7 (nanoparticle bioconjugation)`.
