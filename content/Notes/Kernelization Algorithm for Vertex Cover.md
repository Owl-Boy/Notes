---
tags:
  - Note
---
202510041710

Tags : [[Parameterized Algorithms]]
# Kernelization Algorithm for Vertex Cover
---
For information on the problem, check [[Vertex Cover Problem]]

A Kernelization Algorithm for Vertex Cover would look like the following:
- Note that any isolated vertex can always be removed from any vertex cover, thus one possible reduction would be to remove all isolated vertices. $(|G|,k)\to (|G|-1,k)$
- Note that any vertex with degree more than $k$ must be in the vertex cover because otherwise, at least $k+1$ vertices would be required to cover the edges adjacent to that vertex. $(|G|,k)\to(|G|-1,k-1)$

An exhaustive application of these 2 rules would leave a graph where each vertex has degree at least $1$ and at most $k$. 

We also have that, since the vertex cover has size at most $k$, and each vertex has degree at most $k$, the graph can have at most $k^2+k$ vertices at at most $k^2$ edges. 

That is possible check in  $f(k)$ and also finding a vertex cover with $k^2+k$ vertices can also be done in $g(k)$, where $f$ and $g$ are computable functions. Hence the kernel can be solved in $(f+g)(k)$.


---
# References
- [[Vertex Cover Problem]]
- [[Kernelization]]