---
tags:
  - Note
---
202505231705

Tags : [[Homotopy Type Theory]]
# Fibers of Half Adjoint Equivalences are Contractible
---
>[!lemma]
>If $f: A\to B$ is a [[Half Adjoint Equivalences|half adjoint equivalence]], then for any $y:B$ the fibre $\text{fib}_{f}(y)$ is contractible.

Let $(g, \eta, \epsilon, \tau):\text{ishae}(f)$ and fix $y:B$. For the center of contraction we choose $(gy, \epsilon y)$. Consider any point $(x, p):\text{fib}_{f}(b)$, we need to show $(x,p)=(gy, \epsilon y)$. We first need to show $gy=x$.
$$
\begin{align}
p&:f(x)=y \\
g(p)&:g(f(x))=g(y) \\
\eta(x)^{-1} \cdot (g(p)) &: x=g(f(x))=g(y) \\
g(p)^{-1}\cdot \eta(x)&: g(y)=x
\end{align}
$$
So we put $\gamma:\equiv g(p)^{-1} \cdot \eta(x)$. We have $f(\gamma):f(g(y))=f(x)$ so we get
$$
\begin{align}
f(\gamma) \cdot p &= fg(p)^{-1} \cdot f(\eta x) \cdot p \\
&=fg(p)^{-1} \cdot \epsilon(fx) \cdot p \\
&= \epsilon y
\end{align}
$$
where the second equality is by $\tau$ and the third is by the naturality of $\epsilon$.

For the naturality part, we the endofunctions $\text{id}_{B}$ and $(f\circ g)$ and those are what we are natural over, we get that $f(g(p^{-1})) \cdot \epsilon(f x)=\epsilon(fx) \cdot p^{-1}$.

---
# References
- [[Fibers (HoTT)]]
- [[Half Adjoint Equivalences]]
- [[Contractible Types]]
- [[Natural Transformation]]
