---
tags:
  - Note
  - Incomplete
---
202501312201

Tags : [[Finite Model Theory]]
# Bijective Ehrenfeucht-Fraïssé Game
---
This is a stronger and more restrictive locality criteria than the general [[Ehrenfeucht-Fraïssé Game]].

Just as the standard notion, we have $\mathfrak A \equiv_{0}\mathfrak B$, here the duplicator wins iff $(\emptyset, \emptyset)$ is a partial isomorphism. We start here and construct the new relation as follows:

>[!definition]
>- $\mathfrak A \simeq^\text{bij}_{0} \mathfrak B$ if $\mathfrak A \equiv_{0} \mathfrak B$;
>- $\mathfrak A \simeq^\text{bij}_{k+1} \mathfrak B$ if there is a bijection $f: A \to B$ such that
>	- **Forth:** for each $a\in A$, we have $(\mathfrak A, a)\simeq^\text{bij}_{k}(\mathfrak B, f(a))$
>	- **Back:** for each $b\in B$, we have $(\mathfrak A, f^{-1}(b))\simeq_{k}^\text{bij}(\mathfrak B, b)$
>

Here just 1 of the **Back** and **Forth** is enough since this is a bijection.

Given 2 structures $\frak A$ and $\frak B$ be two structures in a relational vocabulary. There is a $k$-round game played between the same 2 players. If $|A| \neq |B|$, then the duplicator loses before the game even starts. In the $i^\text{th}$ round, the duplicator first selects a bijection $f_{i} : A \to B$. The spoiler moves exactly like they do in the original game, and duplicators response is either $f(a_{i})$ or $f^{-1}(b_{i})$.

Just as in EF games, duplicator wins if there is partial isomorphism between the $\mathfrak A$ and $\mathfrak B$.

---
# References
