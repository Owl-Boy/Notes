---
tags:
  - Note
  - Incomplete
---
202505151805

Tags : [[Ring Theory]], [[Monoid Theory]]
# Monoid Ring
---
Given a [[Monoids|monoid]] $(M, \cdot)$ and a ring $R$, then one can obtain the ring $R[M]$ as follows:

The elements of $R[M]$ are the formal linear combinations
$$
\sum_{m\in M} a_{m} \cdot m
$$
 Where the coefficients belong to $R$ and $a_{m}$ is non-zero for at most finitely many summands.

Here addition is defined component-wise
$$
\sum_{m\in M}a_{m} \cdot m + \sum_{m\in M}b_{m} \cdot m = 
\sum_{m\in M}(a_{m} + b_{m}) \cdot m
$$

The multiplication happens between each element
$$
\left( \sum_{m\in M} a_{m} \cdot m \right) \times \left( \sum_{m\in M} b_{m} \cdot m \right) = \sum_{m\in M} \sum_{m_{1}\cdot m_{2}=m}a_{m_{1}}b_{m_{1}}m
$$

The multiplicative identity is defined as $1_{R}\cdot 1_{M}$ and additive identity is defined as the formal sum in which all summands have coefficient $0$.

---
# References
