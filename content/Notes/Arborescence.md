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
> An *Arborescence* is a directed graph such that the underlying undirected graph with a distinguished root node, and every other node has exact one outgoing edge from it.

An Arborescence is a directed version of a tree. It can also be defined as a tree where all edges are directed towards the root.

The existence of an arborescence that spans all vertices is easy to show, one can just reverse all the edges and start a *BFS* from $r$, if it covers all the edges then it creates an *Arborescence*, hence, one with a minimal weight must exist.

Most of the algorithms for the undirected variants of this problem are not applicable here as most of them are greedy and rely on some [[Properties of Minimum Spanning Trees]] that are not applicable in this scenario. 

An [[Algorithm for Arborescence|algorithm for finding an Arborescence]] that spans all vertices is discussed here.

---
# References
 