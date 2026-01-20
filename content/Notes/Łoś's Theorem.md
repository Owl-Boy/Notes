---
id: Łoś's Theorem
aliases:
  - Łoś's Theorem
  - Loś's Theorem
  - Wash's Theorem
tags:
  - Note
---
202601190158

Tags : [[Model Theory]]
# Łoś's Theorem
---
> [!THM] Theorem 
> Suppose $I$ is a non-empty set, $\mathcal M_i$ are non-empty $L$ structures. Let $\mathcal M$ be their direct product and let $U$ be an ultrafilter on $I$. Then for every formula $\varphi\in L_n$ and every $n$-tuple $\bar a$ from $M$.
> $$
> M / U \models \varphi(\bar a / U) \text{ iff } \|\varphi(\bar a)\| \in U.
> $$

Consider formulas $\varphi,\varphi_1,\varphi_2$ and $\theta$, then:
- $\mathcal M / U\models \lnot\varphi(\bar a / U)$ iff $\mathcal M/ U\not\models\varphi(\bar a / U)$ iff $\|\varphi(\bar a)\|\notin U$ iff $\|\lnot\varphi(\bar a)\|\in U$.
- For conjunction and existential operator, the property follows from [[Reduced Product]].

---
# References
- [[Reduced Product]]
- [[Filters]]
- [[Finiteness Theorem]]
