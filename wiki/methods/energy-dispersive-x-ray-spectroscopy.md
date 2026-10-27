---
title: Energy-Dispersive X-ray Spectroscopy
type: method
tags: [edx, electron-microscopy, elemental-analysis]
lectures: [L08]
updated: 2026-10-19
status: draft
---

# Energy-Dispersive X-ray Spectroscopy

Energy-dispersive X-ray spectroscopy (EDX) uses an electron beam to remove inner-shell electrons; relaxation emits characteristic, element-specific X-rays that are collected by a detector [L8, p.7]. The lecture describes EDX as qualitative and quantitative elemental information and useful for elemental composition in TEM/SEM [L8, p.7].

```mermaid
flowchart LR
  EBeam["High-energy e-"] --> Core["Inner core e- removed"]
  Core --> Relax["Outer e- fills hole"]
  Relax --> Xray["Characteristic X-ray"]
  Xray --> CCD["Detector / CCD"]
  CCD --> Map["Elemental map"]
```
*Takeaway: EDX maps elements by measuring X-ray energies emitted after electron-beam excitation [L8, p.7].*

## Physics
$$E_{\gamma}=E_{\mathrm{shell,outer}}-E_{\mathrm{shell,inner}}$$

| Symbol | Meaning | Units / notes |
|---|---|---|
| $E_{\gamma}$ | emitted X-ray energy | eV or keV |
| $E_{\mathrm{shell,outer}}$ | higher-shell electron energy | eV |
| $E_{\mathrm{shell,inner}}$ | lower-shell electron energy | eV |

Assumptions: emitted lines are element-specific; quantification requires standards/corrections for absorption, fluorescence yield and detector geometry.

## Links
Contrasted with [[electron-energy-loss-spectroscopy]] and related to [[x-ray-fluorescence-spectroscopy]].

