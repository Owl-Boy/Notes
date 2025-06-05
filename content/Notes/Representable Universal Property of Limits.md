---
tags:
  - Note
---
202506011506

Tags : [[Category Theory]]
# Representable Universal Property of Limits

---
Consider a small diagram $F:J\to C$ and the functor composite functor:
$$
C(X, F-) :\equiv J \xrightarrow{\quad F\quad}C \xrightarrow{\;C(X, -)\;} \text{Set}
$$
which is a diagram of shape $J$ in $\text{Set}$, but since [[Set is Complete]], a limit exists, and [[Small Limits in Set are Equalizers]], we have a way to construct it. An element in the set $\text{lim}_{J} C(X, F-)$ is an element of the product $\prod_{j:J}C(X, Fj)$, that is a tuple of morphisms $\lambda_{j}:X\to Fj$ subject to the condition that the following diagram commutes for each:
![[Pasted image 20250601154938.png|200]]

thus an element of $\text{lim}_{J}C(X,F-)$ is precisely the cone over $F$, hence
$$
\text{lim}_{J}C(X, F) \simeq \text{Cone}(X, F)
$$
This is isomorphism in natural in $X$, and since the limit of $F$ is defined as the limit cone $\text{Cone}(-, F)$, we can say that:
>[!theorem]
>For any diagram $J$ whose limit exists, there is a natural isomorphism:
>$$
>C(X, \text{lim}_{J}F) \cong \text{lim}_{J}C(X, F)
>$$ 

A Corollary for this is : [[Covariant Representable Functors from a locally small category to Set preserve all limits]]


---
# References
