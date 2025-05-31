---
tags:
  - Note
---
202505231605

Tags : [[Homotopy Type Theory]]
# Both Directions of Half Adjoints are Logically Equivalent
---
Given a function $f:A \to B$, we have 2 candidate defintions for half adjoint equivalence, that is
- Both most have a function $g:B\to A$
- Both must have a homotopy $\eta:g \circ f \sim \text{id}_{A}$
- Both must have a homotopy $\epsilon:f \circ g \sim \text{id}_{B}$

Now for the first defintion we need 
$$
\tau:\prod_{a:A} f(\eta a)= \epsilon(fa)
$$
and for the second definition we need
$$
\nu: \prod_{b:B} g(\epsilon b)=\eta(gb)
$$
>[!lemma]
>Both the definitions are logically equivalent.

It suffices to show one direction because of the symmetry:
Let $\tau: \prod_{a:A}f(\eta a)=\epsilon(fb)$. We fix $y:B$ and using naturality of $\epsilon$ and  applying $g$ we get the following square:
![[Pasted image 20250523161344.png|300]]
One can apply $\tau(gy)$ on the left equality to get
![[Pasted image 20250523163344.png|300]]
And since $gf=\text{id}$ we get that it commutes with $\eta$ and we get
![[Pasted image 20250523163523.png|300]]

However by naturality of $\eta$ we also have
![[Pasted image 20250523163610.png|300]]
(change is on the right side)

This we get $g(\epsilon y)=\eta(gy)$ as desired.

---
# References
- [[Functions as Equivalences]]
- [[Half Adjoint Equivalences]]
- [[Homotopy(HoTT)]]