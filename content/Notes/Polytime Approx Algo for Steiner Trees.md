---
tags:
  - Note
  - Incomplete
---
202501230501

Tags : [[Topics in Algorithms]]
# Polytime Approximate Algorithm for Steiner Trees
---
## Cleaning up the Graph
Given a graph $G$, one can construct a graph $G'$ such that:
- $G'$ is complete
- Any set of 3 vertices follow the triangle inequality
- For any Steiner Tree in $G'$, there is a Steiner Tree in $G$, which is atmost as heavy.

To construct such a graph, we can first deal with traingle inequality, and the triangles in the graph that already satisfy it. Consider a cycle in the graph whose edge weights are $2, 3, 8$. here the inequality is broken, so one can note that the edge with weight $8$ will never be in any tree, so we can safely discard it, similarly, given any 2 vertices that are connected with an edge such that teh lightest path is not taking the edge, we can delete the edge.

Then for each pair of vertices that do not have an edge between them, and the weight of the edge is the weight of the shortest path between the vertices, and we are done.

So we can assume that the graph satisfies all properties of $G'$.

---
## Algorithm
The Algorithm is simply finding a [[Minimum Spanning Trees]] of the sub-graph induced by $K$.

---
## Correctness.
To prove the correctness, let $T'$ be the optimal Steiner tree for $G'$. No we double all the vertices, and we get a graph where each edge has an even degree, so an Eulerian Tour exists.
- The weight of the tour is $2|T'|$
Given a Eulerian Tour, we can turn it into a Hamiltonian Cycle by Not repeating vertices and skip to the next new vertex. This gives a smaller cycle by triangle inequality.
- $H'$, such that $|H'| < 2|T|$
Now one can skip over vertices that are not in $K$, this creates a cycle that covers exactly all vertices $K$. This process also gives a smaller $H$.
- $H$, such that $|H| \leq |H'|$
Now one can drop an edge to get a tree that contains all vertices in $K$, specifically it will be heavier than the minimum spanning tree.
- $T \leq |H|$ and hence $|T| \leq 2|T'|$.

Hence, proved.

---
# References
