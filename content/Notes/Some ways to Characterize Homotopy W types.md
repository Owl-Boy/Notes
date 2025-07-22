---
tags:
  - Note
---
202506231606

Tags : [[Homotopy Type Theory]]
# Some ways to Characterize Homotopy W types
---
With [[Homotopy Inductive Types]] defined, one can state the definition of a [[W-Types|W-type]] inside Homotopy Type theory. 

These definitions are very scary, so I am just gonna take screenshots (:.

1. $\sup$ function and induction principle:
  ![[Pasted image 20250623172922.png]]
2. $\sup$ functions, recursion principle, uniqueness principles and some coherence properties:
   ![[Pasted image 20250623174212.png]]
3. [[W-Types are the initial element in the category of W-Algebras]]
   $$
   W_{h}(A, B) :\equiv \sum_{I:W\text{Alg}(A, B)}\text{is-Hinit}_{W}(A, B)
   $$

Turns out that
>[!theorem]
>$W_{s}$, $W_{d}$, $W_{h}$ are all mere propositions are are equivalent.

---
# References
- [[Homotopy Inductive Types]]
- [[W-Types]]
- [[W-Types are the initial element in the category of W-Algebras]]
- [[Inductive Types are Initial Algebras]]