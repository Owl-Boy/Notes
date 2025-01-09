---
tags:
  - Note
  - Incomplete
---
202501081701

Tags : [[Finite Model Theory]]
# Connectivity is not FO definable for Finite Graphs
---
Since **Compactness** Fails for finite models, the standard ways of proving the idea discussed in [[Connectivity is not FO Definable]] does not work.

To prove the statement for finite graphs, one can consider the following 2 families:
- $A_{n}$: Cycles of length $n$.
- $B_{n}$: 2 copies of $A_{n}$.

Let $S_{A}$ be the set of formulas which are satisfied by all but finitely many $A_{n}$. symmetrically let $T_{A}$ be the set of formulas which are satisfied by all but finitely many $B_{n}$.

Now we extend the signature of the language by countably many constants $c_{n}$ to write the formulas: $F_{i,j,k}:$ there is no path of length $k$ from $c_{i}$ to $c_{j}$. and let $\cal F$ be the set of all $F_{i,j,k}$.

Now we can define $S = S_{A } \cup \cal F$ and $T = T_{A} \cup \cal F$. 

We can say that the statement "for every vertex there is exactly 1 incoming and 1 outgoing edge". This statement belongs to both $S$ and $T$.

By Lower Lowenheim Skolem theorem, there is a countable model for both $S$ and $T$.

But it needs to satisfy the formula about 1 indegree and 1 outdegree, along with all formulas in $F$. So it must look like countable copies of $\mathbb{Z}$, one for each $c_{n}$. Then it would just look like countable copies of $\mathbb{Z}$ for $S_{A}$ and $T_{A}$, which means both sets of formulas have the same cardinality. And are hence isomorphic. 

This is a contradiction as $S$ contains the formula about connectivity but $T$ contains its negation. So they cannot have the same model.

---
# References
[[Logical Compactness]]
[[Connectivity is not FO Definable]]