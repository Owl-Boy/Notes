---
tags:
  - Note
---
202510110010

Tags : [[Parameterized Algorithms]]
# 3k Vertex Cover Kernelization Algorithm
---
Consider a Vertex Cover instance $(G,k)$, assume that it has no isolated vertices, otherwise just remove them. We apply the Crown lemma to get a matching of size at least $k+1$ or get a crown decomposition.

In the first case, the algorithm concludes that there is no vertex cover of size at least $k$. Otherwise we get a crown decomposition $(C,H,R)$. For the reduced version we take the graph induced on $R$, with parameter $(G, k-|H|)$.

We keep reducing the graph until we have a vertex cover of we have the graph of size at most $3k$.


---
# References
- [[Kernelization Algorithm for Vertex Cover]]
- [[Crown Decomposition]]