---
title: Protein Structure
type: concept
tags: [proteins, secondary-structure]
lectures: [L01, L02, L04]
updated: 2026-10-19
status: draft
---

# Protein Structure

The lecture hierarchy is primary structure > secondary structure > tertiary structure > quaternary structure [L1, p.2]. Primary structure is the amino-acid sequence; secondary structures include alpha helices and beta sheets stabilised by hydrogen bonds; tertiary structure is the folded 3D molecule; quaternary structure is assembly of multiple chains.

```mermaid
flowchart LR
  P1["Primary sequence"] --> P2["Secondary structure"]
  P2 --> P3["Tertiary fold"]
  P3 --> P4["Quaternary assembly"]
```
*Takeaway: protein function and design depend on the propagation of information from sequence to assembly.*

## Key chemistry / physics
- Alpha helix: N-H forms H-bonds to C=O of residues four positions earlier/later, written in the notes as $i+4 \rightarrow i$ [L1, p.2].
- Beta sheet: N-H forms H-bonds to C=O groups from the opposite strand [L1, p.2].
- [[protein-folding-thermodynamics]] controls whether the folded state is favoured in water.

## Links
Used in [[rational-protein-design]], [[rosetta-protein-design]], [[protein-cages]] and [[protein-crystallography]].

## Lecture 4 extension — prediction and validation
Lecture 4 connects protein structure to the [[protein-folding-problem]], [[alphafold]] and [[protein-mpnn]], while also emphasising that crystallographic models must be validated by allowed backbone angles in a [[ramachandran-plot]] [L4, pp.2,4–5].

