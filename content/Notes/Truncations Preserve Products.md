---
tags:
  - Note
  - Incomplete
---
202508311908

Tags : [[Homotopy Type Theory]]
# Truncations Preserve Products
---
>[!theorem]
>For any types $A, B$ the induced map $\|A\times B\|_{n} \to \|A\|_{n}\times\|B\|_{n}$ is an equivalence.

We can show this by showing that it suffices the universal property of the product. 
$$
\begin{align}
(\|A\|_{n}\times\|B\|_{n} \to C) &= (\|A\|_{n} \to (\|B\|_{n} \to C)) \\
&= (\|A\|_{n} \to (B\to C)) \\
&= (A \to (B \to C)) \\
&=A\times B \to C \\
&= \|A\times B\|_{n} \to C
\end{align}
$$
where $C$ is an $n$-type.



---
# References
