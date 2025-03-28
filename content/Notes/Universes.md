---
tags:
  - Note
---
202503220703

Tags : [[Homotopy Type Theory]]
# Universes
---
>[!definition]
>Universes are types whose elements are types, usually represented by $\cal U$.

To avoid the pitfalls of naive set theory, we do not allow there to be a universe $\mathcal U_{\infty}$ that contains all types including itself. To deal with that, we have a universe of types which are not themselves universes called $\cal U_{0}$ and from that we construct a hierarchy of universes. 
$$
\mathcal U_{0} :\mathcal U_{1}:\mathcal U_{2}: \cdots
$$
We also assume that universes are cumulative, so if $A : \mathcal U_{i}$ then $A : \mathcal U_{i+1}$. This is convenient in a lot of places but we do get that an element does not have a unique type.

We will mostly write statements like $A:\mathcal U$, we justify this by saying that it is usually possible to index $\mathcal U$ in a consistent way. 

This is how Bertrand Russel originally defined type theory, as a set theory that avoids Russel's paradox.

>[!definition]
>Given a [[Universes|Universe]] $\cal U$, to model a collection of types inside $\mathcal U$ over some type $A$, we define a function $f:A \to \mathcal U$. Such a function is called a **family of types**.

^ea1d66

---
# References
