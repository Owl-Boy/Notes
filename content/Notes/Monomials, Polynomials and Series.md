---
tags:
  - Note
  - Incomplete
---
202502120902

Tags : [[Weighted Automata and Transducers]]
# Monomials, Polynomials and Series
---
We use the following notations for polynomials and series:
- Polynomials : $\mathbb S <A^*>$
- Series : $\mathbb S <\!\!<A^*>\!\! >$

We can now define a distance between 2 series similar to the [[P-addic Distance]] as follows:
$$
d(f, g) = 
\begin{cases}
2^{-r} & \text{where }r = \inf \{ |w| :\!\!|\!\!: w \in A^*, f(w) \neq g(w)\} \\
0 & \text{if } f=g
\end{cases}
$$

---
# References
[[All Proper series are locally finite (weighted automata)]]