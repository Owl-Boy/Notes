---
tags:
  - Note
---
202504111904

Tags : [[Finite Model Theory]], [[Games on Graphs]]
# Games of Graphs with Fixed Points
---
>[!tip] Game
>Consider the [[Games on Graphs|game]] on graph $G = (V, E)$ with a distinguishing start node $a$.
>On each round $i$:
>- Player 1 first makes the move by selecting the vertex $b_{i}$ such that $(c_{i-1},b_{i})$  is an edge
>- Player 2 then selects the vertex $c_{i}$ such that $(c_{i}, b_{i})$ is an edge
>- On the first move, player 1 must select the vertex $b_{1}$ such that $(a, b_{1})$ is an edge
>  
>The first player to *not* have a legal move loses.

We find the solution of the game by describing the set of points from which player 2 wins in [[Fixed Point Logics|LFP]].

Let $S$ be unary and we define $\alpha(S, x)$ as
$$
\alpha(S, x) :\equiv \forall y \big(E(x, y) \to \exists z(E(y, z) \land S(z))\big)
$$
We get that $F_{\alpha}$ in the $i^\text{th}$ iteration gives the set of points from which player 2 can win, hence we can define the following formula:
$$
[\text{lfp}_{S, x}\alpha(S, x)](a)
$$
which holds iff player 2 has a winning strategy from $a$.

---
# References
