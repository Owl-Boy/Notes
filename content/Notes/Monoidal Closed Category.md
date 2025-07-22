---
tags:
  - Note
  - Incomplete
---
202506201606

Tags : [[Category Theory]]
# Monoidal Closed Category
---
A **Monoidal Closed Cateogry** is one which is both moniodal can closed in a way that the two properties respect each other. 

>[!definition]
>The category of $\text{Set}$ is a monoidal closed category, with the internal hom functor, and the tensor product as the cartesian product.
>The category $\text{Vect}_{k}$ forms a monoidal closed category with tenrsor product as tensor product and internal hom functor.
>The category $\text{Ab}$ of abelian groups with tensor product and internal hom functor form a monoidal closed category.

>[!definition]
>A **Monoidal Closed Category** is a category $C$ equipped with the structure of both a [[Monoidal Category]] and a [[Closed Category]], that is, the functors:
>- $\otimes:C \times C \to C$, which is called the tensor products
>- $[-,-]:C^\text{op}\times C\to C$ called the internal hom functor
>Along with the object $\mathbf{1}$ that satisfes all properties that monoidal categories and closed categories have, along with the ability to curry, functions, that is the natural isomorphism:
>$$
>\text{Hom}_{C}(X \otimes Y, Z) \cong \text{Hom}_{C}(X, \text{Hom}_{C}(Y, Z))
>$$
>for any object $X, Y, Z$.


---
# References