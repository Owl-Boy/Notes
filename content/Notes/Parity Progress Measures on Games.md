---
tags:
  - Note
---
202509182209

Tags : [[Games on Graphs]]
# Parity Progress Measures on Games
---

>[!definition]
>Given:
>- A graph $G=(V, E)$
>- Max priority degree $d$
>- a function $\xi:V \to \mathbb{N}^{\lceil d/2 \rceil}+\{ \top \}$
>
>We call such a function a **game parity progress measure** if for all vertices $v\in V$:
>- If $v\in V_{E}$ and $\xi(v)\neq \top$, then $\xi^{[p(v)]}\geq \min_{(v, w)\in E}\xi^{[p(v)]}(w)$
>	- and if $p(v)$ is odd then the inequality is strict.
>- If $v\in V_{E}$ and $\xi(v)\neq \top$, then $\xi^{[p(v)]}\geq \max_{(v, w)\in E}\xi^{[p(v)]}(w)$
>	- and if $p(v)$ is odd then the inequality is strict.
>
>An intuitive way to understand it would be, our progress measure is sort of like a count to the next good vertex, thus, it should get strictly smaller if we are at an odd vertex. Furthermore, if we are at an even player vertex, then we get to pick our path, then we only need the $\min$ to have a favourable value. If we are at an odd player vertex, then we need the progress to improve in the  best possible way, hence we pick the $\max$.

This here becomes a really useful metric for defining a winning strategy for parity games, due to the following lemma which is very similar to the lemma defined for [[Parity Progress Measures on Graphs]].

>[!lemma]
>For every $0$-dominion $D\in V$, there is a game parity progress measure $\xi$ such that $\text{dom}(\xi)=D$.
>Furthermore, The set $\text{dom}(\xi)$ of a game parity progress is a $0$-dominion.

---
# References
- [[Parity Progress Measures on Graphs]]
- [[Progress Measures (Intuition)]]
- [[Least Progress Measure]]