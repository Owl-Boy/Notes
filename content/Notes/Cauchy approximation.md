---
id: Cauchy approximation
aliases:
  - Cauchy approximation
tags:
  - Note
  - Incomplete
---
202602172241

Tags : [[Homotopy Type Theory]]
# Cauchy approximation
---
We can define a cauchy sequence on rationals as a function $x:\mathbb N\to\mathbb Q$ which satisfies:
$$
\prod_{(\epsilon:\mathbb Q)}\sum_{(n:\mathbb N)}\prod_{m,k\ge n}|x_m - x_k| < \epsilon
$$

We do not truncate the sum type because this way it carries the information of the rate of convergence. In fact by [[Sigma Types respect Universal Properties]], we have the following equivalent type:

$$
\sum_{(M:\mathbb Q_+\to\mathbb N)}\prod_{\epsilon:\mathbb Q_+}\prod_{m,k>M(\epsilon)} |x_m-x_k|< \epsilon.
$$

From this we get that $|x_M(\delta/2)-x_M(\epsilon/2)|\le \delta+\epsilon$ and this carries the same information as the original sequence.

Now we can define a cauchy approximation as an element of the above type:
> [!DEF] 
> A **Cauchy Approximation** is a map $x:\mathbb Q_+\to\mathbb R$ which satisfies
> $$ \forall (\delta,\epsilon :\mathbb Q_+).|x_\delta-x_\epsilon| < \delta+\epsilon. $$
> The limit of such a sequence is a number $l:\mathbb R_d$ such that 
> $$ \forall (\epsilon,\theta:\mathbb Q_+).|x_\epsilon - l| < \epsilon +\delta. $$


---
# References
- [[Dedekind Reals (HoTT)]]
- [[Dedekind Reals are weakly linearly ordered]]
