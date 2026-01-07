---
id: Examples of Complete and Incomplete theories
aliases:
  - Examples of Complete and Incomplete theories
tags:
  - Example
---

202601071249

tags : [[Model Theory]]

#  Examples of Complete and Incomplete theories
---
> [!EXAMPLE] Orders \[$\le;;$\]
> - Pre-orders (not complete) 
>   - $\forall x; x \le x$ (reflexivity)
>   - $\forall x, y, z; x \le y \land y\le z \to x\le z$ (transitivity) 
> - Partial Orders (not complete)
>   - Pre-order 
>   - $\forall x, y; x\le y \land y\le x \to x=y$ (anti-symmetry)
> - Dense Partial Orders (not complete)
>   - Partial Order 
>   - $\forall x, y; x < y \to \exists z; x < z < y$ (density)
>   - $x < y := x \le y \land x \ne y$
> - Dense Partial Order with/without endpoints (Complete!)
>   - Dense Partial Order 
>   - $\exists x; \forall y; x \le y$ or that it doesn't exist (minimum)
>   - $\exists x; \forall y; x \ge y$ or that it doesn't exist (maximum)

> [!EXAMPLE] Lattices \[$\le;\sqcup,\sqcap;$\]
> - Lattices (not complete)
>   - Partial Order 
>   - $\sqcup$ works like least upper bound of 2 elements and $\sqcap$ is the greatest lower bound of 2 elements.
> - Distributive Lattices (not complete)
>   - $\forall x, y, z; x\sqcup (y\sqcap z) = (x\sqcup y)\sqcap (x\sqcup z)$
>   - $\forall x, y, z; x\sqcap (y\sqcup z) = (x\sqcap y)\sqcup (x\sqcap z)$
> - Boolean Lattice \[$1,0,\lnot$\] (not complete)
>   - 1 is maximum element and 0 is minimum 
>   - $\forall x, x \sqcup \lnot x = 1 \land x\sqcap \lnot x = 0$
> - Boolean Lattice without atoms (Complete!)
>   - Boolean Lattice 
>   - $\forall y; y > 0 \to \exists z; 0 > z > y$

> [!EXAMPLE] Groups \[$0, *$\]
> - Group (not complete)
>   - [[Groups In First Order Logic]] 
> - Abelian Group (not complete)
>   - Group
>   - $\forall x, y; x * y = y * x$
> - Groups of finite order (fixed prime $p$) (not complete)
>   - Group
>   - $\forall x; x + x + ... x (p \text{times}) = 0$
> - Abelian Groups of finite order (complete)
>   - Abelian Group 
>   - Group of finite order (fixed $p$)

---
# Related
- [[Groups In First Order Logic|Groups in First Order Logic]]
- [[First Order Logic]]
