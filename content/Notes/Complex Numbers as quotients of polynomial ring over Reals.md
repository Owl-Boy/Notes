---
tags:
  - Note
  - Incomplete
---
202505211605

Tags : [[Ring Theory]]
# Complex Numbers as quotients of polynomial ring over Reals
---
Since [[Quotienting by monic polynomial is an abelian group isomorphism with direct sum]], these can be used to induce a ring structure to the elements of the direct sum.

For example, consider the polynomial $f(x)=x^2+1$ then we get
$$
R[x] / (x^2+1) \cong R \oplus  R
$$
The homomorphism takes the element $(r_{1},r_{2})$ to $r_{1}+r_{2}x$, the multiplication induced by the above is as follows:
$$
\begin{align}
(r_{1},r_{2}) \cdot(s_{1},s_{2}) &\mapsto (r_{1}+r_{2}x)(s_{1}+s_{2}x) \\
&= r_{1}s_{1} + (r_{1}s_{2}+r_{2}s_{1})x + r_{2}s_{2}x^2 \\
&= r_{1}s_{1} + (r_{1}s_{2}+r_{2}s_{1})x + r_{2}s_{2}(x^2+1) - r_{2}s_{2} \\
&=(r_{1}s_{1}-r_{2}s_{2}) + (r_{1}s_{2}+r_{2}s_{1}) \\
&\mapsto(r_{1}s_{1}-r_{2}s_{2}, r_{1}s_{2}+r_{2}s_{1})
\end{align}
$$
If we consider $R$ to be $\mathbb{R}$ we get that the above construction leads to a simple isomorphism with $\mathbb{C}$, precisely $(a, b)$ is sent to $a+ib$.

---
# References
