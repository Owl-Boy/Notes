---
tags:
  - Note
---
202507210007

Tags : [[Category Theory]]
# A locally small, complete category with a small coseparator and intersections of all collections of subobjects has an initial object
---
>[!theorem]
>Let $C$ be a locally small, complete category which has a small coseparator $\Phi$, and the property that every collection of subobjects has an intersection. Then $C$ has an initial object.

We will show that the following object will be the initial object:
- Consider the coseparator $\Phi$
- Let $p$ be its product.
- Let $i$ be the intersection of subobjects of $p$

We claim that $i$ is the initial object in $C$.

Stating that $\Phi$ is the coseparator is the same as stating that the canonical map
$$
c\rightarrowtail \prod_{k\in \Phi}k^{C(c, k)}
$$
is a monomorphism.
The codomain takes each object $k$ from $\Phi$ and makes as many copies of it as there are maps in $C(c, k)$. There is also a map $\prod_{k\in \Phi}\to \prod_{k\in \Phi}k^{C(c, k)}$, whcis is the product over $k\in \Phi$ of the maps $\Delta$ defined to be the identity on each component.

Now consider the pullback:
![[Pasted image 20250721012150.png|350]]
which defines a sub-object $p_{c}$ of $p$. This we have a map $i \to p_{c} \to c$ from the intersection to $c$. This arrow must be unique because if there were 2 arrows, then there would be 2 arrows because the equalizer of these 2 arrows woudl be a smaller sub-object of $p$. This $i$ is initial.

---
# References
- [[Subobjects]]
- [[Separating and Coseparating sets]]
- [[Equalizers and Coequalizers]]
- [[Complete and Cocomplete Categories]]
- [[Small Categories]]