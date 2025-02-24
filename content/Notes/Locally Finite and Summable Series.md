---
tags:
  - Note
  - Incomplete
---
202502121402

Tags : [[Weighted Automata and Transducers]]
# Locally Finite and Summable Series
---
>[!definition]
>We say that a family of series is __summable__ if $\exists f \forall \epsilon>0\exists I \subseteq_{\text{fin}} \mathbb{N} \forall J \supseteq I, J \subseteq_{\text{fin}}\mathbb{N}$ we have $d\left( f, \sum_{i\in J}f_{i} \right)<\epsilon$.
>
>We say that a sequence of series is **Locally finite** if $\forall w\in A^*$, the set $I_{w}=\{ i | <f_{i, w}> \neq 0 \}$ is finite

>[!todo] TODO : Find motivation for definition of summable

>[!lemma]
>For any sequence of series $f_{n}$ we have the following
>$$
>f_{n} \text{ is summable } \iff f_{n} \text{ is locally finite}
>$$

If a sequence of functions is locally finite then the sum is trivially defined, each component is the sum of finite number so it is easy to construct the function that witnesses the fact that the sequence is also summable.

---
>[!lemma]
>All proper series are locally finite, and hence also summable

A proper series is defined as followed:
Consider a function $f$ such that $f(\epsilon)=0$.
- $f^0= \mathbb 1$
- $f^1=f$
- $f^{l+1}=f^l f$
Since $f(\epsilon)=0$ we show $f^n(w)=0$ if $|w|<n$. Proof is by induction
**Base Case:** For $n=0$ the statement is trivially true.
**Induction Step:** Let $n=m+1$. Consider a word $w$ such that $|w|< m+1$. Let $w=w_{1}w_{2}$ such that $f^{m+1}(w)=f^m(w_{1})\cdot f(w_{2})$. Either $|w_{1}| < m$ or $|w_{2}|=0$ so we are done.


---
# References

