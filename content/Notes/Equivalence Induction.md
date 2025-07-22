---
tags:
  - Note
---
202506261706

Tags : [[Homotopy Type Theory]]
# Equivalence Induction
---
>[!theorem]
>Given any type family $D:\prod_{A,B} (A\simeq B) \to \cal U$ and function $d:\prod_{A:\cal U}D(A, A, \text{id}_{A})$, there exists $f:\prod_{A,B:\cal U}\prod_{e:A\simeq B} D(A, B,e)$ such that $f(A, A, \text{id}_{A})=d(A)$ for all $A:\cal U$ 

This states that, to prove something for all equivalences, one only needs to prove it for identity functions. This is another way to state [[Univalence]].

This is because the [[Univalence]] Axiom for a universe $\cal U$ precisely says that the type family:
$$
(- \simeq -):\cal U \to U \to U
$$
together with $id:\prod_{A:\cal U}(A\simeq A)$ satisfies the 4th point in [[Identity System]], hence is equivalent to point 1.

---
# References
- [[Univalence]]
- [[Higher Groupoid Structure of Pi Type|Function Extensionality]]
- [[Identity System]]
- [[Homotopy Induction]]