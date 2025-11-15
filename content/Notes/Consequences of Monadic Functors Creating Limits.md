---
tags:
  - Note
  - Incomplete
---
202510171710

Tags : [[Category Theory]]
# Consequences of Monadic Functors Creating Limits
---
- Inclusion of a reflective subcategory creates all limits
- A reflective subcategory of a complete category is complete.
- Given the [[p-addic integers]] defined as the limit of a diagram of shape $\omega^{\text{op}}$ given as 
  $$
  \mathbb{Z}_{p}:\equiv \lim_{n} \mathbb{Z} / p^n \to \dots \to \mathbb{Z} /p^3 \to \mathbb{Z} / p^2 \to \mathbb{Z}/p
  $$
  can be written as a set (as forgetful functor preserves limits)
  $$
  \mathbb{Z}_{p} = \{ (a_{1} \in \mathbb{Z}/p, a_{2} \in \mathbb{Z}/p^2 \dots) \mid a_{n} \equiv a_{m} \mod p^{\text{min}(m, n)}\}
  $$
  such that the projection maps defined are ring homomorphisms, this tells us that addition and multiplication are componentwise.
- $\text{Set}$ is [[Complete and Cocomplete Categories|cocomplete]]. As the contravariant powerset functor is monadic
- $\text{Mod}_{R}\to\text{Ab}$ creates all colimits that $\text{Ab}$ admits. For any pair of groups $A$ and $A'$, there is a natural isomorphism
  $$
  \text{Ab}(R \otimes _{\mathbb{Z}}A, A') \simeq \text{Ab}(A, \text{Hom}_{\mathbb{Z}}(R, A'))
  $$
  but we know what the tensor product $R\otimes_{\mathbb{Z}}-$ has a right adjoint $\text{Hom}_{\mathbb{Z}}(R, -)$. Due to [[RAPL|LAPC]], $R \otimes_{\mathbb{Z}}-$ preserves all colimits, so the second point of [[Monadic Functors Create all limits and some colimits]] applies to all diagrams. 

---
# References
- [[Monadic Functors Create all limits and some colimits]]