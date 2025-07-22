---
tags:
  - Note
  - Incomplete
---
202506201606

Tags : [[Category Theory]]
# Closed Category
---
A category  $C$ is **closed**, if given any 2 objects $a, b:\cal C$ the collection  $\text{hom}(a, b)$ crates an object in the category $C$.

>[!example]
>The category $\text{Set}$ is **closed** because we can talk about the set of functions between two give sets.
>
>The category $\text{Ab}$ is **closed** because the homset can be given a pointwise addition structure, with the trivial map being the identity.

>[!definition]
>A **closed** category, is a category $C$ with the following data:
>- A functor $[-,-]: C^\text{op}\times C\to C$ called the internal hom functor.
>- An object $I$ called the *Unit*-object
>- A natural isomorphism $i:\text{id}_{c}\cong[I,-]$
>- A transformation $j_{X}:I\to[X,X]$ which is [[Extraordinary natural transformation|extranatural]] in $X$
>- A transformation $L_{Y\ Z}^X=[[X, Y], [X, Z]]$ which is [[Natural Transformation|natural]] in $Y$ and $Z$ and is [[Extraordinary natural transformation|extranatural]] in $X$.
>such that the following coherence diagram commute
>- ![[Pasted image 20250620163132.png|200]]
>- ![[Pasted image 20250620163151.png|200]]
>- ![[Pasted image 20250620163222.png|200]]
>- ![[Pasted image 20250620163238.png|500]]

---
# References
