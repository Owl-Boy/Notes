---
tags:
  - Note
---
202502240002

Tags : [[Finite Model Theory]]
# Even is not MSO-expressible
---
Let $\sigma = \emptyset$. Here the goal is to figure out if a model is of even size or not.

Turns out, for $2$ models $\mathfrak { A, B }$ such that $|A|, |B|>2^k$ then $\mathfrak A \equiv_{k}^\text{MSO} \mathfrak B$.
>[!success] Strategy for *duplicator*
>The strategy is very similar to [[Even Atoms in Boolean Algebras]].
>
>We shall satisfy the following invariant:
>- Both players here get to choose sets, and hence will partition the models each time a move is played, 
>- so at turn $i$ if the new partition created by the *spoiler* is of size more than $2^i$, then the partition created by the *duplicator* will also be of a size more than $2^i$, 
>- otherwise it will be of the same size.
>
>The strategy itself goes as follows:
>- Suppose the *spoiler* picks a set $U \subseteq A$, then we have the following cases:
>	- $|U|<2^{k-1}$, then we have that $|A\setminus U|>2^{k-1}$: In this case, the *duplicator* must pick a subset $V\subseteq B$ such that $|V| < 2^{k-1}$.
>	- $|U^C|<2^{k-1}$, Then we do the same strategy but with the complement.
>	- $|U^C|\geq 2^{k-1}$ and $|U|\geq 2^{k-1}$: In this scenario the *duplicator* must also find a set like that in $B$
>- Now the arena is divided into 2 parts, the parts are either of size more than $2^{k-1}$, in which a game can be played and won by the *duplicator*, or they are of the same size, where the *duplicator* will clearly win.

---
# References
