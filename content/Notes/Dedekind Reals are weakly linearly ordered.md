---
id: Dedekind Reals are weakly linearly ordered
aliases:
  - Dedekind Reals are weakly linearly ordered
tags:
  - Note
---
202602172207

Tags : [[Homotopy Type Theory]]
# Dedekind Reals are weakly linearly ordered
---
We can define $<$ and $\le$ operators as follows:
$$
\begin{aligned}
(x\le y)&:\equiv \forall(q:\mathbb Q).L_x(q)\Rightarrow L_y(q)\\
(x<y)&:\equiv \exists(q:\mathbb Q). U_x(q)\land L_y(q)
\end{aligned}
$$

We have that linearly is valid if we have excluded middle.
$$
(x \le y) \lor (y\le x)
$$
but without it we get a weaker version of linearity.
$$
(x\le y)\Rightarrow (x\le z)\lor (z\le y)
$$

Here if we let $u = (x+y)/2$ and $\epsilon=(y-x)/2$ we can rewrite the above expressions as:
$$
(u-\epsilon < z)\lor (z < u+\epsilon)
$$

Since we don't have linearity, sating that $x\le y \lor y \le x$ is a stronger statement than $x\ne y$, so we define:
$$
x\#y :\equiv x\le y \lor y\le x
$$

---
# References
- [[Dedekind Reals (HoTT)]]
