---
tags:
  - Note
---
202504280204

Tags : [[Finite Model Theory]]
# Game for Counting Logic
---
>[!tip] Setup
>A Bijective [[Ehrenfeucht-Fraïssé Game]] is played between 2 players, the *spoiler* and the *duplicator*. The Arena for the game is 2 first order structures and the goal of the duplicator is prove that these are the same, and the goal for the spoiler is to show that the structures are different.

>[!definition] Gameplay
>Given 2 structures $\mathfrak A$ and $\mathfrak B$, the spoiler directly wins if $|A| \neq |B|$. If $|A| = |B|$, the duplicator starts by giving a bijection $f:A \to B$ between the 2. Then the game is played for $n$ rounds, in each round the spoiler first picks a vertex $a: A$, and then for duplicator choice, the vertex $f(a):B$ is picked. If after $n$ rounds, these points form a partial isomorphism then the duplicator wins, otherwise the spoiler wins.

This seems significantly harder for the duplicator as they have to reveal their entire strategy before the game and their strategy can't have them pick the same point for multiple choices of the spoiler.

>[!theorem]
>Given 2 structures $\mathfrak A$ and $\mathfrak B$, the following are equivalent:
>- $\mathfrak A \equiv^{\text{bij}}_{k} \mathfrak B$
>- $\mathfrak A$ and $\mathfrak B$ agree on all $\mathcal{L}_{\infty, \omega}^*\text{(Cnt)}$ formulas of rank at most $k$.

---
# References
