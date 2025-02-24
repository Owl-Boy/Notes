---
tags:
  - Note
  - Incomplete
---
202502232202

Tags : [[Finite Model Theory]], [[Logic]]
# Rank-k m,l Types MSO
---
Given a structure $\mathfrak A$, an $m$-tuple $\vec{a} \in A$ and an $l$-tuple $V$ of subsets of $A$, the rank $k$-types of $\vec{a}, \vec{V}$ in $\mathfrak A$ is the set:
$$
\text{mso-tp}_{k} (\mathfrak A, \vec{a}, \vec{V}) = \{ \varphi(\vec{x}, \vec{X})\in \text{MSO}[k] \mid \mathfrak {A} \vDash \varphi(\vec{a}, \vec{V}) \}
$$
Similar to [[Rank-k Types (FO)]], there is an inductive argument that shows 
>[!theorem]
>If we fix $k,m,l$
>- There are only finitely many $\text{MSO}$ rank $k$ $m, l$-types.
>- There is an MSO formula $\alpha_{i}$ such that on every model $\frak A$, the formula is true iff it has type $T_{i}$.

The proof is a straightforward induction.

This will be used to describe the strategy for [[Ehrenfeucht-Fraïssé Game for MSO]].
 
---
# References
