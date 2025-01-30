---
tags:
  - Note
  - Incomplete
---
202501292301

Tags : [[Finite Model Theory]]
# Gaifman-Locality
---
>[!definition]
>An $m$-ary query $Q$, $m>0$ on $\sigma$-structures $\mathfrak{A}$ and every $\vec{a}_{1}, \vec{a}_{2} \in A^m$,
>$$
>\begin{matrix}
> N_{d}^\mathfrak A (\vec{a}_{1})\cong N_{d}^\mathfrak A(\vec{a}_{2}) & \text{implies} & (\vec{a}_{1} \in Q(\mathfrak A) \iff a_{2}\in Q(\mathfrak A))
>\end{matrix}
>$$


The minimum $d$ for which the above holds is called the locality rank of $Q$ and is denoted by $\text{lr}(Q)$.

One important difference [[Hanf-Locality]] and [[Gaifman-Locality]] is that the former talks about 2 structures while the latter talks about locality on one structure.

The way to use *Gaifman-locality* to show that query $Q$ is not definable in a logic $\mathcal{L}$ is:
- Show that all $m$-ary queries, $m>0$ every $\mathcal{L}$ query is *Gaifman-local*, 
- Show that $Q$ is not *Gaifman-local*

---
# References
