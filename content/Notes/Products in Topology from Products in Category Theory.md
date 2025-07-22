---
tags:
  - Note
  - Example
---
202505151505

Tags : [[Category Theory]]
# Products in Topology from Products in Category Theory
---
The product pair of spaces $X$ and $Y$ is a space called $X \times Y$ equipped with continuous projections
$$
X \xleftarrow{\quad\pi_{1}\quad} X \times Y \xrightarrow{\quad\pi_{2}\quad} Y
$$
satisfying the universal property: For any other space $A$ with continuous maps $f:A \to X$ and $g: A \to Y$ , there is a unique morphism $h:A \to X \times Y$ such that the following diagram commutes:
![[Pasted image 20250515153343.png|350]]

Taking $A$ to be the singleton, the underlying set functor $U: \text{Top} \to \text{Set}$, the bijections:
$$
\text{Hom}_{\text{Top}}(*, X \times Y) \cong \text{Hom}_{\text{Top}}(*, X) \times \text{Hom}_{\text{Top}}(*, Y)
$$
How that the underlying set is the cartesian product. 

To define the topology, consider the underlying set of $X \times Y$ and all topologies on it, the universal property tells us that the topology of the space $X \times Y$ should be the coarsest space which makes the projection maps continuous.

Similarly for product of arbitrary spaces, the product topology is again defined to be the coarsest topology which makes the projections continuous.

---
# References
- [[Limits and Colimits]]
- [[Universal Property of Products and Coproducts]]
- [[Product topology]]