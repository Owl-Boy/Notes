---
tags:
  - Note
---
202506020206

Tags : [[Category Theory]]
# Representable Universal Property of Colimits
---
The Idea is very similar to [[Representable Universal Property of Limits]], and the plan is to use duality. For a functor $F :J \to C$ and $X:C$ we can define 
$$
C(F-, X) :\equiv J^\text{op} \xrightarrow{\quad F\quad }C^\text{op}\xrightarrow{\;C(-, X)\;} \text{Set}
$$
Again, we know that the limit exists and can be constructed as an equalizer. Hence elements of $\text{lim}_{J}C(F-, X)$ are elements of $\prod_{j\in J}C(Fj, X)$, such that the following diagram commutes
![[Pasted image 20250602023922.png|200]]
thus we have $\text{lim}_{J}C(F-, X)$ thus we have the theorem
>[!theorem]
>For any diagram $J$ whose colimit exists, there is a natural isomorphism 
>$$
>C(\text{colim}_{J}F, X) \simeq \text{lim}_{J^\text{op}}C(F-, X)
>$$


---
# References
- [[Representable Universal Property of Limits]]
- [[Examples of Representable Universal Property of Colimits]]