---
tags:
  - Note
  - Incomplete
---
202505091405

Tags : [[Category Theory]]
# Universal Property
---
To define a **Universal Property** we must first define what a **Universal Construction** is. To define a **Universal Construction**, one needs the following:
- Categories $C, D$.
- A functor $F: C \to D$
- An object $X:D$ 

We call the pair $(A, u: X \to F(A))$ a **Universal Morphism** from $X$ to $F$ if it has the following property that is called the **Universal Property**. (here, $A:C$)

For any morphism $u':X \to F(A')$, there is a unique morphism $h:A \to A'$ such that the following diagram commutes:
![[Pasted image 20250510010744.png|400]]

There is a dual notion for this concept which is the **Universal Morphisms** from $F$ to $X$,that is the pair $(A, u:F(A) \to X)$ such that for any morphism $u':F(A') \to X$ there is a unique morphism $h: A' \to A$ such that the following diagram commutes:

![[Pasted image 20250510011743.png|400]]



---
# References
[[Universal Property (Riehl)]]