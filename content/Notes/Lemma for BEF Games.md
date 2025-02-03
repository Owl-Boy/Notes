---
tags:
  - Note
  - Incomplete
---
202501312301

Tags : [[Finite Model Theory]]
# Lemma for BEF Games
---
>[!lemma]
> $\mathfrak A \simeq_{k}^\text{bij} \mathfrak B$ iff $\mathfrak A \equiv_{k}^\text{bij} \mathfrak B$ 

By [[Local Equivalence Lemma]], $(\mathfrak A, \vec{u})\leftrightarrows_{3d+1}(\mathfrak B, \vec{v})$ implies the existence of a bijection such that $(\mathfrak A, \vec{uc})\leftrightarrows_{d}(\mathfrak B, \vec{v}f(c))$. Since the winning condition for the bijective game is that $N_{0}^\mathfrak A \cong N_{0}^\mathfrak B$, where $\vec{a}$ and $\vec{b}$ are teh moves of the game on $\mathfrak A$ and $\mathfrak B$, by induction on $k$ we conclude:

>[!lemma] Corollary
>If $(\mathfrak A, \vec{a}) \leftrightarrows_{\frac{3^k-1}{2}} (\mathfrak B, \vec{b})$ then $(\mathfrak A, \vec{a}) \equiv_{k}^\text{bij}(\mathfrak B, \vec{b})$.

Since bijective games are harder than standard [[Ehrenfeucht-Fraïssé Game|EF games]], they characterize a logic that is more expressive than [[First Order Logic|FO]]. 

---
# References
