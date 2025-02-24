---
tags:
  - Note
  - Incomplete
---
202502240002

Tags : [[Finite Model Theory]]
# Even is $(MSO + <)_{\text{inv}}$-expressible
---
This is fairly easy. With [[Monadic Second Order Logic]], one can quantify a set. If there exists a set which contains exactly half of the model then we are done, and $<$ lets us express that in the following formula:

$$
\exists X\Big(\exists x\ y, \big(\text{first}(x) \land \text{last}(y) \land \forall z (z\neq y \to z\in X \iff \text{next}(z)\not\in X)\big)\Big)
$$
Where we have the following definitions:
- $\text{first}(x)\equiv \forall y, x \leq y$
- $\text{last}(y) \equiv \forall x, x\leq y$
- $\text{next}(w,z) \equiv \lnot \exists x, w\leq x \leq z$

There has been a slight abuse of notation and $\text{next}$ has been defined as a function.

This also shows that $\text{MSO} \subsetneq (\text{MSO}+<)_{\text{inv}}$

---
# References
