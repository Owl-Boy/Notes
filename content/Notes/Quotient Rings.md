---
tags:
  - Note
  - Incomplete
---
202505191105

Tags : [[Ring Theory]]
# Quotient Rings
---
While defining quotients, we, as usual, have to put structure on the kernel that makes sure that the quotient map respects the ring-structure.

It must be an [[Ideals|ideal]] as discussed in the note. This makes sure that addition is consistent, as an ideal is also a normal subgroup of $(R,+)$.

Thus a nice idea is to consider the cosets of the ideal treat them as the elements of the quotients.

To see if it works, consider cosets $(a+I)$ and $(b+I)$
- We have $(a+I)+(b+I)=(a+b+I)$
- We have $(a+I)\cdot (b+I) = (ab + aI + bI + I^2)=(ab+I)$

Thus we can say $R /I$ is a quotient-ring of $R$ if $I$ is an ideal of $R$.

>[!theorem]
>Let $I$ be an ideal of $R$. Then every ring-homomorphism $\phi:R \to S$ such that $I \subseteq \text{ker}(\phi)$, there exists a unique homomorphism $\phi' :R / I \to S$ such that the following diagram commutes:
>![[Pasted image 20250519121922.png|300]]

---
# References
