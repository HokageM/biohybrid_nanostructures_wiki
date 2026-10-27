---
title: Coherent X-ray Imaging
type: method
tags: [cxi, x-ray, imaging]
lectures: [L07]
updated: 2026-10-19
status: draft
---

# Coherent X-ray Imaging

Coherent X-ray imaging (CXI) records diffraction from single particles or non-crystalline samples using coherent X-rays, with the notes stating resolutions down to about 3 nm [L7, p.5]. It is proposed for detailed imaging of nanoparticles and biological samples without requiring crystals [L7, p.5].

```mermaid
flowchart LR
  Coherent["Coherent X-ray beam"] --> Particle["Single particle"]
  Particle --> Diff["Diffraction pattern"]
  Diff --> Phase["Phase retrieval"]
  Phase --> Image["Real-space density"]
```
*Takeaway: CXI reconstructs images from coherent diffraction instead of using lenses [L7, p.5].*

## Physics
The detector records intensity, not phase:

$$I(\mathbf{q})=\left|F(\mathbf{q})\right|^2$$

| Symbol | Meaning | Units / notes |
|---|---|---|
| $I(\mathbf{q})$ | diffraction intensity at scattering vector $\mathbf{q}$ | counts |
| $F(\mathbf{q})$ | complex scattering amplitude | arbitrary amplitude |
| $\mathbf{q}$ | reciprocal-space vector | m$^{-1}$ |

Assumptions: coherent illumination and sufficient oversampling are needed for phase retrieval. Radiation damage remains a challenge for biological specimens [L7, pp.4–6].

## Links
Shares the phase-retrieval issue with [[phase-problem]] and the source requirements of [[synchrotron-radiation]] / [[x-ray-free-electron-laser]].

