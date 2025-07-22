---
tags:
  - Note
---
202506071606

Tags : [[Category Theory]]
# Any category with Pullback and a terminal object has all finite limits, with pushouts and an initial object has all finite colimits
---
>[!theorem]
>Any category with all pullbacks and a terminal object has finite limits.

>[!lemma]
>In any category with terminal object $1$, the following pullback defines the product.
>![[Pasted image 20250607161504.png|250]]

The proof is trivial.

>[!lemma]
>In any category with binary products, the following pullback defines an equalizer:
>![[Pasted image 20250607161707.png]]

The universal property of product states that
$$
\text{Hom}(E, B\times B) \cong \text{Hom}(E, B) \times \text{Hom}(E, B)
$$
and of the pullback is 
![[Pasted image 20250607162143.png|500]]

And since in the category of sets, we get [[Limits in the Category of Sets#^d39f53]]. Composition with $e$ and $l$ defines a isomorphism between $X$-shaped generalized elements of $E$ and pairs of generalized elements $(X \xrightarrow aA, X\xrightarrow b B)$ so that $fa = b = ga$. This composing with $e_{*}$ defines an isomorphism between elements of $\text{Hom}(X, E)$ and the subset of $\text{Hom}(X, A)$ consisting of those generalized elements $a$ such that $fa=ga$  and by [[Limits in the Category of Sets#^6d3859]] we get 
$$
\text{Hom}(X, E) \overset {e_{*}}\rightarrowtail \text{Hom}(X, A) \underset{f_{*}}{\overset{g_{*}}{\rightrightarrows}} \text{Hom}(X, B)
$$
which is an equalizer diagram and we are done.


---
>[!theorem]
>Dually, Any category with all pushouts and an initial object has finite colimits.

---
# References
- [[Limits in the Category of Sets]]
- [[Any Category with Coproducts and Coequalizers is Cocomplete, with Products and Equalizers is Complete]]