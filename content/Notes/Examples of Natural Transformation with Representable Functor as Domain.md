---
tags:
  - Note
  - Incomplete
---
202505052205

Tags : [[Category Theory]]
# Examples of Natural Transformation with Representable Functor as Domain
---
>[!example]
>Consider the ordinal category $\omega$. Whose elements are all finite ordinals and morphism are the $\leq$ relation.
>
>We first consider the functor $F:\omega \to \text{Set}$, that sends an element labelled $k$ to $F_{k}$, hence defining a sequence of sets $F_{n}$. This also gives a function $f_{n,n+1}$ between sets $F_{n} \to F_{n+1}$.
>
>Now consider the functor $\omega(k, -)$ that sends $i<k$ to the empty set and $i\geq k$ to some singleton set.
>
>We also have that there exits a natural transformation $\alpha:\omega(k, -) \to F$ given by the arrow $\alpha_{n}:\omega(k, n) \to F_{n}$ such that all the squares of the following diagram commute.
>
>![[Pasted image 20250505225022.png]]
>
>Now clearly, for $\alpha_{i<k}$ we have the function defined already to be the empty function. For $\alpha_{k}$ we can pick any element from $F_{k}$. But after that the choices are fixed because of $f_{k,k+1}$ and so on.

>[!example]
>Given a group $G$, consider the represented functor $\mathcal  G:\text{B}G \to \text{Set}$ and another functor $F:\text{B}G \to \text{Set}$ and a natural transformation $\phi:\mathcal G \to X$, both of which are left-$G$-sets. Since the category is a 1 object category, there is a unique component of the natural transformation $\phi: \mathcal G \to X$. To do so, given an element $g:\mathcal G$ we need to find an element $x:X = \phi(g)$, but note that $\phi(g \cdot h)=g \cdot \phi(h)$ and taking $h=e$ we get $\phi(g)=g \cdot \phi(e)$, hence our choices are again fixed after picking $e$.

---
# References
