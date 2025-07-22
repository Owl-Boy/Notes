---
tags:
  - Note
---
202507141507

Tags : [[Category Theory]]
# Limits and Colimits as Adjunctions
---
>[!theorem]
>A category $C$ admits all limits of diagrams indexed by a small category $J$ iff the constant diagram functor $\Delta:C\to C^J$ admits a right adjoint. It admits all colimits of $J$-indexed diagram iff $\Delta$ admits a left adjoint.:
>![[Pasted image 20250714155247.png|150]]

These adjoints define the limit and colimit functors.

The dual statement is immediate. For $c\in C$ and $F\in C^J$, the hom set $C^J(\Delta c,F)$ is the set of universal transformations from the constant diagram at $c$ to $F$. This is precisely the set of cones over $F$ with summit $c$. There is also an object $\text{lim }F\in C$ such that 
$$
C^J(\Delta c, F)\cong C(c, \text{lim }F)
$$
that is natural in $c$ iff the limit exists. If such a natural isomorphism exists for all diagram $F\in C^J$, then by  [[Unique construction of Adjunction]] we can extend the objects $\text{lim }F$ to a limit functor $C^J\to C$.

---
# References
- [[Adjunctions]]
- [[Limits and Colimits]]
- [[Unique construction of Adjunction]]
- [[Duality]]