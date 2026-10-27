---
title: Apoferritin
type: material
tags: [protein-cage, nanoreactor, ferritin]
lectures: [L09]
updated: 2026-10-19
status: draft
---

# Apoferritin

Apoferritin is the iron-free ferritin protein shell used as a nanoreactor for nanoparticle synthesis [L9, p.15]. The lecture gives four motivations: it constrains nanoparticle size, works under mild conditions, leaves a defined atomic-scale shell around the inorganic product and is biocompatible enough to be functionalized with targeting ligands or water-soluble cargo [L9, p.15].

```mermaid
flowchart LR
  Apo["Apoferritin hollow shell"] --> Load["Load precursor ions"]
  Load --> React["Oxidation / reduction / precipitation"]
  React --> NP["Confined NP core"]
  NP --> Bio["Biocompatible protein shell"]
```
*Takeaway: apoferritin turns ferritin’s biological cavity into a size-limited inorganic reaction vessel [L9, p.15].*

## Chemistry / physics
The size limit is geometric:

$$d_{\mathrm{NP}}\lesssim d_{\mathrm{cavity}}$$

| Symbol | Meaning | Units / notes |
|---|---|---|
| $d_{\mathrm{NP}}$ | nanoparticle diameter | nm |
| $d_{\mathrm{cavity}}$ | internal apoferritin cavity diameter | nm |

Assumptions: the inequality captures confinement only. Actual product size also depends on pore transport, precursor concentration, nucleation number and growth kinetics [L9, p.15].

## Links
Derived from [[ferritin]] and an example of [[protein-cages]] and [[nanoparticle-synthesis-in-nanoreactors]].

