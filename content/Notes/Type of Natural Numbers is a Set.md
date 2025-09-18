---
tags:
  - Note
---
202508280108

Tags : [[Homotopy Type Theory]]
# Type of Natural Numbers is a Set
---
>[!theorem]
>The type $\mathbb{N}$ is a [[Sets in Type Theory|set]].

We show that $\mathbb{N}$ has [[Decidability (HoTT)|decidable equality]] and then we get our result from [[Hedberg's Theorem]]. Let $x, y:\mathbb{N}$, we proceed induction on $x$ and case analysis of $y$ to prove $(x=y)+\lnot(x=y)$.
- If $x\equiv{0}$ and
	- $y \equiv 0$, then we have $\text{inl}(\text{refl}_{0})$
	- $y\equiv\text{suc }m$, then we have a proof for $\lnot(x=y)$ which we can use.
- For inductive step, let $x \equiv\text{suc }n$, let 
	- $y \equiv 0$, then we have a proof that $\lnot(x=y)$
	- $y\equiv\text{suc }m$, then we can use the result from $m=n$.

---
# References
- [[Sets in Type Theory]]
- [[Decidability (HoTT)]]
- [[Hedberg's Theorem]]