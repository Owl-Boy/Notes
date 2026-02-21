---
id: Applications of Yoneda Lemma
aliases:
  - Applications of Yoneda Lemma
tags:
  - Example
---
202602201955

Tags : [[Category Theory]]
# Applications of Yoneda Lemma
---
## In Cartesian Closed Categories

To show that 
$$
(A^B)^C \cong A^{B\times C}
$$

We now only need to show:
$$
h((A^B)^C) \cong h(A^{B\times C})
$$
Which is now pretty straigthforward:

$$
\begin{aligned}
\text{Hom}(X, (A^B)^C) &\cong \text{Hom}(X\times C, A^B)\\
&\cong \text{Hom}( (X\times C) \times B, A)\\
&\cong \text{Hom}(X\times (B\times C), A)\\
&\cong \text{Hom}(X, A^{B\times C})
\end{aligned}
$$

And all of this is natural in $X$. Given any function $f:Y\to X$ we simply pre-compose to get the natural transformation.

---
# References
- [[Yoneda Lemma]]
- [[Yoneda Embedding]]
