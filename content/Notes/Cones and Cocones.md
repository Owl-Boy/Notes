---
tags:
  - Note
  - Incomplete
---
202505151305

Tags : [[Category Theory]]
# Cones and Cocones
---
>[!definition]
>For any diagram of shape $J$ in the category $C$, the **constant functor at** $c:J \to C$ sends every object to $c$ and all moprhisms in $J$ to the identity morphism $\mathbf{1}_{c}$.

>[!definition]
>A **Cone** of a diagram $F:J \to C$ with *summit* or *apex* $c$ is the natural transformation $\lambda:c \to F$ where the codomain is the constant functor at $c$, the components $\lambda_{j} :c \to Fj$ for $j\in J$ are called the *legs* of the cone.
>>[!example] A Cone
>>![[Pasted image 20250515140527.png]]

Dually we have

>[!definition]
>A **Cocone** of a diagram $F:J \to C$ with *nadir* $c$ is the natural transformation $\lambda:F \to c$ where the domain is the constant functor at $c$, whose legs are $\lambda_{j} :Fj\to c$ for $j\in J$.
>>[!example]
>>![[Pasted image 20250515140627.png]]

Another terminology for these are *cones over a diagram* for cones and *cones under a diagram* for cocones.

---
# References
- [[Diagram]]
- [[Limits and Colimits]]