---
tags:
  - Note
  - Incomplete
---
202511121011

Tags : [[Games on Graphs]]
# Probabilistic Perspective Games
---
The idea **probabilistic perspective games** is that from each vertex a player is allowed to have a strategy, where they randomly move to any one of its neighbours:

Thus for a probabilistic strategy involves taking a run, and returning and probability distribution for it.

Given a strategy for both players, a run is uniquely determined and the probability of a finite prefix of a run is defined as the probability of taking each step.

Note that it is proven that any winning condition defined in LTL will be a measurable set.

In deterministic games it is proven that there is an almost surely winning strategy iff there is a winning strategy, but here

>[!theorem]
>There is a game $\cal G$ such that player $1$ can almost $(P, F)$ win, but cannot $P$-win

Take the same game as [[Deterministic Perspective Games]] and give the condition
$$
\theta = \diamond((p \land\circ\#\land\circ\circ p ) \lor(q \land \circ \#\land\circ\circ q))
$$
Player 2 can ruin any deterministic strategy, but not a randomized one, with 50% chance of going in each direction.

>[!theorem]
>There is game that player one can $(PP)$-almost surely win but no $(PF)$-almost surely win.

Consider the same graph but with the condition
$$
\Phi = \diamond((p \land\circ\$\land\circ\circ p ) \lor(q \land \circ \$\land\circ\circ q))
$$
Here, player 2 can always spoil any player 1 strategy, but player 1 can winning by deploying a 50-50 strategy on each moves.

>[!theorem]
>Probabilistic Perspective games are not determinedL

Consider the same graph with the game
$$
\phi \equiv \circ\circ\circ((p\to\circ\circ p)\lor(q\to\circ\circ q))
$$

---
# References
- [[Deterministic Perspective Games]]
- [[Perspective Games]]