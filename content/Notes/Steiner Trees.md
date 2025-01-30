---
tags:
  - Note
---
202501230301

Tags : [[Topics in Algorithms]], [[Advanced Algorithms]]
# Steiner Trees
---
Given a graph $G = (V, E)$, let $K\subseteq V$. We define a steiner tree as follows:

>[!definition]
>A *Steiner Tree* $T$ is a sub-tree of $G$ such that $K\subseteq V_{t}$.

A steiner tree is a sub-tree of a graph which definitely contains a subset $K$ of the vertices and can potentially contain vertices that outside of $K$.

The problem of finding if there exists a steiner tree of weight less than some $d$ given a graph $G$ is $\text{NP-COMPLETE}$, then analysis is given [[Steiner Trees are NP Complete|here]].

Since the problem is [[NP Complete]], there is no known polytime algorithm for solving the problem. There is a polytime approximation algorithm for finding a Steiner tree of a graph which is a 2-approximation, that is discussed in: [[Polytime Approx Algo for Steiner Trees]].

---
# References
