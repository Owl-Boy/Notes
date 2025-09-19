---
tags:
  - Note
---
202509182209

Tags : [[Games on Graphs]]
# Least Progress Measure
---
Consider the set of progress measures that can be defined on a parity game $G$. 

A small parity progress measure is defined by a function $V\to M_{V}\cup \{ \top \}$, these functions can be ordered component-wise, this gives a partial order on the set, which will be a complete lattice, the component wise $\text{min}$ and $\text{max}$ defines the join and meet operators.

We have the following lemma
>[!lemma]
>Let $\rho_{1}$ and $\rho_{2}$ be progress measures. Then $\rho_{1} \sqsubseteq \rho_{2}\Rightarrow\text{dom}(\rho_{1}) \supseteq\text{dom}(\rho_{2})$.

Thus, there exists a least progress measure. This progress measure also happens to be efficient to compute, and the computation is discussed in [[Computing the Least Progress Measure]].

---
# References
- [[Parity Progress Measures on Games]]
- [[Progress Measures (Intuition)]]
- [[Complete Lattice]]