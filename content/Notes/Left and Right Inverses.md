---
tags:
  - Note
---
202505231805

Tags : [[Homotopy Type Theory]]
# Left and Right Inverses
---
>[!definition]
>Given a function $f:A\to B$, we define the types:
>$$
>\begin{align}
>\text{linv}(f) &:\equiv \sum_{g:B\to A} g \circ f \sim \text{id}_{A} \\
>\text{rinv}(f) &:\equiv \sum_{g:B \to A} \sim \text{id}_{B}
>\end{align}
>$$ 
>Which define the types of left and right inverses of a function.

----
>[!lemma]
>If $f:A \to B$ has a quasi-inverse, the so do
>$$
>\begin{align}
>(f \circ -) &: (C \to A) \to (C \to B) \\
>(- \circ f) &: (B \to C) \to (A \to C)
>\end{align}
>$$

If $g$ is a quasi-inverse of $f$ then $(g\circ-)$ is the quasi-inverse of $(f\circ -)$ and $(-\circ g)$ is the quasi-inverse of $(-\circ f)$.

---

>[!lemma]
>If $f:A \to B$ has a quasi inverse, then the types $\text{rinv}(f)$ and $\text{linv}(f)$ are contractible

^1c1929

By function extensionality we have 
$$
\text{linv}(f)\simeq \sum_{g:B\to A} (g\circ f = \text{id}_{A})
$$
But this is a fiber of $(-\circ f)$ over $\text{id}_{A}$ so it is contractible, same for $\text{rinv}$ being equivalent to the fiber of $(f \circ -)$ over $\text{id}_{B}$. Both of these are contractible by [[Fibers of Half Adjoint Equivalences are Contractible]].

---
# References
- [[Functions as Equivalences]]
- [[Half Adjoint Equivalences]]
- [[Mere Propositions]]
- [[Higher Groupoid Structure of Pi Type|Function Extensionality]]