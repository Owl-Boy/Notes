---
tags:
  - Note
  - Incomplete
---
202505022305

Tags : [[Homotopy Type Theory]]
# Types are Higher Groupoids
---
After we have shown [[Identity is an Equivalence]], we now need to show that this is also coherent with the higher groupoid structure, thus we do the following:
>[!lemma]
>Suppose $A:\cal U$ and $x,y,z,w:A$ and that $p:x = y$ and $q: y=z$ and $r: z=w$, then:
>- $p=p\cdot \text{refl}_{y}$ and $p= \text{refl}_{x}\cdot p$
>- $p^{-1} \cdot p = \text{refl}_{y}$ and $p \cdot p^{-1} = \text{refl}_{x}$
>- $(p^{-1})^{-1} = p$
>- $p \cdot(q \cdot r) = (p \cdot q) \cdot r$

>[!note]
>Note that these equalities are propositional.

- For the first one, it is sufficient to show it for the case when $y=x$ and $p=\text{refl}_{x}$, but in this case we have $\text{refl}_{x} \cdot \text{refl}_{x} \equiv \text{refl}_{x}$.
- Same ideas as before
- Path induction again, and we have that $\text{refl}_{x} \equiv \text{refl}_{x}^{-1}$.
- By induction again, we can assume all are $\text{refl}_{x}$ so we get
	- $(p \cdot q) \cdot r$
	- $(\text{refl}_{x} \cdot \text{refl}_{x}) \cdot \text{refl}_{x}$
	- $\text{refl}_{x}$
	- $\text{refl}_{x} \cdot (\text{refl}_{x} \cdot \text{refl}_{x})$
	- $p \cdot (q \cdot r)$

>[!attention]
>Not that this now only talks about the $2$-groupoids structure, but we can extend this idea to any $n$ that we want, we will not be looking at arguments that require full well defined-ness of the $\infty$-groupoids structure.

---
# References
