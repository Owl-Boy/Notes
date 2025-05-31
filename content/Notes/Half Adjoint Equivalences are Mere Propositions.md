---
tags:
  - Note
---
202505231605

Tags : [[Homotopy Type Theory]]
# Half Adjoint Equivalences are Mere Propositions
---
>[!lemma]
>If $f$ is a half adjoint equivalence, then for any $(g, \epsilon):\text{rinv}(f)$, the type $\text{rcoh}_{f}(g, e)$ is contractible

by the lemma in [[Coherence Types for Equivalences]], and the fact that dependent function types preserve contractible spaces, it suffices to show that for each $a:A$, the type $(gfx, \epsilon(fx))=_{\text{fib}_{f}(fx)}(x, \text{refl}_{fx})$ is contractible.

But $\text{fib}_{f}(fx)$ is contractible as $f$ is a half-adjoint equivalence, so its path space is also contractible.

---
>[!theorem]
>For any $f:A\to B$ the type $\text{ishae}(f)$ is a mere proposition.

We show that $\text{ishae}(f) \to \text{is-Contr}(\text{ishae}(f))$ is inhabited. So assume $f$ be to be a half-adjoint equivalence and we will show that $\text{ishae}(f)$ is contractible.
We now get that the type $\text{ishae}(f)$ is equivalent to
$$
\sum_{u:\text{rinv}(f)} \text{rcoh}_{f}(\text{pr}_{1}(u), \text{pr}_{2}(u))
$$
But since $\text{rinv}(f)$ is contractible due to [[Left and Right Inverses#^1c1929|this lemma]] and for each $u$, the previous lemma gives that the specified type is contractible.


---
# References
- [[Functions as Equivalences]]
- [[Half Adjoint Equivalences]]
- [[Coherence Types for Equivalences]]
- [[Left and Right Inverses]]
