---
tags:
  - Note
---
202506171506

Tags : [[Homotopy Type Theory]]
# $\mathbb{N}$ is the initial object in the category of $\mathbb{N}$-Algebras
---
Consider an arbitrary $\mathbb{N}$-algebra $\mathcal D:\equiv(D,d_{0}, d_{s})$. To construct a $\mathbb{N}$-homomorphism, we first construct a function $f:\mathbb{N} \to D$ which can be defined using the recursion principle of $\mathbb{N}$.
$$
\begin{align}
f(0) &:\equiv c_{0} &&\equiv d_{0}\\
f(\text{suc }k) &:\equiv c_{s}(k, f(k)) &&\equiv d_{s}(f(k))
\end{align}
$$
Now its easy to show that this is a $\mathbb{N}$-homomorphism. And because of [[Uniqueness of functions created using induction principle]], we get that the type of $\mathbb{N}$-homomorphisms is contractible. $\square$

---
# References
- [[Type of Natural Number Algebra]]
- [[N is the initial object in the category of N-Algebras]]
- [[Initial, Terminal and Zero Objects]]
- [[Inductive Types]]
- [[Inductive Types are Initial Algebras]]
- [[Natural Numbers in Type Theory]]
- [[Uniqueness of functions created using induction principle]]