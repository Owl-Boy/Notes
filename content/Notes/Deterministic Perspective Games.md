---
tags:
  - Note
---
202511120911

Tags : [[Games on Graphs]]
# Deterministic Perspective Games
---
In a **Deterministic Perspective Game**, each player gets to pick exactly 1 outgoing state for the token to go to, when it is in their part of the graph, consider the following graph:
![[Pasted image 20251112093458.png]]
>[!example]
>Consider the winning condition
>$$
>\square\diamond ((p \to \circ\circ p) \land (q \to \circ\circ q))
>$$
>Here Player 1 can win by copying the move from player 2, but actually, player 1 can also just alternate between $p$ and $q$ and it will still be winning for them. The first is a finite memory strategy while the second is a positional, hence perspective strategy.

But we have the following theorem:
>[!theorem]
>Given a game $\cal G$, we have that $\cal G$ is:
>- $FF$ winning for player 1 $\iff$ $FP$ is winning for player 1
>- $PF$ winning for player 1 $\iff$ $PP$ is winning for player 1

Left to right is trivial, for right to left, argument is the same, so consider an $FF$ game such that for each strategy $\sigma$, there is an $F$ strategy $\tau$ such that $\tau$ defeats $\sigma$. To make a $P$ strategy out of $\tau$, note that the game is determined by $\sigma$ and $\tau$, thus player 2 can themselves fill in the information about parts of the run from $\sigma$ if not given, thus giving a perspective strategy.

Thus we can talk about $F$ and $P$ winning strategies in stead of $FF$, $FP$...
As it is not dependent on the second player. It does however matter for the first player.

>[!theorem]
>There is a game that is $F$-winnable by player 1 but not $P$-winnable.

Consider the above graph with the condition
$$
\Psi \equiv \square((($ \land \circ p)\to\circ\circ\circ p) \lor(($ \land \circ q)\to\circ\circ\circ q))
$$
There is an obvious $F$ winning strategy for player $1$ and player 2 has an obvious winning strat if player 1 cannot use $F$ strat, player 2 can simply counter the next move that player 1 would play.

>[!theorem]
>Perspective games are not determined

The previous example has that player 1 cannot have a winning strategy, similarly, since the game is F-winnable for player 1, player 2 does not have a P-winning strategy either.

---
# References
- [[Perspective Games]]
- [[Probabilistic Perspective Games]]