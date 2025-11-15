---
tags:
  - Note
---
202511152211

Tags : [[Games on Graphs]], [[Logic]]
# Perspective-ATL*
---
$\text{Perspective-ATL}^*$ is an extension of [[Alternating-time Temporal Logic|ATL]] that allows one to quantify over [[Perspective Games|Perspective strategies]] we thus augment the syntax using the following

$$
\begin{matrix}
\Phi'  & :\equiv & \Phi  & | & \langle\!\langle A\rangle\!\rangle_{P} \Psi   & | &  \langle\!\langle A\rangle\!\rangle_{M} \Psi
\end{matrix}
$$

And the semantics
- $\langle\!\langle A\rangle\!\rangle_{P}$ quantifies of perspective strategies for players in $A$ and all strategies for the other player.
- $\langle\!\langle A\rangle\!\rangle_{M}$ quantifies of memoryless strategies for players in $A$ and all strategies for the other player.

---
# References
- [[Alternating-time Temporal Logic|ATL]]
- [[Perspective Games]]
- [[Semantics of ATL*]]