---
tags:
  - Note
---
202508311808

Tags : [[Homotopy Type Theory]]
# Truncations as a Reflective subcategory
---
>[!lemma]
>$n$-truncations are functorial.

This is straightforward from [[Universal Property of Truncations]].

- Given types $A:\cal U$, there is a type $\|A\|_{n}:\cal U$ 
- Given a function $f:A\to B$ there is a function $\|f\|_{n}:\|A\|_{n}\to\|B\|_{n}$ by first post compsing with $|-|_{n}$ and then using [[Universal Property of Truncations]]., There is also the homotopy:
  $$\text{nat}_{n}^f:\prod \|f\|_{n}(|a|_{n})=|f(a)|_{n}
  $$
 expresses naturality.

>[!theorem]
>Given $f, g:A\to B$ and a homotopy $h:f\sim g$, there is an induced homotopy $\|h\|_{n}:\|f\|_{n} \sim \|g\|_{n}$  such that the composite 
>$$
>|f(a)|_{n}\overset{\text{nat}_{n}^f(a)^{-1}}= \|f\|_{n}(|a|)_{n}\overset{\|h\|_{n}(|a|_{n})}= \|g\|_{n}(|a|_{n}) \overset{\text{nat}_{n}^g(a)}= |g(a)|_n 
>$$
>is equal to $\text{ap}_{|-|_{n}}(h(a))$.

We have $\text{ap}_{|-|_{n}}(h(a)):|f(a)|_{n}=|g(a)|_{n}$, and we can obtain a homotopy $(\|f\|_{n}\circ |-|_{n})\sim (\|f\|_{n}\circ |-|_{n})$ and since $(-\circ|-|_{n})$ is an equivalence, there must be a path inducing $\|f\|_{n}=\|g\|_{n}$ inducing it, and coherence laws for functional extensionality imply the theorem.

>[!Lemma] Corollary
>A type $A$ is an $n$-type iff $|-|_{n}:A\to\|A\|_{n}$ is an equivalence.

Left to right follows from closure of $n$-types under equivalence. On the other hand if $A$ is an $n$-type, we can define $\text{ext}(\text{id}_{A}):\|A\|_{n}\to A$. Then $\text{ext}(\text{id}_{A})\circ |-|_{n}=\text{id}_{A}$ by definition. we need to show $|-|_{n}\circ\text{ext}(\text{id}_{A})\circ |-|_{n}=\text{id}_{\|A\|_{n}}\circ |-|_{n}$.
![[Pasted image 20250831192235.png]]

---
# References
- [[Reflective Subcategory]]
- [[Universal Property of Truncations]]
- [[Truncation]]