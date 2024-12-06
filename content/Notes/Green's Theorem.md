---
tags:
  - Note
  - Incomplete
---
202412020612

Tags : [[Algebraic Automata Theory]]
# Green's Theorem
---
>[!theorem] 
>Let $\cal M$ be a finite monoid and $e$ be an idempotent element of $\mathcal M$. Then $H(e)$ is a group.

By [[Location Lemma]], $H(e)$ is a [[Semi-Groups|semi-group]]. And for every element $s, t$ we have $ex = s$ and $ye = t$, so $se = s$ and $te = t$. So $H(e)$ forms a monoid with $e$ as its identity.

Also given an $s$ there are $s_{l}$ and $s_{r}$ such that $s_{l}s=e$ and $ss_{r}=e$ but they might not be in the monoid, but we have $t_{l}= es_{l}e$ in $J(e)$, and we can see that $t_{l} \leq_{l} e$ and $t_{l} \leq_{r} e$, therefore $t_{l}\in  H(e)$. So every element of the monoid has a left and right inverse, which means both are equal. and hence we have a group.

---
# References
