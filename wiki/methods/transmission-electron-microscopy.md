---
title: Transmission Electron Microscopy
type: method
tags: [tem, electron-microscopy]
lectures: [L08]
updated: 2026-10-19
status: draft
---

# Transmission Electron Microscopy

Transmission electron microscopy (TEM) passes an electron beam through a thin sample to image internal distances, atomic/crystal structure, morphology and defects [L8, p.10]. The lecture emphasizes extremely high resolution but also vacuum, stable construction, cooling/maintenance and sample-thickness requirements [L8, p.10].

```mermaid
flowchart LR
  Source["Electron source"] --> Lenses["Electromagnetic lenses"]
  Lenses --> Sample["Thin sample"]
  Sample --> Diff["Diffraction / transmitted e-"]
  Diff --> Image["Image / SAED pattern"]
```
*Takeaway: TEM forms images from electrons transmitted through a thin specimen [L8, p.10].*

## Physics
Selected-area electron diffraction (SAED) uses reciprocal-lattice spacing:

$$R\,d=L\lambda$$

| Symbol | Meaning | Units / notes |
|---|---|---|
| $R$ | diffraction spot/ring radius on detector | m |
| $d$ | lattice spacing | m |
| $L$ | camera length | m |
| $\lambda$ | electron wavelength | m |

Assumptions: small-angle electron diffraction and calibrated camera length. The scan names SAED as a way to learn crystalline structure [L8, p.10].

## Links
Supports [[energy-dispersive-x-ray-spectroscopy]], [[electron-energy-loss-spectroscopy]] and stained/cryo workflows in [[cryo-em]].

