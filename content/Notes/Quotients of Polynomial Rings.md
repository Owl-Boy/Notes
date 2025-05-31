---
tags:
  - Note
  - Incomplete
---
202505211505

Tags : [[Ring Theory]]
# Quotients of Polynomial Rings
---
Let $R$ be a non-zero ring, and let $f$ be a polynomial in $R[x]$ of degree $d$.

We assume that $f$ is monic for the following reasons.
- A Monic polynomial is necessarily a non-zero divisor
- If $f$ is monic then $\text{deg}(f\cdot g)= \text{deg}(f)+\text{deg}(g)$ for all polynomials $q$.
- We have a convenient notion of division with remainder

That is if $g(x)$ is a polynomial, then one can write
$$
g(x) = f(x) \cdot q(x) + r(x)
$$
where $r$ is a polynomial whose degree is less than that of $f$.

We also have that quotients are remainders are uniquely determined.
>[!lemma]
>Let $f$ be a monic polynomial, then
>$$
>f(x) q_{1}(x) + r_{1}(x) = f(x)q_{2}(x)+r_{2}(x)
>$$
>Where degrees of $r_{1}$ and $r_{2}$ is less than that of $f$, then $q_{1}=q_{2}$ and $r_{1}=r_{2}$.

Straight forward, from the above we have
$$
f(x)(g_{1}(x)-g_{2}(x))=r_{2}(x)-r_{1}(x)
$$
The degree of the expression on the right must be less than $f$, that means $(g_{1}(x)-g_{2}(x))$ must be $0$, and that means $(r_{2}(x)-r_{1}(x))$ must also be $0$.

This is equivalent to the statement
>[!lemma] Corollary
>Let $f$ be a monic polynomial, then for every $g:R[x]$, there is a unique polynomial $r$ such that $\text{deg}(f)>\text{deg}(r)$ for which
>$$
>g(x) + (f(x)) = r(x) + (f(x))
>$$


---
# References
