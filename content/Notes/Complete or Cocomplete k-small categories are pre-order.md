---
tags:
  - Note
---
202506141306

Tags : [[Category Theory]]
# Complete or Cocomplete $\kappa$-small categories are pre-order
---
>[!theorem]
>Any $\kappa$-small category that admits all $\kappa$-small limits, or that admits all $\kappa$-small colimits is a [[Preorder]].

Let $\lambda$ be the set of morphisms in a $\kappa$-small category $C$. We need to show that for any pair of parallel morphisms $f,g:B\rightrightarrows A$, they are identical, that is $f=g$. 

Consider the case when all $\kappa$-small limits exists. Then consider the exponent $A^\lambda$, we know from [[Examples of Representable Universal Property of Colimits]]. There are $2^\lambda$ distinct morphisms from $B\to A^\lambda$ where components are either $f$ or $g$. But that would contradict the cardinality $C$. Hence $f=g$.

Taking $\lambda$ many co-products of $B$ and doing the same gives the dual part of the proof.

---
# References
- [[Complete and Cocomplete Categories]]
- [[Preorder]]
- [[Cardinality of a small category]]
- [[Examples of Representable Universal Property of Colimits]]