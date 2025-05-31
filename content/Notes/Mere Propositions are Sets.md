---
tags:
  - Note
---
202505171805

Tags : [[Homotopy Type Theory]]
# Mere Propositions are Sets
---
>[!theorem]
>Every [[Mere Propositions|mere proposition]] is a [[Sets in Type Theory|set]].

Suppose $f:\text{is-Prop}(A)$, then for all $x, y:A$ we have $f(x,y):x=y$. Fixing $x$ we get $g(y):\equiv f(x, y)$. Then for $y,z:A$ and $p:y=z$ we have $\text{apd}_{g}(p): p_{*}(g(y))=g(z)$ and by [[Higher Groupoid Structure of Identity Types]] we get $g(y)\cdot p=g(z)$, that is $p=g(y)^{-1}\cdot g(z)$, hence any path between $y$ and $z$ must be equal.

---

This has the following interesting corollary:
>[!theorem]
>$\text{is-Prop}$ and $\text{is-Set}$ are mere propositions.

Consider $f, g:\text{is-Prop}(A)$, we will show $f=g$ by function extensionality. By the previous lemma, after fixing $x, y$ we get $f(x, y)= g(x, y)$ because of the previous proposition, hence it is also a set.

Consider $f, g: \text{is-Set}(A)$, which says, forall $x, y:A$ and $p,q:x=y$ we have $f(a,b,p,q):p=q$ and $g(a,b,p,q):p=q$. But since $A$ is a set, we have $x=y$ is a set, hence $f(a,b,p,q)=g(a,b,p,q)$, and thus by function extensionality we have $f=g$.



---
# References
- [[Mere Propositions]]
- [[Sets in Type Theory]]
- [[Identity Type]]