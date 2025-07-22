---
tags:
  - Note
---
202505241505

Tags : [[Category Theory]]
# Preservation, Reflection and Creation of Limits
---
>[!definition]
>For any class of diagrams $K: J \to C$ and a functor $F:C \to D$, we say $F$:
>- **Preserves** limits if for any diagram $K$ and limit cone over $K$, the image of this cone defines the limit cone cover the composite diagram $FK:J \to D$.
>- **Reflects** limits if for any cone over the diagram $K$ whose image upon applying $F$ is a limit cone of $FK$, is a limit cone over $K$.
>- **Creates** those limits if whenever $FK$ has a limit in $D$, there is some limit cone that can be lifted to a limit cone over $K$, and $F$ reflects the limits in the class of diagrams.

>[!theorem]
>If $F:C \to D$ creates limits for a particular class of diagrams in $C$, and $D$ has limits of those diagrams, then $C$ admits those limits and $F$ preserves them.

Consider any diagram in $D$ which has a limit as per her example, so given any cone $FK$ which as a limit $\mu:d \Rightarrow FK$, hypothesis implies there is a limit of the cone $K$ which is $\lambda:c \Rightarrow K$ such that the image of $\lambda$ under $F$ is $\mu$. This shows that $C$ admits the class of limits.

To show that $F$ preserves limits, consider a cone $\lambda:c \Rightarrow K$. But since limits are unique up to isomorphism, $\lambda$ is isomorphic to the limit induced by $\mu :d \Rightarrow FK$, hence the image of $\lambda$ is isomorphic to $\mu$, hence it is also a limit.

---
# References
- [[Limits and Colimits]]
- [[Natural Transformation]]