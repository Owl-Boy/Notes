---
tags:
  - Note
---
202505300005

Tags : [[Homotopy Type Theory]]
# Functions types to isomorphic types are isomorphic
---
>[!lemma]
>Let $A, B, X:\cal U$ such that $A \simeq B$, then 
>$$
>(X \to A) \simeq (X \to B)
>$$

The proof is simple, consider $e:A\simeq B$, we can think of $e = \text{idtoeqv}(p)$ for some $p:A\to B$. Then we induct on $p$, so we get $X\to A \simeq X\to A$, whose equivalence is witnessed by identity.

---

>[!lemma] Corollary
>Let $P:A \to\cal U$ be a family of contractible types, then there is an equivalence
>$$
>\alpha:\left( A \to \sum_{x:A}P(x) \right) \simeq (A \to A)
>$$ 

We have,  $\text{pr}_{1}: \sum_{x:A}P(x) \to A$ and $x$ give us an equivalence $\text{fib}_{\text{pr}_{1}}(x) \simeq P(x)$ so $\text{pr}_{1}(x)$ is an equivalence when it is contractible. Now from the previous lemma its direct.

---
# References
- [[Weak Function Extensionality]]
- [[Univalence Implies Weak Function Extensionality]]
- [[Contractible Types]]
