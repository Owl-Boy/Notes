---
tags:
  - Note
  - Incomplete
---
202505151405

Tags : [[Category Theory]]
# Limits and Colimits
---
>[!definition] Limits and Colimits 1
>For any diagram $F:J \to C$, there is a functor
>$$
>\text{Cone}(-,F): C^\text{op} \to \text{Set}
>$$
>that sends $c$ to the *set* of cones over $F$ with the summit $c$. A limit of $\text{Cone}(-, F)$ is an object $\lim F$ and the *limit cone* defining the natural isomorphism 
>$$
>\text{Cone}(-, F) \cong \text{Hom}_{C}(-, \lim F)
>$$
>Dually, we can define the functor
>$$
>\text{Cone}(F, -): C \to \text{Set}
>$$
>That sends the $c$ to the set of cocones under $F$ with nadir $c$. And the object representing this functor would give the *colimit cocone*.
>

One can also define limits and colimits as the terminal and initial object in the appropriate category of elements.

>[!definition] Limits and Colimits 2
>For may diagram $F: J \to C$, a **Limit** is a terminal obejct in the category of cones over $F$, which is the catgory $\int \text{Cone}(-, F)$. Where the morphisms look as follows:
>![[Pasted image 20250515145308.png]]
>An object here is a cone over $F$, with any summit. Here the forgetful functor, takes a cone to it summit.
>Dually, one can define a **Colimit** as the initial object in the category of cocones.

>[!definition]
>The data of a diagram, together with its limit or colimit is called the **Limit Diagram** or the **Colimit Diagram** respectively.
>
>A $J$ indexed diagram with a cone over it can be combined to define a diagram indexed by $J^\triangleleft$, which has $J$ as a full subcategory with a freely adjointed initial object. Dually a diagram indexed by $J$ along with a cocone can be defined as a diagram indexed by $J^\triangleright$ which has $J$ as a full subcategory along with a freely adjoined terminal object.

---
# References
