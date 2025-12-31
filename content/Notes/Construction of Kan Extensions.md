---
id: Construction of Kan Extensions
aliases:
  - Construction of Kan Extensions
tags:
  - Note
---
202512301636

Tags : [[Category Theory]]
# Construction of Kan Extensions
---
The [[Kan Extensions]] of a functor is supposed to be an approximation of an extension. The left and right ones being the two closest from different directions and the closeness is described by the [[Universal Property (Riehl)|Universal Property]] of the Kan Extension.

Thus, consider categories $C,D$ and $E$ with functors $F:C\to E$ and $K:C\to D$. To define the extension $\text{Lan}_K F$, for each object $d:D$ we need to give a map. To make this functorial, we see the collection of objects in $C$ such that any $c$ from that has a map to $d$, that is $\exists m:Kc\to d$. Then the image of $d$ under $\text{Lan}_K F$ should have a map from $Fc$. This also needs to preserve some more structure than just having a map from every such $c$.
- Restrict the category $C$ to the set of objects that map to $d$. We want the image of $d$ under $\text{Lan}_K F$ to be the colimit of image of the diagram under $F$.

It is necessary for defining the [[Natural Transformation]] for this property to hold for every $d$.

The image of morphisms and the natural transformation is also direct from this construction:
- If there is a morphism $f:d\to d'$, then note that for any object $c$, if there is a map $Kc\to d$, then there is a map $Kc\to d'$ which we get by post-composing with $f$. One can find a canonical map in the category $E$ by the universal property of colimits.
- The maps of the cones are precisely going to be the data of the natural transformations.

> [!THM]
>
> Given categories $C,D,E$ and functors $F:C\to E$ and $K:C\to D$, if for very object $d:D$, we consider the comma category $K\downarrow d$.
>
> Let $\Pi_K^d:K\downarrow d \to C$ be the canonical projection map.
>
> If the colimit of the following diagram always exists : $(K\downarrow d) \mid\vartriangleright \Pi_K^d \vartriangleright F$
>
> Then we can define the left kan extension at $d$ to be the above colimit. The morphisms and the natural transformations can be extracted from the colimit information.

Moreover, if we have that $K$ is fully faithful and that $E$ is complete (or cocomplete) then the counit (unit) defines a natural isomorphism $K\vartriangleright\text{Ran}_K F\cong F$ ($F\cong K\vartriangeright\text{Lan}_K F$).

This is because during the construction, for each $c$, the category $K\downarrow Kc$ is isomorphic to $C\downarrow c$ and hence has a terminal object, which will correspond to $c$ itself, thus the image of $Kc$ under the kan extension is isomorphic to $Fc$. 

---
# References

- [[Kan Extensions|kan Extensions]]
- [[Limits and Colimits]]
- [[Universal Property (Riehl)|Universal Property]]
- [[Natural Transformation]]
- [[Fully Faithful Functors Reflect Limits and Colimits]]
