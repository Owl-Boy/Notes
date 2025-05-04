---
tags:
  - Note
  - Incomplete
---
202505031405

Tags : [[Homotopy Type Theory]]
# Functions as Functors
---
After seeing that [[Types are Higher Groupoids]], we now want to make sure that morphisms between these behave as functors, or with a topological interpretation, functions are continuous.

>[!lemma]
>let $f:A \to B$ be a function, then for any $x, y:A$ we have the operation:
>$$
>\text{ap}_{f}: (x=_{A}y) \to (f(x) =_{B}f(y))
>$$
>And for each $x$ we have $\text{ap}_{f}(\text{refl}_{x})\equiv \text{refl}_{f(x)}$

The notion of $\text{ap}$ is the same as application, it lifts the equality to the range of the function.

Proving it is fairly straightforward, let $p$ be the path that connects $x$ and $y$, then we do path induction on $p$, and we can define $\text{refl}_{f(x)}$ as the output.

And we now prove that $\text{ap}_{f}$ behaves like a functor.
>[!lemma]
>For functions $f:A \to B$ and $g:B \to C$ and paths $p:x=_{A}y$ and $q: y=_{A}z$ we have:
>- $\text{ap}_{f}(p \cdot q) =_{B} \text{ap}_{f}(p)\cdot \text{ap}_{f}(q)$.
>- $\text{ap}_{f}(p^{-1}) = \text{ap}_{f}(p)^{-1}$
>- $\text{ap}_{g}(\text{ap}_{f}(p)) = \text{ap}_{g \circ f}(p)$
>- $\text{ap}_{\text{id}_{A}}(p)=p$

---
# References
