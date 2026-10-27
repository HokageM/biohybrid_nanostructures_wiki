---
title: Isoelectric Point
type: concept
tags: [proteins, charge, colloids]
lectures: [L03, L06]
updated: 2026-10-19
status: draft
---

# Isoelectric Point

## In one paragraph
The isoelectric point (pI) is the pH where a protein or particle has approximately zero net charge. Lecture 3 lists pI as a variable in protein solubility and crystallisation, while lecture 6 notes that $\zeta\approx0$ mV near the isoelectric point reduces colloidal stability [L3, pp.23–24; L6, p.21].

## The chemistry
For one acidic/basic pair, a schematic net-charge expression is:

$$Z(pH)=\frac{+1}{1+10^{pH-pK_a^{\mathrm{base}}}}-\frac{1}{1+10^{pK_a^{\mathrm{acid}}-pH}}$$

| Symbol | Meaning | Units / notes |
|---|---|---|
| $Z(pH)$ | net charge number | dimensionless |
| $pH$ | acidity of solution | dimensionless |
| $pK_a^{\mathrm{base}}$ | conjugate-acid $pK_a$ of a basic group | dimensionless |
| $pK_a^{\mathrm{acid}}$ | acid-group $pK_a$ | dimensionless |

Assumptions and validity limits: this equation is outside the lecture material and only illustrates why charge changes with pH; real proteins contain many ionisable groups with shifted p$K_a$ values. At pI, reduced electrostatic repulsion favours aggregation or crystallisation [L3, pp.23–24; L6, p.21].

```mermaid
xychart-beta
  title "Net charge vs pH (schematic)"
  x-axis "pH" ["acidic", "pI", "basic"]
  y-axis "net charge" -5 --> 5
  line "protein" [4, 0, -4]
```
*Takeaway: crossing the pI flips net charge and can minimise colloidal repulsion [L6, p.21].*

## Typical orders of magnitude
- pH and pI are dimensionless; zeta potential near pI is close to 0 mV [L6, p.21].
- Stable colloids are associated with $\zeta<-30$ mV or $\zeta>+30$ mV [L6, p.21].
- Crystallisation screens vary pH, salt concentration and precipitants [L3, pp.23–24].

## Connections
Related to [[surface-charge]], [[zeta-potential]], [[salting-in-salting-out]], [[protein-crystallization-phase-diagram]], [[chaotropic-kosmotropic-ions]] and [[debye-length-slipping-plane]].
