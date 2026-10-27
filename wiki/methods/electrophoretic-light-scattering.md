---
title: Electrophoretic Light Scattering
type: method
tags: [els, zeta-potential, electrophoresis]
lectures: [L06]
updated: 2026-10-19
status: draft
---

# Electrophoretic Light Scattering

Electrophoretic light scattering (ELS) applies an electric field and measures particle mobility through the Doppler shift of scattered light [L6, p.21].

$$\mu=\frac{\varepsilon\zeta}{\eta}$$

| Symbol | Meaning | Units / notes |
|---|---|---|
| $\mu$ | electrophoretic mobility | m$^2$ V$^{-1}$ s$^{-1}$ |
| $\varepsilon$ | permittivity | F m$^{-1}$ |
| $\zeta$ | zeta potential | V or mV |
| $\eta$ | viscosity | Pa s |

```mermaid
flowchart LR
  Field["Applied E-field"] --> Move["Particles move"]
  Move --> Doppler["Doppler shift"]
  Doppler --> Mobility["Mobility"]
  Mobility --> Zeta["ζ potential"]
```
*Takeaway: ELS turns electrophoretic motion into zeta potential [L6, p.21].*

