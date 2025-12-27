---
id: The Category Graph is Closed
aliases:
  - The Category Graph is Closed
tags:
  - Note
---
202512272105

Tags : [[Discrete Homotopy Theory]]
# The Category Graph is Closed
---
The internal hom functor $\text{hom}^\otimes$ of 2 graphs $X$ and $Y$ is defined as follows:
$$
\begin{align}
\text{hom}^\otimes(X, Y)_V &= \text{Graph}(X, Y)\\
\text{hom}^\otimes(X, Y)_E &= \{f\sim g \iff \forall x:X, f(x)\simeq g(x)\}
\end{align}
$$
where $f, g\in \text{Graph}(X, Y)$ and $x \simeq y$ means $x \sim y$ or $x = y$.

Thus we can show that the category $\text{Graph}$ is category with exponential objects.

---
# References
- [[Closed Category]]
- [[The Category Graph is Monoidal]]
