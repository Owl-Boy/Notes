---
tags:
  - Note
  - Incomplete
aliases:
  - Edmond's Algorithm
---
202501291801

Tags : [[Topics in Algorithms]]
# Algorithm for Arborescence
---
Edmond's Algorithm finds a minimal [[Arborescence]] in a directed edge-weighted graph. Unlike all previous algorithm, this one is not a greedy algorithm.

The key property that makes finding and proving Arborescences in a graph easier are the following:
- For each vertex $v$, let $O_{v}$ the set of out going edges and $e$ is the edge with least weight in $O_{v}$, from each edge in $O_{v}$ reduce $\text{weight}(e)$ from it. This operation preserves the ordering of the arborescences.
	- This is because each arborescence must have exactly 1 outgoing edge from each vertex (except $r$), and hence the the weight of each arborescence is reduced by exactly sum of minimum edge weights from each vertex.
- Here if we find an arborescence of weight $0$ then it has to be the minimal arborescence.

---
## The Algorithm

$\text{EDMOND}(G=\langle V, E\rangle, r:V)$:
- For each $v\in V\setminus \{ r \}$, find the weight of the smallest out going edge, say $k$ and sub-tract $k$ from weights of all outgoing edges of $v$, let that graph be $G'$
- From each vertex in $G'$ that is not $r$, pick an outgoing edge with $0$ weight (if conflict pick arbitrarily).
- If $G'$ is an arborescence, then we are done and we return $G'$, otherwise it will contain cycles.
- Contract all cycles of $G'$ to a single point, this point will not have any outgoing edge from it. We call this graph $G''$. We recursively apply the algorithm on $G''$
- An outgoing edge from the node representing the cycle in $G''$ tells us which node from the cycle to delete to replace it with in $G'$.
- Return the corresponding sub-graph of $G$.

---
## Correctness
If one finds a minimum arborescence of $G'$, that trivially gives the correct minimal arborescence for $G$, as the operation to construct $G'$ does not change the minimal arborescence.

Given a minimum arborescence for $G''$ one can find a minimal arborescence for $G'$ to show that:
- Consider a arborescence in $G''$ that can be converted to a spanning tree in $G'$ by expanding the vertices to cycles and removing the appropriate edge of the cycle.
- There will not be any better one that disagrees on the cycle because otherwise, when converting to $G''$ it would give a di-graph with weight that is greater than or equal to the weight of the minimum arborescence, hence it is not better than the one constructed in the previous example.  

>[!todo] Draw Diagrams

In each iteration, the algorithm goes over all edges, and for each recursive call, the new graph has at least 1 less vertex, hence the algorithm takes at most $O(|E| \cdot | V|)$ time.

---
# References
