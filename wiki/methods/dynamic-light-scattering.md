---
title: Dynamic Light Scattering
type: method
tags: [dls, scattering, brownian-motion]
lectures: [L06]
updated: 2026-10-19
status: draft
---

# Dynamic Light Scattering

Dynamic light scattering (DLS) determines size distributions of particles or polymers in solution by measuring time-dependent scattered-light fluctuations from [[brownian-motion]] [L6, pp.18–20].

$$g^{(2)}(\tau)=\frac{\langle I_{det}(t)I_{det}(t+\tau)\rangle}{\langle I_{det}(t)\rangle^2}$$

| Symbol | Meaning | Units / notes |
|---|---|---|
| $g^{(2)}(\tau)$ | intensity autocorrelation | dimensionless |
| $I_{det}$ | detector intensity | counts s$^{-1}$ |
| $\tau$ | delay time | s or µs |

```mermaid
xychart-beta
  title "DLS autocorrelation decay (schematic)"
  x-axis "delay time τ / µs" ["0", "10", "100", "1000"]
  y-axis "g2(τ)-1" 0 --> 1
  line "small fast particles" [1, 0.45, 0.08, 0]
  line "large slow particles" [1, 0.8, 0.35, 0.04]
```
*Takeaway: faster decay means faster diffusion and smaller hydrodynamic size.*

