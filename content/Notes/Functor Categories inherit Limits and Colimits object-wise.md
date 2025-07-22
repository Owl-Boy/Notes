---
tags:
  - Note
---
202505301405

Tags : [[Category Theory]]
# Functor Categories inherit Limits and Colimits object-wise
---
>[!theorem]
>If $A$ is small category, then the forgetful functor $C^A \to C^{\text{ob }A}$ strictly creates all limits and colimits that exist in $C$. These limits are defined objectwise, that is for each $a$ the evaluator function $\text{ev}_{a}: C^A\to C$ preserves all limits and colimits.

The functor category $C^{\text{ob }A}$ is the $A$-indexed product of $C$ with itself in the cateogry $\text{CAT}$, a diagram of shape $J$ is an $A$-indexed product of diagrams of shape $J$ in $C$, and a limit of each of the diagram assemble into a limit of a diagram in $\prod_{a:\text{ob }A}C$. Thus $C^{\text{ob} A}$ contains all limits of $C$ that can be evaluated pointwise.

To show that $C^A\to C^{\text{ob }A}$ strictly creates all limits and colimits, we show that for any $F:J\to C^A$, the $\text{ob }A$-indexed family of objects $\text{lim}_{j\in J} F_{j}(a)$ extends to function on $A$ valued in $C$. The universal property of limits is used to define action of the functor on morphisms in $A$, and uniqueness of the universal object implies that this contruction is functorial.

---
# References
- [[Limits and Colimits]]
- [[Functors]]