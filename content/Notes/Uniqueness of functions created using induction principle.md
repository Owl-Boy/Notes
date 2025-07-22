---
tags:
  - Note
---
202506161506

Tags : [[Homotopy Type Theory]]
# Uniqueness of functions created using induction principle
---
The induction principle is strong enough to prove its own uniqueness.

>[!lemma]
>Let $f, g:\prod_{x:\mathbb{N}} E(x)$ be two function which satisfy the recurrences
>$$
>e_{z}: E(0) \quad \text{and} \quad e_{s}: \prod_{k:\mathbb{N}}E(k) \to E(\text{suc }k) 
>$$
>up to propositional equality, that is:
>$$
>f(0) = e_{z} = g(0)
>$$
>and 
>$$
>\begin{align}
>\prod_{k:\mathbb{N}} f(\text{suc }k) = e_{s}(k, f(k))\\
>\prod_{k:\mathbb{N}} g(\text{suc }k) = e_{s}(k, g(k))
>\end{align}
>$$
>then $f=g$.

We do induction on the type family $D(x):\equiv f(x)=g(x)$, for the base case we have 
$$
f(0)=e_{z}=g(0)
$$
For the inductive case, assume $n:\mathbb{N}$ such that $f(n)=g(n)$, then 
$$
f(\text{suc } n)=e_{s}(n, f(n))=e_{s}(n, g(n)) = g(\text{suc }n) 
$$
Now we invoke function extensionality.

The same proof can be redone for all inductive types, me thinks.


---
# References
- [[Inductive Types]]
- [[Similar description of inductive types lead to equal types]]
- [[Natural Numbers in Type Theory]]