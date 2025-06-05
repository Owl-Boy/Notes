---
tags:
  - Note
  - Incomplete
---
202506011706

Tags : [[Category Theory]]
# Representation of Limits as Limits in the Category of Sets
---
>[!theorem]
>Let $C$ be a locally small category then:
>- Covariant functor $C(X, -)$ preserves all limits that exist in $C$.
>- The covariant yoneda embedding $y: C\hookrightarrow\text{Set}^{C^\text{op}}$ both preserves and reflects limits. That is, a cone over a diagram in $C$ is a limit iff its image under the yoneda map is a limit.

### Covariant Interpretation
By [[Representable Universal Property of Limits]], we get that any composite diagram of the form
$$
J \xrightarrow{\quad F\quad}C\xrightarrow{\;C(X, -)\;}\text{Set}
$$
such that isomorphism of the above diagram commutes with the following diagram:
![[Pasted image 20250601162903.png|500]]

The component of the left map are the legs of the limit cone in $C$ of the diagram. The components of the right diagonal is the legs of the limit cone of $F$ under the functor $C(X, -)$.

## Contravariant Interpretation
Consider the contravariant functor $C(-, \text{lim}\ F)$ represented by the limit of $F:J\to C$. When this is considered as an object of $\text{Set}^{C^\text{op}}$ is the limit of the diagram
$$
J \xrightarrow{ F}C\xhookrightarrow{ y } \text{Set}^{C^\text{op}}
$$
whose objects are representable functors  $C(-,Fj)$. Thus the Yoneda embedding preserves all limits. But it also reflects all limits as [[Fully Faithful Functors Reflect Limits and Colimits]].

---
By Duality, we also get the following
>[!theorem]
>Let $C$ be a locally small category then:
>- Contravariant functor $C(-, X)$ preserves all colimits that exist in $C$.
>- The contravariant yoneda embedding $y: C^\text{op}\hookrightarrow\text{Set}^{C}$ both preserves and reflects limits. That is, a cone under a diagram in $C$ is a colimit iff its image under the yoneda map is a limit.

---
# References