---
tags:
  - Note
---
202505241605

Tags : [[Category Theory]]
# Fully Faithful Functors reflect Limits and Colimits
---
>[!theorem]
>Any fully faithful functors reflect any limits and colimits present in its domains.

Consider a diagram $K : J \to C$ and a fully faithful functor $F:C \to D$ such that the diagram $FK:J \to D$ has the limit $\mu:d \Rightarrow FK$ which is the image of the cone $\lambda:c \Rightarrow K$. We need to show that $c$ is a limit cone.

Consider any cone over $\lambda' : c' \Rightarrow K$, the functor takes it to the cone $\mu':d' \Rightarrow FK$. But the universality of $\mu$ states that there is a unique morphism $g:d' \to d$ such that the cone factors though the limit cone.
But fully faithfulness of $F$ tells us that the $g$ is of the form $Ff$ which will be the unique morphisms that makes $\lambda'$ factor through $\lambda$. Hence $\lambda$ is a limit cone. If this is not unique, then it can pushed down to $D$ to show that $g$ was not unique either.

Colimits are also reflected by duality.

---
# References
- [[Limits and Colimits]]
- [[Preservation, Reflection and Creation of Limits]]
- [[Equivalence of Categories]]
- [[Equivalences Reflect, Preserve and Create Colimits]]