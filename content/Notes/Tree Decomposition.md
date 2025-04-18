---
tags:
  - Note
---
202503311203

Tags : [[Finite Model Theory]]
# Tree Decomposition
---
Intuitively, a tree decomposition represents a vertex of a graph $G$, as a sub-tree of some tree, in a way that vertices in $G$ are adjacent only if the corresponding sub-trees intersect, thus $G$ is the *intersection graph* of the tree.

>[!definition]
>Given a graph $G=(V, E)$, a tree decomposition of $G$ is a pair $(X, T)$, where $X = \{ X_{1} \dots X_{n} \}$ is a family of subsets of $V$ and $T$ is a node whose vertices are the subsets $X_{i}$ satisfying the following properties:
>- The union of all sets $X_{i}$ is $V$.
>- For every edge $(u, v)$ in the graph, there is a subset $X_{i}$ which contains both $u$ and $v$ which is in the tree.
>- If $X_{i}$ and $X_{j}$ both contain a vertex $v$, then there is a path between $X_{i}$ and $X_{j}$ in which all vertices also contain $v$.

Bodlaender gave an algorithm for finding the tree-decomposition of a graph with bounded [[Tree Width]] in linear time, discussed [[Bodlaender's Algorithm for Finding Tree Decomposition of Small Tree Width Graphs in Linear Time|here]].

# References
