---
tags:
  - Note
  - Incomplete
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

Now consider a game where all cycles are even, we need to construct a parity progress measure.

---
# References
