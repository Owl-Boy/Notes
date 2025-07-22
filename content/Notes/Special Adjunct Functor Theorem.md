---
tags:
  - Note
---
202507210107

Tags : [[Category Theory]]
# Special Adjunct Functor Theorem
---
>[!theorem]
>Let $U:A\to S$ be a continuous functor, whose domain is complete and whose domain and codomain are locally small. Furthermore if $A$ has a small coseparating set and every collection of subobjects of a fixed object in $A$ admit and intersection, then $U$ admits a left-adjoint.

For each $s\in S$, the category $s\downarrow U$ is locally small and complete. Monomorphisms in $s\downarrow U$ are preserved and reflected by $\prod:s\downarrow U\to A$, so the comma category has intersection of subobjects created by this functor. If $\Phi$ is a coseparating set for $A$ then the set
$$
\Phi' = \{ s\to Ua\mid a\in \Phi \}
$$
is a coseparating set of $s\downarrow U$, because $S$ is locally small $\Phi'$ is a set. Applying [[A locally small, complete category with a small coseparator and intersections of all collections of subobjects has an initial object]], we get that each comma category provides a left adjoint, by [[A functor admits a left adjoint iff all its comma categories have an initial object]].

---
# References
- [[Subobjects]]
- [[A locally small, complete category with a small coseparator and intersections of all collections of subobjects has an initial object]]
- [[A functor admits a left adjoint iff all its comma categories have an initial object]]
- [[Monomorphisms and Epimorphisms]]
- [[Preservation, Reflection and Creation of Limits]]
- [[Adjunctions]]