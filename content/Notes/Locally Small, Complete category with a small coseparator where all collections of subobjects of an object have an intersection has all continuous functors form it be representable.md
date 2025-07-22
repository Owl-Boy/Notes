---
tags:
  - Note
---
202507210207

Tags : [[Category Theory]]
# Locally Small, Complete category with a small coseparator where all collections of subobjects of an object have an intersection has all continuous functors form it be representable
---
>[!theorem]
>Suppose $C$ is locally small, complete, has a small coseparating set, and has the property that every collection of subobjects of a fixed object has an intersection. Then any continuous functor $F:C\to\text{Set}$ is representable.

By [[Special Adjunct Functor Theorem]], $F$ has a left adjoint $L:\text{Set}\to C$. In particular there is a natural isomorphism
$$
C(L(*), c)\cong \text{Set}(*, Fc)\cong Fc
$$
where $*$ is the singleton set. The object $L(*)$ represents $F$.

---
# References
