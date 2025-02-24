---
tags:
  - Note
  - Incomplete
---
202502191402

Tags : [[Weighted Automata and Transducers]], [[Module Theory]]
# Semi-Modules
---
**Semimodules** are [[Modules]] that are defined over a commutative [[Monoids|monoid]] instead of an [[Abelian Groups|Abelian Group]].

>[!definition]
>A **Left Semimodule** is the tuple $\langle M,R, +, \cdot  \rangle$ such that
>- $\langle M, +\rangle$ for an [[Abelian Groups|Abelian Group]].
>- $R$ is a commutative monoid.
>- For the operator $\cdot : R \times M \to M$
>	- $r\cdot(x+y)=r\cdot x + r \cdot y$
>	- $(r + s)\cdot x = r \cdot x + s \cdot x$
>	- $rs \cdot x = r \cdot (s \cdot x)$
>	- $1 \cdot x = x$
>
>A **Right Module** is defined by the the operator $\cdot : M \times R \to M$.

---
# References
