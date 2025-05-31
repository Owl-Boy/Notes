---
tags:
  - Note
---
202505251705

Tags : [[Homotopy Type Theory]]
# Bi-invertible Maps
---
With [[Left and Right Inverses]] defined, one can put them together to get the following type:
$$
\text{biinv}(f) :\equiv \text{linv}(f) \times \text{rinv}(f)
$$
We have shown that $\text{biinv}(f) \to \text{qinv}(f)$ and $\text{qinv}(f)\to\text{biinv}(f)$ in [[Left and Right Inverses]], now we show the following.

>[!lemma]
>For any $f:A\to B$, the type $\text{biinv}(f)$ is a [[Mere Propositions|mere proposition]].

Suppose $f$ is bi-invertible, we will show that $\text{biinv}(f)$ is contractible. We have $\text{biinv}(f)\to\text{qinv}(f)$ and $\text{qinv}(f)\to\text{is-Contr}(\text{rinv}(f))$ similarly for $\text{linv}(f)$. Using those we can construct $\text{is-Contra}(\text{biinv}(f))$.

>[!lemma]
>$\text{biinv}(f)\simeq\text{ishae}(f)$

We first have maps on both sides, because both are logically equivalent to $\text{qinv}(f)$. But both are mere proposition, so we get an equivalence.

---
# References
- [[Functions as Equivalences]]
- [[Half Adjoint Equivalences]]
- [[Mere Propositions]]
- [[Left and Right Inverses]]