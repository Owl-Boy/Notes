---
id: Examples of Kan Extensions
aliases:
  - Examples of Kan Extensions
tags:
  - Example
---

202512291338

tags : [[Category Theory]]

#  Examples of Kan Extensions
---

> [!EXAMPLE] Yoneda Lemma
> The [[Yoneda Lemma]] says that for any $a\in A$, the [[Representable Functors|representable functor]] $A(a,-)$ is a left Kan extension of the terminal object $\mathbb 1 \to \text{Set}$ along $a:\mathbb 1\to A$.

> [!EXAMPLE]
> Consider the case where the function $F$ factors through $K$ along $H$. Then it is not ncessarily the case that $(H, 1_F)$ is the left Kan extension of $F$ along $H$. To demonstrate this, consider the case where $C=*$ and $D=E = *\to*$.
>
> If we take $H$ to also be the terminal object functor, then $F$ factorizes and we have $\text{id}_F$ as the witness natural transformation.
>
> This is not the left Kan extension, that would be when $H$ is the identity functor. 

> [!EXAMPLE]
> Consider the partial order on $\mathbb Q$ of rationals and $\mathbb R_{>0}$. We have a functor $2^{-}:\mathbb Q \to \mathbb R_{>0}$. If we extend the target to be $\bar R_{>=0}$ then it becomes a complete and cocomplete poset. Thus we get a left (and right) kan extension along $\mathbb Q\hookrightarrow \mathbb R$. In this case its the exponential function $2^-: \mathbb R\to\mathbb R_{>0}$

---
# Related
- [[Kan Extensions]]
- [[Construction of Kan Extensions]]
- [[Yoneda Lemma]]
- [[Representable Functors]]


