---
tags:
  - Note
---
202507191607

Tags : [[Category Theory]]
# Adjoints of Inclusion functor from Ring to Rng
---
Consider the functor $I:\text{Ring}\hookrightarrow\text{Rng}$ which is the inclusion functor. Our goal is to find adjoints of this functor.

The first idea we can try using is [[RAPL]], because $\mathbb{Z}$ is the initial object in $\text{Ring}$. We see that $\mathbb{Z}$ is not initial in $\text{Rng}$ so there can be no right adjoint.

But we have that the trivial ring is the terminal object in both $\text{Rng}$ and $\text{Ring}$ so there might be a left adjoint.

Finding a left adjoint is to a non-unital ring $R$ involves finding a ring $R^*$ such that the following natural isomorphism holds:
$$
\text{Ring}(R^*, S)\cong \text{Rng}(R, S)
$$
for all non-unital rings $S$. To define this natural isomorphism is to define the representation of the functor $\text{Rng}(R, -):\text{Rng}\to\text{Set}$. By [[Universal Elements are Universal Elements]], a representation defines an initial object the [[Element Category]]:$\int\text{Rng}(R, -)$. Objects in this category are homomorphisms $R\to S$ whose codomain is a unital ring and morphisms are commutative triangles like:
![[Pasted image 20250719162503.png|200]]

This category is isomorphic to the [[Comma Category]] $R\downarrow\text{Ring}$. We will solve the problem if new find a unital ring $R^*$ and a ring homomorphism $R\to R^*$ that is initial in this category.

This leads to the following general lemma: [[A functor admits a left adjoint iff all its comma categories have an initial object]].

---
# References
- [[Adjunctions]]
- [[RAPL]]
- [[Comma Category]]
- [[Universal Elements are Universal Elements]]
- [[Universal Property (Riehl)]]
- [[A functor admits a left adjoint iff all its comma categories have an initial object]]
- [[Element Category]]