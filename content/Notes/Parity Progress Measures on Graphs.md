---
tags:
  - Note
---
202509180109

Tags : [[Games on Graphs]]
# Parity Progress Measures on Graphs
---
>[!definition]
>Given:
>- A graph $G=(V, E)$
>- Max priority degree $d$
>- a function $\xi:V \to \mathbb{N}^{\lceil d/2 \rceil}$
>
>We call $\xi$ a progress measure if for all  vertices $v\in V$ we have
>$$
>\xi^{[p(v)]}(v) \geq \max_{(v,w)\in E}\xi^{[p(v)]}(w)
>$$
>This inequality is strict if priority of $v$ is odd.
>
>The measure is called *small* if for every vertex $v$, in the tuple $(a_{d-1},a_{d-3}\dots a_{3},a_{1})$ which is $\xi(v)$, the entry $a_{q}$'s value is at most as much as the number of vertices with priority $q$.

Parity progress measure happen to be a good way to capture the existence of paths with max degree odd because of the following lemma: [[A graph admits a small parity progress measure iff all cycles in the graph are even]].

---
# References
- [[Progress Measures (Intuition)]]