---
tags:
  - Note
---
202510130110

Tags : [[Parameterized Algorithms]]
# Kernelization Algorithm for d-Hitting Set
---
>[!theorem]
>*d-HITTING SET* admits a kernel with at most $d!k^d$ sets and at most $d!k^d\cdot d^2$ elements.

The idea is that if $\mathcal A$ contains a sunflower of size at least $k+1$ then the Hitting set $H$ of $\mathcal A$ must intersect with the core of the sunflower.

This we have the reduction rule: Let $(U, \mathcal A, k)$ be an instance of $d$-HITTING SET and assmue $\mathcal A$ contains a sunflower $S$ of cardinality $k+1$ with core $Y$. Then return $(U', A', k)$, where $\mathcal A'=(\mathcal A-S) + Y$.

The algorithm is as follows: If for some $d' \in \{ 1\dots d \}$, the number of sets $\mathcal A$ of size exactly $d'$ is more than $d'!k^{d'}$ then the [[Sunflower Lemma]] shows us that there exists a sunflower of size $k+1$. If we apply the procedure exhaustively, we obtain a family o size at most $d!k^d\cdot d$. If $\emptyset \in \mathcal A'$ at any point, then the algorithm concludes that there is no hitting of size at most $k$, otherwise every set contains at most $d$ elements, so the kernel is at most $d!k^d\cdot d^2$.

---
# References
- [[Sunflower Lemma]]
- [[Kernelization]]