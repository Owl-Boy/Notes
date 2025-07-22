---
tags:
  - Note
---
202505151505

Tags : [[Category Theory]]
# Products and Coproducts
---
>[!definition]
>A **Product** is a [[Limits and Colimits|Limit]] of a diagram indexed by a discrete category, with only identity morphisms. 

A diagram indexed by such a category $J$ is just a collection of objects $F_{j}\in C$ for each $j\in J$ and a cone over this is simply a collection of morphisms $\lambda_{j}:c \to F_{j}$. 

The limit is typically denoted by $\prod_{j\in J}F_{j}$ while the legs are denoted by the maps
$$
\left( \pi_{k} : \prod_{j\in J}F_{j} \to F_{k} \right)_{k\in J}
$$
which are also called **Projections**, the universal property asserts that composition with the projection map defines a universal isomorphism:
$$
C\left( c, \prod_{j\in J}F_{j} \right) \underset{\quad\cong\quad}{\xrightarrow{(\pi_{k})_{*}}} \prod_{k\in J} C(c, F_{k}) \cong \text{Cone}(c, F)
$$

[[Products in Topology from Products in Category Theory|Here are some examples]].

>[!definition]
>$\coprod_{j\in J} A_{j}$ is the colimit of the diagram $(A_{j})_{\in J}$ indexed by the discrete category $J$. The legs of the colimit cone $\iota_{j'}: A_{j'}\to \coprod_{j\in J}A_{j}$ are referred to as **coproduct injections**, though there are not necessarily injections.

---
# References
- [[Limits and Colimits]]
- [[Universal Property of Products and Coproducts]]
- [[Products in Topology from Products in Category Theory]]