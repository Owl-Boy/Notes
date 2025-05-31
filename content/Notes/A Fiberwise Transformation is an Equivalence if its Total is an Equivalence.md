---
tags:
  - Note
---
202505261805

Tags : [[Homotopy Type Theory]]
# A Fiberwise Transformation is an Equivalence if its Total is an Equivalence
---
>[!lemma]
>If $f$ is a fiberwise transformation between 2 families $P$ and $Q$ over a type $A$, it is an equivalence iff $\text{total}(f)$ is an equivalence.

From [[Total Spaces (HoTT)#^cf9900]] we get for all $x:A, v:Q(x)$ that $\text{fib}_{\text{total}(f)}(x, v)$ is contractible iff $\text{fib}_{f(x)}(v)$ is contractible.

This $\text{fib}_{\text{total}(f)}$ is contractive for all $w:\sum_{x:A}Q(x)$ iff $\text{fib}_{f(x)}(v)$ is contractible for all $x, v$.

---
# References
- [[Contractible Types]]
- [[Fibers (HoTT)]]
- [[Total Spaces (HoTT)]]
- [[Functions as Equivalences]]