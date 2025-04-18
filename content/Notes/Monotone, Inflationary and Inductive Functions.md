---
tags:
  - Note
  - Incomplete
---
202504101904

Tags : [[Finite Model Theory]]
# Monotone, Inflationary and Inductive Functions
---
>[!definition]
>$f$ is called **monotone** if $x \leq y \implies f(x) \leq f(y)$
>
>$f$ is called **inflationary** if $x \leq f(x)$
>
>let $x_{0} = \bot$ and $x_{i+1} = f(x_{i})$, then we say $f$ is **inductive** if $x_{i} \geq x_{i+1}$

---
>[!lemma]
>If $f$ is monotone or inflationary, then $f$ is inductive.

This is easy, if $f$ is inflationary, then $x_{i} \leq f(x_{i})=x_{i+1}$, so we are done.

If $f$ is monotone, then we have that if for some $a$, $x_{a} \leq x_{a+1}$ then for all $b>a, x_{b} \leq x_{b+1}$. But $x_{0}= \bot$, so we have $x_{0} \leq x_{1}$, hence $f$ is inductive.

---
# References
