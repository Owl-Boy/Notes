---
tags:
  - Note
---
202505101205

Tags : [[Category Theory]]
# Universal Property 
---
>[!definition]
>A **Universal Property** of an element $c:C$ is expressed by a [[Representable Functors|Representable Functor]] $F$ together with a **Universal Element** $x \in Fc$ which defines the [[Natural Transformation|Natural Isomorphism]] $C(c, -) \cong F$ or $C(-, c) \cong F$ according to the [[Yoneda Lemma]].

This definition seems fairly complicated as compared to [[Universal Property (Mac Lane)|this one]]. So to unpack the definition. 
Lets also call $c$ to be the **Universal Object**.
For any representable functor $F$ we have an essentially unique object, $c$ such that $C(c, -) \cong F$. At the same time the [[Yoneda Lemma]], tells us that the collection of [[Natural Transformation]]s $C(c, -) \cong F$ are in bijection with the set $Fc$. 

Thus there must be one element $x\in Fc$ such that the isomorphism given by the Yoneda Lemma maps to it. We call that element the **Universal Element** and we call $F$ along with $x$ the **Universal Property**.

>[!example]
>Consider the forgetful functor $U: \text{Ring} \to \text{Set}$ which is represented by $\mathbb{Z}[x]$. The universal element which defines the natural isomorphism
>$$
>\text{Ring}(\mathbb{Z}[x], R) \cong UR
>$$
>is $x\in \mathbb{Z}[x]$. The bijection is to evaluate a ring homorphism $\phi: \mathbb{Z}[x] \to R$ at $x$.

---
# References
- [[Representable Functors]]
- [[Natural Transformation]]
- [[Yoneda Lemma]]
- [[Universal Property (Mac Lane)]]
- [[Equivalence of Definitions of Universal Property]]
- [[Limits and Colimits]]
- [[Element Category]]