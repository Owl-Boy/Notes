---
tags:
  - Note
---
202505252105

Tags : [[Homotopy Type Theory]]
# Surjections and Embeddings
---
>[!definition]
>We say that a function $f$ is **surjective** (or is a **surjection**) if the type $\|\text{fib}_{f}(b)\|$ is inhabited for all $b:B$.

This definition is very similar to the set theory definition of a surjection, and a simple types as proposition conversion would give: 
$$
\forall (b: B), \exists (a:A), f(a)=b
$$
holds.

similarly we have a similar notion of an injection given by:
>[!definition]
>We say $f:A\to B$ is an embedding if for every $x, y:A$, the function $\text{ap}_{f}:(x=_{A}y) \to (fx =_{B} fy)$ is an equivalence.

translating this directly leads to the statement, given 2 elements $x, y:A$ and elements $f(x), f(y):B$, then, if $f(x)=f(y)$ then $x=y$.

---
# References
- [[Mere Propositions]]
- [[Sets in Type Theory]]
- [[Identity Type]]