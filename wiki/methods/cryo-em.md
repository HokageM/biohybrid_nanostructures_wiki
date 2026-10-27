---
title: Cryogenic Electron Microscopy
type: method
tags: [cryo-em, microscopy, structure]
lectures: [L03, L08]
updated: 2026-10-19
status: draft
---

# Cryogenic Electron Microscopy

Cryogenic electron microscopy is listed as frozen in water, sample-complicated, and lower-resolution than crystallography in the lecture comparison [L3, p.13].

```mermaid
flowchart LR
  Protein["Protein in vitrified water"] --> Beam["Electron beam"]
  Beam --> Images["Particle images"]
  Images --> Map["3D density map"]
```
*Takeaway: cryo-EM observes frozen hydrated proteins without crystals, but the scan emphasises sample and resolution limits.*

## Links
Contrasted with [[nmr]] and [[protein-crystallography]].

## Lecture 8 extension — single-particle pipeline
Lecture 8 expands cryo-EM into a workflow: biochemical preparation, cryogenic sample preparation, imaging/data collection, image processing, 3D reconstruction, density-map interpretation and model building [L8, p.9]. The advantage is imaging highly sensitive biological samples with low electron dose and less signal-to-noise loss than room-temperature electron microscopy; the notes also stress that cryo-EM is not diffraction-only, but reconstructs local images of many individual particles [L8, p.9].

```mermaid
flowchart LR
  Prep["Biochemical preparation"] --> Vitrify["Vitrify sample"]
  Vitrify --> LowDose["Low-dose imaging"]
  LowDose --> Pick["Particle finding"]
  Pick --> Align["Average + class + align"]
  Align --> Back["Back projection"]
  Back --> Model["Model"]
```
*Takeaway: cryo-EM uses many weak particle images to reconstruct a 3D biological structure [L8, p.9].*

### Physics
Image averaging improves signal-to-noise approximately as:

$$\mathrm{SNR}_N\approx \sqrt{N}\,\mathrm{SNR}_1$$

| Symbol | Meaning | Units / notes |
|---|---|---|
| $\mathrm{SNR}_N$ | signal-to-noise ratio after averaging $N$ images | dimensionless |
| $N$ | number of particle images | count |
| $\mathrm{SNR}_1$ | signal-to-noise ratio of one low-dose image | dimensionless |

Assumptions: independent, similarly distributed noise and correctly aligned particles; heterogeneous conformations reduce the gain.
