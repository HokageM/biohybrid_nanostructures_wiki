---
title: Reciprocal Space and Fourier Transform
type: concept
tags: [reciprocal-space, fourier, electron-density]
lectures: [L03]
updated: 2026-10-19
status: draft
---

# Reciprocal Space and Fourier Transform

The notes show real-space crystal/protein features transformed into reciprocal space, where spots encode distances and periodicities; a Fourier transform relates real and reciprocal space [L3, p.21]. Reflections on the detector become structure factors, and a Fourier transform gives electron density inside the crystal [L3, p.22].

$$
\rho(\mathbf{x})=\frac{1}{V}\sum_{hkl}|F_{hkl}|\exp(i\phi_{hkl})\exp(-2\pi i\,\mathbf{h}\cdot\mathbf{x})
$$

| Symbol | Meaning | Units |
|---|---|---|
| $\rho(\mathbf{x})$ | electron density | e nm$^{-3}$ |
| $V$ | unit-cell volume | nm$^3$ |
| $F_{hkl}$ | structure-factor amplitude | complex/scaled |
| $\phi_{hkl}$ | phase | radians |
| $\mathbf{h}$ | reciprocal vector | nm$^{-1}$ |
| $\mathbf{x}$ | real-space position | nm |

```mermaid
flowchart LR
  Real["Real-space unit cell"] -- "Fourier transform" --> Recip["Reciprocal-space spots"]
  Recip -- "inverse transform + phases" --> Density["Electron density"]
  Density --> Model["Protein model"]
```
*Takeaway: crystallography infers real-space electron density from reciprocal-space diffraction.*

## Links
Connected to [[x-ray-diffraction]], [[bragg-law]] and [[protein-crystallography]].
