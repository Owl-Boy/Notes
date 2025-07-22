---
tags:
  - Note
  - Incomplete
---
202506201606

Tags : [[Category Theory]]
# Monoidal Category
---
A **Monoidal Category** is a category with a product operator defined on its objects that works like a monoid.

>[!example]
>The category $\text{Set}$ is a monoidal category under both catesian product and disjoint union operators.
>
>The [[Category of Modules]] is closed under direct sum.

>[!definition]
>A category  $C$ is **Monoidal** when it is equipped with the following:
>- A functor $\otimes: C \times C \to C$, this is called the tensor product.
>- An object $\mathbf{1}:C$
>Along with natural isomorphism that give properties of the monoid to the product
>- $\lambda_{c}:\mathbf{1}\times c \cong c$
>- $\rho:c \times 1\cong c$
>- $\alpha_{x, y, z}: (x \otimes y)\otimes z \cong x \otimes(y \otimes z)$
>Along with the following coherence diagrams
>- ![[Pasted image 20250620164449.png|200]]
>- ![[Pasted image 20250620164504.png|450]]

---
# References
