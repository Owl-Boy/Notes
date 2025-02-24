---
tags:
  - Note
  - Incomplete
---
202502132002

Tags : [[Finite Model Theory]]
# $\text{FO}(\{ +, \times \})$
---
Turns out nonuniform $\text{AC}^0$ is not truly a complexity class. So we a restrict the class to $\text{FO}(\{ +, \times \})$.

>[!theorem] 
>The class of structures definable in $\text{FO}(\{ +, \times \})$ is $\text{AC}^0$.

Here the relation symbols are on natural numbers and are defined as follows;
- $+ = \{ (i, j, k) \ |\ i+j=k \}$
- $\times = \{ (i, j, k) \ |\ i\times j=k \}$

This is more powerful than $\text{FO}(<)$ as we can define $a < b$ as $\exists z (a+z=b)$.
Using that we can also define $\min$ and $\max$.

The integer division $\lfloor x / y \rfloor$ and $x \mod y$ are also definable in $\text{FO}(\{ +, \times \})$
- $u= \lfloor  x / y \rfloor \iff (u \cdot y) \leq x \land \exists v < y(x = u \cdot y + v)$
- $u = x \mod y \iff \exists v\left( v = \lfloor  x / y \rfloor\quad \land\quad u+y \cdot v = x\right)$

Using there we are going to prove the following theorem: [[BIT is expressible in FO(+, *)]].

---
# References
