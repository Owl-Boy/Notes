---
id: Monoidal Functor
aliases:
  - Monoidal Functor
tags:
  - Note
---
202512272305

Tags : [[Category Theory]]
# Monoidal Functor
---

Monoidal Functors are [[Functors|functors]] from one [[Monoidal Category]] to another, these preserve the monoidal structure of the category, that is, these functors come with natural transformations which satisfy some coherence axioms, and these can be divided into 3 types:

>[!Definition] 
> Let $(\mathcal C, \otimes, I_{\mathcal C})$ and $(\mathcal D, \bullet, I_{\mathcal D})$. A **lax monoidal functor** from the category $\mathcal C\to \mathcal D$ is a functor together with natural transformations:
> $$
> \phi_{A, B} : FA\bullet FB \to F(A\otimes B)
> $$
> which preserves the monoid product and 
> $$
> \phi : I_{\mathcal D} \to FI_{\mathcal C}
> $$
> 
> Along with the associativity and the identity property coherence maps.

These can be extended to form a **strong monoidal functor** by making all coherence maps invertible.

If these maps are made to be identities, then we call it a **strict monoidal functor**.

---
# References
- [[Monoidal Category]]
