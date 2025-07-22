---
tags:
  - Note
---
202507191707

Tags : [[Category Theory]]
# A complete, locally small category with a jointly weakly initial set of objects has an initial object
---
>[!theorem]
>If a category $C$ is [[Small Categories|locally small]], [[Complete and Cocomplete Categories|complete]] and has a [[Weakly initial objects and joint weakly initial sets|jointly weakly initial]] set of obejcts $\Phi$, then $c$ has an [[Initial, Terminal and Zero Objects|initial object]].

Consider the limit $l$ of the inclusion of the full subcategory spanned by the objects of $\Phi$. Since $C$ is locally small, this diagram is small, and the limit exists because $C$ is complete.

It is fairly obvious that $l$ is [[Weakly initial objects and joint weakly initial sets|weakly initial]]. To show that it is inital, we need to define a cone $\lambda:l\to{1}_{C}$ with the property that the component $\lambda_{l}$ is the identity morphism. And we will be done by [[Identity Functor admits a limit iff there is an initial object]].

To prove that the maps $\lambda_{c}$ defines a cone, consider any morphism $f:c\to c'$ in $C$. We have a morphism $h_{c}:k\to c$ for some $k\in \Phi$ and we have a morphism $h_{c'}:k'\to c'$ for some $k'\in \Phi$, now consider $p$ which is the pull back of $h_{c'}$ and $f\circ h_{c}$. But we also have a map $k''\to p$ where $k''\in \Phi$ as depicted below.
![[Pasted image 20250719172334.png|300]]

We have that the dashed arrows also belong to the full subcategory of $C$ spanned by $\Phi$, so the top triangles commute. These are legs of $\kappa$, which was teh cone used to define $l$. We will now define $\lambda$ to be $\kappa$ wherever and the commutativity of the rest of the diagram proves that $\lambda$ forms a limit cone.

We now have that the following diagram commutes for all $k\in \Phi$:
![[Pasted image 20250719173049.png|250]]

This tells us that $\lambda_{l}$ defines a factorization of the limits cone though itself, thus $\lambda_{l}=1_{l}$.


---
# References
- [[Small Categories]]
- [[Complete and Cocomplete Categories]]
- [[Weakly initial objects and joint weakly initial sets]]
- [[Initial, Terminal and Zero Objects]]
- [[Equivalence of Categories]]
- [[Identity Functor admits a limit iff there is an initial object]]
- [[Limits and Colimits]]