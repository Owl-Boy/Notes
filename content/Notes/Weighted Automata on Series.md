---
tags:
  - Note
  - Incomplete
---
202502121502

Tags : [[Weighted Automata and Transducers]]
# Weighted Automata on Series
---
[[Kleene Shutzenberger Theorem]] states that recognizable functions are the same as rational series, we can consider automata that multiply a [[Monomials, Polynomials and Series|polynomial]] to the partial series that has been constructed so far as follows:

>[!todo] TODO : Draw a diagram from the transition matrix below

A transition matrix for the automata given in the above example would like, all these are necessarily degree 1 terms
$$
\begin{bmatrix}
a+2b & 3a \\
4b & 2a+3b
\end{bmatrix}
$$
To find the value of a word of length $n$, find the coefficient of a word $w$ in $I \cdot \mu^n \cdot F$.

This is also clearly closed under addition, scalar multiplication (left multiply to initial vector, right multiply to final vector) and cauchy product, all have similar constructions to [[Closure Properties of Recognizable functions]].

This shows that all Rational Functions are Recognizable.

>[!todo] TODO write construction for Kleene Star

---
# References
