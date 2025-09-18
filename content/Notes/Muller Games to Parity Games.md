---
tags:
  - Note
---
202509131709

Tags : [[Games on Graphs]]
# Muller Games to Parity Games
---
[[Last Appearance Record]] can be used to convert Muller Games to Parity games similar to how the note discusses the conversion of Muller Games to Rabin games. 

Let $(G, \cal F)$ be a muller game with $n$ vertices and let $\cal S$ be the [[Last Appearance Record|LAR]] automaton for the game described as
$$
\mathcal S = (S, V, s_{0}, \delta) 
$$
And let $G'$ be the games obtained by taking the product with $\cal S$, then consider the following colouring function:
$$
c((i_{1}\dots i_{r}), h) = \begin{cases}
2h & \text{if } \{ i_{1}\dots i_{h} \}\in \cal F \\
2h-1 & \text{if } \{ i_{1}\dots i_{h} \}\not\in \cal F 
\end{cases}
$$

Using this, the player that needs to satisfy the muller condition, becomes the even player for parity game.

---
# References
- [[omega-Automata]]
- [[Last Appearance Record]]