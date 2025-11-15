---
tags:
  - Note
---
202511120711

Tags : [[Games on Graphs]]
# Perspective Games
---
Perspective games capture the idea that players can only view the part of the game that is in their control and have no information over the decisions of the other players until it affects them.

Perspective games are given their name from perspective strategies, which are based only on the part of the run seen by a player, for example, consider a run $\rho=\rho'v_{1}$ such that $v_{1} \in V_{1}$, Then for all such words, our strategy is defined as 
$$
f_{1}:\pi_{1}(\rho')v_{1} \mapsto v:V
$$
note that $\pi_{1}(\rho):V_{1}^*$.

Apart form that, we are adding the information that there is a finite set of atomic proposition $\text{AP}$ such that each state has a set of atomic propositions associated with it, so choose a winning condition to be a set of run that satisfy an [[Linear Temporal Logic|LTL]] formula $\Psi$.

---
# References
- [[Linear Temporal Logic|LTL]]
- [[Deterministic Perspective Games]]
- [[Probabilistic Perspective Games]]