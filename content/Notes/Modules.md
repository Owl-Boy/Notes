---
tags:
  - Note
---
202502191402

Tags : [[Module Theory]], [[Weighted Automata and Transducers]]
# Modules
---
A **Module** is a generalization of a Vector space, where the set of scalars are allowed to be a part of any [[Ring]].

>[!definition]
>A **Left Module** is the tuple $\langle M,R, +, \cdot  \rangle$ such that
>- $\langle M, +\rangle$ for an [[Abelian Groups|Abelian Group]].
>- $R$ is an abelian ring
>- For the operator $\cdot : R \times M \to M$
>	- $r\cdot(x+y)=r\cdot x + r \cdot y$
>	- $(r + s)\cdot x = r \cdot x + s \cdot x$
>	- $rs \cdot x = r \cdot (s \cdot x)$
>	- $1 \cdot x = x$
>
>A **Right Module** is defined by the the operator $\cdot : M \times R \to M$.

A **Module** can also be defined as an action of a [[Ring]] on an [[Abelian Groups]], that is a [[Ring Homomorphisms|Ring Homomorphism]] form a ring $R$ to an the endomorphism ring of an abelian group $M$, written as:
$$
\sigma: R \to \text{End}_{\text{Ab}}(M)
$$
---
# References
- [[Ring]]
- [[Abelian Groups]]
- [[Ring Homomorphisms]]
- [[Examples of Modules]]
- [[Category of Modules]]