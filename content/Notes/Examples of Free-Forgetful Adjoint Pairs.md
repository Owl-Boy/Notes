---
tags:
  - Example
---

202507021717

tags : [[Category Theory]]

#  Examples of Free-Forgetful Adjoint Pairs
---
The following forgetful functors admit left adjoints defining "free construction".
- $U:\text{Set}_{*}\to\text{Set}$. The left adjoint takes $X$ to $X_{+}:= X \sqcup \{ X \}$.
- $U:\text{Monoid}\to\text{Set}$. The [[Free Monoid]] on a set $X$ is the set $\prod_{n\geq {0}}X^{\times n}$
- $U:\text{Ring} \to\text{Ab}$, forgetting the multiplicative structure. The free abelian ring on the group $A$ is $\bigoplus_{n\geq 0}A^{\otimes n}$.
- $U:\text{Ab}\to\text{Set}$. The Left adjoint defines the [[Free Abelian Group]].
- $U:\text{Mod}_{R}\to S$. The Left adjoint defines the [[Free Module]].
- $U:\text{Ring}\to\text{Set}$. The left adjoint can be constructed by composing the let adjoints $\text{Set}\to\text{Ab}\to\text{Ring}$. Its the free monoid on the free abelian group.
- $(-)^\times:\text{Ring}\to\text{Group}$ which maps a ring to its group of units. The free ring on a group $F$ is the group ring $\mathbb{Z}[G]=\bigoplus_{G}Z$. Whose elements are finite formal sums of group elements. The group operation defines a bilinear multiplication law.
- $U:\text{Group}\to\text{Set}$. The left adjoint defines the [[Free Group]]. 
- $U:Ab \hookrightarrow\text{CMonoid}$, the inclusion. has the left adjoint $\text{Gr}$ which carries a commutative monoid $(M,+,0)$ to its group completion, also called the _Grothendieck Group_: the set $\text{Gr}(M,+,0)$ is the quotient of $M \times M$ by the relation $(a, b) \simeq (a',b')$ iff there is a $c$ such that $a+b'+c=a'+b+c$.
- $U:\text{Group} \hookrightarrow\text{Monoid}$. The left adjoint contructs the "group completion" of a monoid as a quotient of the free group on its underlying set mod the monoid relation.
- ---
# Related
- [[Adjunctions]]
- [[Free Monoid]]
- [[Free Abelian Group]]
- [[Free Module]]
- [[Free Group]]