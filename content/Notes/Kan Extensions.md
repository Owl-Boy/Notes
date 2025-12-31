---
id: Kan Extensions
aliases:
  - Kan Extensions
tags:
  - Note
---
202512291308

Tags : [[Category Theory]]
# Kan Extensions
---
> [!DEF] 
> Given Functors $F:C \to E$, $K:C\to D$, a **left Kan extension** of $F$ along $K$ is a functor $\text{Lan}_K F  :D\to E$ together with a natural transformation $\eta : F \Rightarrow (K;\text{Lan}_K F)$ such that for any other such pair $G: D\to E, \gamma: F\Rightarrow (K;G)$, $\gamma$ factors uniquely through $\eta$.
>
> Dually, a **right Kan extension** of $F$ along $K$ is a functor $\text{Ran}_K F :D \to E$ together with a natural transformation $\epsilon:(K;\text{Ran}_K F) \Rightarrow F$ such that all such all natural transformations from similar pairs factor through $\epsilon$.

In simpler words, given the categories $C, D, E$ and functors $F:C\to E$ and $K:C \to D$, consider the category of functors of type $G:D\to E$ such that there is a natural transformation $F \Rightarrow (K;G)$. The left kan extensions is the initial object of this category. 

If we consider the natural transformation $(K;G)\Rightarrow F$, then the terminal object of that category is the right kan-extension.

![Left_kan_extension.png](Attachments/Left_kan_extension.png)

---
# References

- [[Examples of Kan Extensions]]
- [[Functors]]
- [[Natural Transformation|natural Transformation]]\

