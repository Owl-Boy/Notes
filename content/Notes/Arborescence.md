---
tags:
  - Note
---
202501291701

Tags : [[Topics in Algorithms]]
# Arborescence
---
Given a directed graph $G=(V, E)$ and distinguished node $r \in V$ called the root, we define an *Arborescence* as follows:

>[!definition]
> An *Arborescence* $T$ is a sub-graph of $G$ such that each vertex $v\in V \setminus \{ r \}$ has exactly $1$ path to $r$ and has minimum weight among all graphs that satisfy the above property.

An Arborescence is a directed version of a spanning tree. It can also be defined as a spanning tree where all edges are directed towards the root.

The existence of such a tree is easy to show, one can just reverse all the edges and start a *BFS* from $r$, if it covers all the edges then it creates an *Arborescence*, hence, one with a minimal weight must exist.

Most of the algorithms for the undirected variants of this problem are not applicable here as most of them are greedy and rely on some [[Properties of Minimum Spanning Trees]] that are not applicable in this scenario. 

An [[Algorithm for Arborescence|algorithm for finding an Arborescence]] is discussed here.

---
# References
 