---
tags:
  - Note
  - Incomplete
---
202507111607

Tags : [[Category Theory]]
# Any Equivalence can be promoted to an Adjunction
---
>[!theorem]
>Any equivalence 
>$$
>C\underset{G}{\overset F \leftrightarrows} D \quad \eta:1_{C} \cong GF,\quad \epsilon:FG \cong 1_{D}
>$$
>can be promoted to an adjoint equivalence in which the natural isomorphisms satisfy the triangle identities by replacing either of the original specified natural iromosphisms by a new unit or counit.

We have 
$$
\gamma := G\xRightarrow{\eta G}GFG\xRightarrow{G\epsilon}G
$$
but this composite might not be identity. We need to redefine either $\epsilon$ or $\eta$ so as to absorb the isomorphism $\gamma^{-1}$.

Let $\epsilon':=\epsilon \cdot F\gamma^{-1}$. By naturality of $\eta$ the following diagram commutes:
![[Pasted image 20250711165952.png|350]]

proving one traingle identity $G\epsilon'\cdot \eta G=1_{G}$. By naturality of $\eta$ and $\epsilon'$ and by the first triangle identity, the following diagram commutes:
![[Pasted image 20250711170300.png|350]]
Proving $\epsilon'_{F}\cdot F{\eta}$ is an idempotent. By cancellation any idempotent isomorphism must be identity. Thus $\epsilon'_{F}\cdot F\eta=1$

---
For the other proof if $\eta:1_{C}\cong GF$ is one of the natural isomorphism defining the equivalence then the function
$$
D(Fc, d)\xrightarrow{G}C(GFc,Gd)\xrightarrow{(\eta)_{c}^*}C(c, Gd)
$$
defines a natural isomorphism for all $c$ and $d$. The first map is an isomorphism because $G$ is fully faithful and the second map is an isomorhism because $\eta_{c}$ is an isomorphism. Thus $F$ and $G$ define and adjunction with unit $\eta$.

---
# References
