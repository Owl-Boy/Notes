---
id: Dedekind Reals are Cauchy Complete
aliases:
  - Dedekind Reals are Cauchy Complete
tags:
  - Note
---
202602172309

Tags : [[Homotopy Type Theory]]
# Dedekind Reals are Cauchy Complete
---
> [!THM]
> Every [[Cauchy approximation]] in $\mathbb R_d$ has a limit.

Given a Cauchy approximation $x:\mathbb Q_+ \to \mathbb R_d$ define 
$$
\begin{aligned}
L_y(q)&:\equiv \exists(\epsilon,\theta:\mathbb Q_+).L_{x_\epsilon}(q+\epsilon+\theta).\\
U_y(q)&:\equiv \exists(\epsilon,\theta:\mathbb Q_+).U_{x_\epsilon}(q-\epsilon-\theta).
\end{aligned}
$$

It is fairly straightforward to show that these form a dedekind cut.

To show that $y$ is the limit of $x$, consider any $\epsilon,\theta:\mathbb Q_+$, since $\mathbb Q$ is dense in $\mathbb R_d$ there merely exist $q, r$ such that
$$
x_\epsilon-\epsilon-\theta  < q < x_\epsilon-\epsilon-\theta/2 < x_\epsilon
$$
and we give a symmetric condition for $y$. But then we get that $q < y < r$ and hence $|y - x_\epsilon| < \epsilon+\theta$.

---
# References
- [[Dedekind Reals (HoTT)|Dedekind Reals]]
- [[Dedekind Reals are weakly linearly ordered]]
- [[Cauchy approximation]]

