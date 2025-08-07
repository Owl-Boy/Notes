---
tags:
  - Note
---
202507261307

Tags : [[Homotopy Type Theory]]
# Quotient map is surjective
---
>[!theorem]
>The function $q:A \to A / R$ which is the [[Set Quotient|quotient]] map is [[Surjections and Embeddings|surjective]].

To prove this, we need to show that for any $x:A /R$, there must exists an $a:A$ such that $q(a)=x$. We use the induction principle of $A /R$. 
- If $x\equiv q(a)$ then we are done, we just return $a$.
Since the goal is a mere proposition, it already respects path constructors so we are done.

---
# References
- [[Set Quotient]]
- [[Surjections and Embeddings]]