---
tags:
  - Note
---
202505042205

Tags : [[Category Theory]]
# Commuting of Rectangles and Squares
---
Given a rectangle such taht its outermost morphisms commute does not imply that the inner squares commute, for example.

![[Pasted image 20250504230042.png]]

This is because for that to work, the first and last morphisms must be cancellable, hence we get the following lemma:

>[!lemma]
>Consider the morphisms with the indicated sources and targets
>![[Pasted image 20250504230353.png]]
>Then this data defines a commutative rectangle if either:
>- Right square commutes and $m$ is a monomorphism
>- Left square commutes and $f$ is an epimorphism

The statements are duals, so to prove the first one, we have $m \cdot h \cdot f =m \cdot k \cdot h$, and since $m$ is a monomorphism we can cancel it out.

---
# References
- [[Category]]