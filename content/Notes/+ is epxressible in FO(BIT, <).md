---
tags:
  - Note
  - Incomplete
---
202503231703

Tags : [[Finite Model Theory]]
# $+$ is epxressible in $\text{FO}(\text{BIT}, <)$
---
For this the standard carry-forward algorithm works. We first define the ternary relation 
$$
\text{carry}(x, y, u) = \exists v \left( 
\begin{align}
(v < u\  \land\  &\text{BIT}(x, v) \land \text{BIT}(y, u)) \land \\
\forall w (w<u \land w > v) &\to (\text{BIT}(x, w) \land \text{BIT}(y, w))

\end{align}
\right) 
$$

Then we can define $x + y = z$ as
$$
\forall u \left( \text{BIT}(z, u) \leftrightarrow (\text{BIT}(x, u) \otimes \text{BIT}(y, u)) \otimes \text{carry}(x, y, u) \right) 
$$

---
# References
