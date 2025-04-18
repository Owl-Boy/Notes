---
tags:
  - Note
  - Incomplete
---
202504101904

Tags : [[Finite Model Theory]]
# Fixed Points
---
Given  [[Monotone, Inflationary and Inductive Functions]] on a partial order $(L, \leq)$, one can get the following collection of fixed point.
- If $f$ is monotone, and $(L, \leq)$ is a complete lattice, then there are always fixed points, which themselves form a complete lattice, specifically there must exists a **Least Fixed Point** of $f$ called the $\text{lfp}(f)$, this is from the [[Knaster-Tarski Theorem]].
- In case of $f$ being inflationary, we say that $x_{\infty}$ is the **Inflationary Fixed Point** of $f$ if it is a fixed point and is denoted as $\text{ifp}(f)$. In case of finite orders, this is always a fixed point.
- In general, given a function $f$ we define the **Partial Fixed Point** of the function as follows:
	- $x_{\infty}$ if $\exists n_{0}$ such that for all $n \geq n_{0}$ we have $x_{n}=x_{n+1}$
	- otherwise we define it as $\bot$
	- This is denoted as $\text{pfp}(f)$

>[!lemma]
>If $f$ is monotone and $(L, \leq)$ is a finite complete lattice, then 
>$$
>\text{lfp}(f) = \text{ifp}(f) = \text{pfp}(f)
>$$

---
# References
