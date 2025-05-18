---
tags:
  - Note
---
202505151805

Tags : [[Ring Theory]]
# Units
---
>[!definition]
>An element $u$ of a ring $R$ is a **left-unit** if there is an element $v\in R$ such that $uv=1$. Dually $v$ is a **right-unit**. Two-sided units are called **Units**.

>[!lemma]
>If $R$ is a ring:
>- Left multiplication by left-units is surjetive
>- Right multiplication by left units is injective
>- There is a unique inverse of 2-sided units
>- 2-sided units form a group under multiplication

Proof is as follows:
- Starting at a left-unit, one can left multiply to get $1$ and then multiply to get anything, and use associativity of multiplication.
- Given an element $a$ we have $a \cdot u \cdot u^{-1}=a$, hence right multiplication by $u$ must be injective.
- Consider $2$ inverses $v_{1},v_{2}$, then $v_{1} = v_{1} \cdot u\cdot v_{2} = v_{2}$.
- $R$ is a monoid under multiplication. These units have inverses too, and are closed under multiplication. Hence form a group.

---
# References
