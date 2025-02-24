---
tags:
  - Note
  - Incomplete
---
202502232302

Tags : [[Finite Model Theory]]
# Ehrenfeucht-Fraïssé Game for MSO
---
>[!tip] Setup
>An MSO game is played between 2 people, a *spoiler* and a *duplicator*, on an arena which consists of 2 structures $\mathfrak A$ and $\mathfrak B$ with the same vocabulary $\sigma$. The goal of the *spoiler* is to show that the models are different, and the goal of the duplicator is to show that they are the same.

An example game is given in [[Even is not MSO-expressible]]
## Gameplay
In the [[Monadic Second Order Logic|MSO]] *Ehrenfeucht-Fraïssé Game*, the players play a certain number of rounds, and each round consists of the following steps.
1. *Spoiler* picks a structure
2. Then the *Spoiler* can either pick a point or a set of points from that model.
3. Then the *Duplicator* responds by picking a point or a set of points in the other model.

## Winning 
After $n$ rounds, both the players will have a vector of points and sets $(\mathfrak A, \vec{a}, \vec{V})$ and $(\mathfrak B, \vec{b}, \vec{U})$, then we have that the duplicator wins iff $\text{mso-tp}_{k}(\mathfrak A, \vec{a}, \vec{V}) =\text{mso-tp}_{k}(\mathfrak B, \vec{b}, \vec{U})$ which is the same as $(\mathfrak A, \vec{a}, \vec{V}) \equiv_{k}^\text{MSO}(\mathfrak B, \vec{b}, \vec{U})$.

---
# References
