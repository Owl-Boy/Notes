---
tags:
  - Note
---
202508311808

Tags : [[Homotopy Type Theory]]
# Universal Property of Truncations
---
>[!theorem]
>Let $n\geq -2$, $A:\cal U$ and $B:n$-type. The following map is an equivalence:
>$$
>\begin{cases}
> &(\|A\|_{n}\to B)  &\longrightarrow &(A\to B) \\
> &g &\longmapsto &g\circ |-|_{n}
>\end{cases}
>$$

Given that $B$ is $n$-truncated, any $f:A\to B$ can be extented to a map $\text{ext}(f):\|A\|_{n}\to B$. The map $\text{ext}(f)\circ|-|_{n}$ is equal to $f$, because for every $a:A$ we have $\text{ext}(f)(|a|_{n})=f(a)$ by definition. And the map $\text{ext}(g\circ |-|_{n})$ is equal to $g$ because both send $|a|_{n}$ to $g(|a|_{n})$.

This says that $n$-types form a [[Reflective Subcategory]]

---
# References
- [[Universal Property (Riehl)]]
- [[Reflective Subcategory]]
- [[Truncation]]