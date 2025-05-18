---
tags:
  - Note
  - Incomplete
---
202505062205

Tags : [[Homotopy Type Theory]]
# Transports to a Family of Paths
---
First, lets consider the simple case
>[!lemma]
>For any $A$ and $a:A$ with $p:x_{1} = x_{2}$ we have 
>$$
>\begin{align}
>\text{transport}^{x \mapsto a=x}(p, q) &= q \cdot p \\
>\text{transport}^{x \mapsto x=a}(p, q) &= p^{-1} \cdot q\\ 
>\text{transport}^{x \mapsto x=x}(p, q) &= p^{-1} \cdot q \cdot p
>\end{align}
>$$

^fc445a

Proof is by path induction on $p$.

Now consider the following:
>[!Lemma]
>Let $B:A \to \cal U$ and $f,g:\prod_{(x:A)}B(x)$ with $p:a=a'$ and $q:f(a)=_{B(a)}g(a)$, then we have 
>$$
>\text{transport}^{x \mapsto f(x)=g(x)}(p, q) = (\text{apd}_{f}p)^{-1} \cdot p_{*}(q)  \cdot (\text{apd}_{g}p)
>$$

We have one final characterization:
>[!theorem]
>For $p:a=_{A}a'$ with $q: a=a$ and $r:a'=a'$
>$$
>(\text{transport}^{x \mapsto x=x}(p, q)=r) \simeq (q \cdot p = p \cdot r)
>$$

Proof is by path induction on $p$.

---
# References
