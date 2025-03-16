---
tags:
  - Note
  - Incomplete
---
202503091203

Tags : [[Topics in Algorithms]]
# Multi-way Cuts
---
>[!question]
>Given a graph $G= (V, E)$  and a subset $S$ of vertices, the goal is to find the set of edges with the smallest total weight such that removing those edges from $G$ disconnects every vertex in $S$ with every other vertex.

Multiway cut problem, or Multiterminal cut problem is a generalization of the [[Min-cut Problem]].

>[!example] Application in Distributed Computing
>Each vertex represents an object, and an edge $e$ of cost $c_e$ between them represents the cost of communication between the objects. The objects have to be partitioned to reside on $k$ different machines, with special object $s_i$ residing on the $i^\text{th}$ machine. The goal is to partition the objects residing on the $k$ machines in such a way that the communication cost between the machines is minimized

We know the following facts about this problem:
- The Multiway cut problem has an efficient solution if $S$ has just 2 elements, It is then equivalent to [[Min-cut Problem]]
- If there are more than $2$ elements in $S$ then the problem is [[NP (Complexity Class)|NP-Hard]]
- Multiway Cut with more than 2 elements in $S$ is also known to be [[APX (Complexity Class)|APX-Hard]]
- Multiway Cut can be solved exactly for $k$

One of the greedy algorithms to solve the problem is given in [[Isolating Cut Heuristic for Multicut Problem]]


---
# References
