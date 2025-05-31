---
tags:
  - Note
---
202505261205

Tags : [[Homotopy Type Theory]]
# Surjection and Embedding are equivalent to Equivalences
---
>[!theorem]
>A function $f:A \to B$ is an equivalent iff it is both a surjection and an equivalence.

If $f$ is an equivalence, then each fiber is contractible, hence $\|\text{fib}_{f}(b)\|$ is inhabited, hence $f$ is surjective. 

Now given that $f$ is is an equivalence, let $f^{-1}$ be its quasi inverse. We will then we claim that $\text{ap}_{f^{-1}}$ is the quasi inverse of $\text{ap}_{f}$. Consider $p:x=y$ and $(ap_{f^{-1}} \cdot ap_{f}) p:f^{-1}(f(x))=f^{-1}(f(y))$. But we have the homotopy between $f^{-1}(f(x))$ and $\text{id}(x)$, given by $\lambda p. \beta^{-1}(x) \cdot p \cdot \beta(y)$, a similar argument works the other way round.

Now given that $f$ is a surjection and an embedding, we need to show that it is an equivalence. 

Given $a:A$ we first construct $g:B \to A$ as follows: 
We show that given any $b:B$ the type $\sum_{x:A}f(x)=b$ is contractible. Since $f$ is a surjection, there merely exists an $a:A$ such that, $f(a)=b$, hence the above type is inhabited. To show that this is a mere proposition, consider $x,y:A$, and $p:f(x)=b$ and $q:f(y)=b$, we need to show that $p=q$.
We have $p \cdot q^{-1}$ which states that $f(x)=f(y)$ and since $f$ is an embedding we get $r:x=y$. so we just need to show $r_{*}(p)=q$, but we already ahve that $\text{ap}_{f}(r)=p  \cdot q^{-1}$, so we get both types are logically equivalent.

We also know that $\text{is-embedding}$ and $\text{is-surjection}$ are mere propositions, so we get that 
$$
\text{is-equiv} \simeq (\text{is-embedding} \times \text{is-surjection})
$$

---
# References
- [[Surjections and Embeddings]]
- [[Functions as Equivalences]]
- [[Identity Type]]
- [[Transport]]
