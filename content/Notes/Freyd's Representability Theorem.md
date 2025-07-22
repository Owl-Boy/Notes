---
tags:
  - Note
---
202507211507

Tags : [[Category Theory]]
# Freyd's Representability Theorem
---
>[!theorem]
>Let $F:C\to\text{Set}$ be a [[Continuous and Cocontinuous Functor|continuous functor]] and let $C$ be [[Complete and Cocomplete Categories|complete]] and [[Small Categories|Locally Small]]. If $F$ satisfies the solution set condition:
>- There exists a set $\Phi$ of objects of $C$ so that for any $c\in C$ and any element $x\in Fc$, there exists an object $s\in \Phi$ and an element $y\in Fs$, and a morphism $f:s\to c$ such that $Ffy=x$,
>
>Then $F$ is representable.

The solution set defines a [[Weakly initial objects and joint weakly initial sets|jointly weakly initial]] set of objects in the comma category $*\downarrow F\cong \int F$. Then by [[Forgetful functor from comma category strictly creates limits]] we have that this category is complete, so by [[A locally small, complete category with a small coseparator and intersections of all collections of subobjects has an initial object]] we have that $\int F$ has an initial rate. And since [[Universal Elements are Universal Elements]], we have a representation for $F$.

---
# References
- [[Continuous and Cocontinuous Functor]]
- [[Complete and Cocomplete Categories]]
- [[Small Categories]]
- [[Weakly initial objects and joint weakly initial sets]]
- [[Forgetful functor from comma category strictly creates limits]]
- [[A locally small, complete category with a small coseparator and intersections of all collections of subobjects has an initial object]]
- [[Universal Elements are Universal Elements]]
- [[Representable Functors]]