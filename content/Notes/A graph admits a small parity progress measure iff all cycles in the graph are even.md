---
tags:
  - Note
---
202509180209

Tags : [[Games on Graphs]]
# A graph admits a small parity progress measure iff all cycles in the graph are even
---
>[!theorem]
>A graph $G$  has all its cycles even iff there exists a [[Parity Progress Measures on Graphs|parity progress measure]] on $G$.

We first show that if a graph has a parity progress measure, then all its cycles have max degree even. 

Given a parity progress measure and a cycle in the graph, If the maximum degree is odd $k$, then in the cycle, there are either vertices of degree $k$ or vertices of degree smaller $k$, hence for the cycle the value of $\xi^{k}$ strictly goes down for some vertices and possibly stays the same, which is a contradiction.

Now we show that if all cycles of a graph are even then there exists a small parity progress measure.

Now consider a game where all cycles are even, The idea is an induction on the maximum degree. If the maximum degree is even, we delete all such vertices, and we find parity progress measure for the leftover graph, we can also assume them to be sink states with measure 0.

If the maximum degree is odd, the these vertices divide the graph into components such that we can treat the entire graph as a DAG, where the vertices are these maximum odd degree vertices and the edges correspond to the connected components. We can then perform a toposort and use the values to define the maximum entry in the measure. For all of the components, we define the measure to be the maximum from all incoming max degree vertices, the rest is similar to the previous case.



---
# References
[[Parity Progress Measures on Graphs]]
[[Progress Measures (Intuition)]]