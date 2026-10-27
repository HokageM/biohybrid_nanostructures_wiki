---
title: CASP
type: method
tags: [benchmark, protein-structure, prediction]
lectures: [L02, L04]
updated: 2026-10-19
status: draft
---

# CASP

CASP is noted as a critical assessment of techniques for protein structure prediction: a tournament where methods such as Rosetta and deep learning are evaluated [L2, p.10].

```mermaid
flowchart LR
  Targets["Unknown target structures"] --> Predict["Prediction methods"]
  Predict --> Compare["Compare to experimental structures"]
  Compare --> Benchmark["Assess accuracy"]
```
*Takeaway: CASP measures whether prediction/design methods reproduce real structures.*

## Links
Connected to [[rosetta-protein-design]], [[protein-structure]] and [[protein-crystallography]].

## Lecture 4 extension — AlphaFold context
Lecture 4 returns to CASP implicitly through the protein-folding problem: [[alphafold]] is presented as a successful AI solution trained on structural and sequence data [L4, p.5]. CASP remains the benchmarking frame that links prediction methods to experimentally determined structures.

