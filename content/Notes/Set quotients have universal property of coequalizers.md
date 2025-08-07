---
tags:
  - Note
---
202507261307

Tags : [[Homotopy Type Theory]]
# Set quotients have universal property of coequalizers
---
>[!theorem]
>For any set $B$, precomposing with $q$ yields an equivalence:
>$$
>(A /R \to B) \simeq \left( \sum_{(f:A\to B)}\prod_{(a,b:A)}R(a,b)\to (f(a) = f(b)) \right)
>$$

The quasi inverse of $-\circ q$ which will be from right to left is just the recursion principle for $A /R$. This is the right inverse.

For the left inverse, we need to show that for any $g:A /R\to B$ and $x:A /R$ we have $g(x)=\overline{g \circ q}(x)$. But we have a mere existance of an $a$ such that $a=q(x)$ from [[Quotient map is surjective]]. Since our desired property is a [[Mere Propositions]], we may assume that there exists an $a$ such that $g(x)=g(q(a))=\overline{g\circ q}(q(a))=\overline{g\circ q}(x)$.

---
# References
- [[Set Quotient]]
- [[Mere Propositions]]
- [[Quotient map is surjective]]