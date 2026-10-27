---
title: ProteinMPNN
type: method
tags: [protein-design, sequence-design, ai]
lectures: [L04]
updated: 2026-10-19
status: draft
---

# ProteinMPNN

ProteinMPNN is mentioned as the inverse direction of AlphaFold: given a protein structure, predict a sequence that should realise it [L4, pp.4–5].

```mermaid
flowchart LR
  Backbone["Target backbone / structure"] --> MPNN["ProteinMPNN"]
  MPNN --> Seq["Designed sequence"]
  Seq --> Test["Expression + validation"]
```
*Takeaway: inverse design proposes sequences, but biochemical testing remains necessary.*

