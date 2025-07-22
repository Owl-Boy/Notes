---
tags:
  - Example
---
202507071407

Tags : [[Category Theory]]
# Examples of Mutual left and right adjoints
---
>[!example]
>Fix an natural number $n$ and an algebraically closed field $\mathbb k$ and consider the set of elements in the polynomial ring $\mathbb{k}[x_{1},x_{2}\dots x_{n}]$ and in the vector space $\mathbb k^n$. Then there are contravariant functors between the powerset poset as follows:
>$$
>P(\mathbb k[x_{1}\dots x_{n}])^\text{op} \xrightarrow V P(\mathbb k^n)\quad\text{and} \quad P(\mathbb k^n)^\text{op}\xrightarrow{I} P(\mathbb k[x_{1}\dots x_{n}])
>$$
>Where
>- $V$ sends a set of polynomials to the set of points where all the polynomials are zero.
>- $I$ sends a set of points to the set of polynomials which are zero on all points of $I$
>
>This defines a mutual right adjoint because 
>$$
>T \subseteq V(S) \quad \text{iff}\quad S \subseteq I(T)
>$$
>And units encode:
>$$
>T \subseteq V(I(T)) \quad\text{and}\quad S \subseteq I(V(S))
>$$
>The fixed points of units are closely related to [[Zarisky Topology]].

>[!example]
>Let $\sigma$ be a [[Syntax of First Order Logic|vocabulaty]] and let $\text{Axiom}_{\sigma}$ be a set of axioms whose signature is $\sigma$ and let $\text{Struct}_{\sigma}$ be a set of $\sigma$-[[Semantics of First Order Logic|structure]].
>
>Let $M \subseteq\text{Struct}_{\sigma}$ and $A \subseteq\text{Axiom}_{\sigma}$. We say that $M \vDash A$ if all axioms in $A$ are true in all models in $M$.
>
>This gives us the following contravariant functors:
>$$
>P(\text{Axiom}_{\sigma})^\text{op}\xrightarrow{\text{True in}}P(Struct_{\sigma})
>$$
>and
>$$
>P(\text{Struct}_{\sigma})^\text{op}\xrightarrow{\text{Satisfies}}P(\text{Axiom}_{\sigma})
>$$
>These are mutual right adjoints, forming the [[Galois Connection]] between [[Syntax of First Order Logic|Syntax]] and [[Semantics of First Order Logic|Semantics]].

---
# References
- [[Mutual Left and Right Adjunctions]]
- [[Polynomial Rings]]
- [[Algebraic Closure]]
- [[Fields]]
- [[Zarisky Topology]]
- [[Adjunctions]]
- [[Adjunctions in Posets]]
- [[Galois Connection]]
- [[Semantics of First Order Logic]]
- [[Syntax of First Order Logic]]