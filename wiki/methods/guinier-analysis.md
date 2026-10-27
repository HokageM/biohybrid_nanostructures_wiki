---
title: Guinier Analysis
type: method
tags: [saxs, radius-of-gyration, model-fitting]
lectures: [L06]
updated: 2026-10-19
status: draft
---

# Guinier Analysis

Guinier analysis extracts radius of gyration from the low-$q$ region of a SAXS curve [L6, p.22].

$$I(q)\approx I(0)\exp\left(-\frac{1}{3}q^2R_g^2\right)$$

| Symbol | Meaning | Units / notes |
|---|---|---|
| $I(q)$ | scattered intensity | arbitrary units |
| $I(0)$ | zero-angle intensity | arbitrary units |
| $q$ | scattering vector | nm$^{-1}$ |
| $R_g$ | radius of gyration | nm |

```mermaid
xychart-beta
  title "Guinier region (schematic)"
  x-axis "q²" ["low", "mid", "high"]
  y-axis "ln I(q)" 0 --> 10
  line "linear Guinier fit" [9, 7, 4]
```
*Takeaway: the very-low-$q$ slope gives an overall size measure.*

