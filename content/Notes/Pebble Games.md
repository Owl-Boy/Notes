---
tags:
  - Note
  - Incomplete
---
202504292004

Tags : [[Finite Model Theory]]
# Pebble Games
---
**Pebble Games** are an [[Ehrenfeucht-Fraïssé Game|EF Game]] like characterization for $\mathcal{L}_{\infty, \omega}^\omega$.

>[!tip] Setup
>A $k$-pebble game is played on 2 structures $\frak A, B$, by 2 players, the *Spoiler* and the *duplicator* where the players have pairs of pebbles $(p_{i}^\mathfrak A, p_{i}^\mathfrak B)_{i \in [k]}$

>[!definition] Gameplay
>The game is played as follows:
>1. Spoiler Picks a model
>	1. We assume spoiler picked $\frak A$
>2. Spoiler takes a pebble $p_{i}^\mathfrak A$ and moves it to a different location.
>3. The duplicator responds by moving the pebble $p_{i}^\mathfrak B$.

>[!attention] Winning Condition
>We denote the finite $n$-round game with $\text{PG}_{k}^n(\mathfrak A, \mathfrak B)$ and the infinte game with $\text{PG}_{k}^\infty(\mathfrak A,\mathfrak B)$.
>After each round the pebbles define a relation $F \subseteq A \times B$.
>The duplicator wind the game if they can ensure that the pebbles give an isomorphism. We then state $\mathfrak A \equiv_{k,n}^{\infty,\omega} \mathfrak B$ or $\mathfrak A \equiv_{k,n}^{\infty,\omega} \mathfrak B$.

>[!theorem]
>Two structures $\mathfrak A, \mathfrak B$ agree on all sentences of $\mathcal{L}_{\infty, \omega}^k$ up to quantifier rank $n$ iff $\mathfrak A \equiv_{k, n}^{\infty, \omega}\mathfrak B$.
>They agree on all sentences iff $\mathfrak A \equiv _k^{\infty, \omega}, \mathfrak B$.

---
# References
