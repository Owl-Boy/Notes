---
tags:
  - Example
---

202412151126

tags : [[Set Theory]]

# Ordered Fields and Archimedean Axiom
---
>[!Theorem]
>The [[Ordered Fields|Axioms of Ordered Fields]] do not imply the Archimedean Axiom

## Without Dedikend Comopleteness

The proof is by constructing a model of [[Ordered Fields]] that does not satisfy the Archimedean Axioms which, given a field $F$, is as follows:
$$
\forall x, y \in F \setminus \{ 0 \} \big[\exists n\in \mathbb{N} [y \leq n \cdot x ]\big]
$$
where $n \cdot x$ is defined as $x$ added to itself $n$ many times.

We first construct a field, and then give it an ordering:
- Consider the field of fractions over the ring of polynomial, hence the terms will be of the form $p(x) / q(x)$ where neither of them have common factors.
- Consider the following ordering on the field.
	- $f < g$ if $f(0)<g(0)$
	- If the functions match on $0$, then compare them at 1 and so on until they disagree.

Check if the axioms hold:
- Since the ring of polynomials is an integral domain, the field of fractions can be constructed, hence all the addition and multiplication axioms are satisfied.
- Ordering axioms
	- reflexivity is trivial
	- If $x \leq y$ and $y \leq x$ then the functions agree on all integers, hence they are the same
	- transitivity is trivial
	- if $x \leq y$ then $x + c \leq y+c$ trivially
	- If $x, y \geq 0$ then the first non $0$ value on integers is positive, hence their product is also positive.

Failure of the Archimedean Axiom:
Consider the functions $f : x \mapsto x$ and $g: x \mapsto x+1$.
Any $k\cdot f$ of the form $x \mapsto k*x$ we have that $k \cdot f(0)<g(0)$.

---
## With Dedikend Completeness
If one has a field with dedikend completeness, we show that the field does satisfy the Archimedean Axiom:

FTSOC consider non zero $x, y$ such that $\forall n\in \mathbb{N}, n \cdot x \leq y$. Then consider the set $X = \{ n \cdot x\;|\;n\in \mathbb{N} \}$. Let $s$ be the supremem, and we have that $s \leq y$. Consider $s' = s-x$. We have that $s' < s$ but $s'$ is also an upper bound for $X$ which contradicts the minimality of $s$. Hence the set $X$ is not bounded which contradicts the hypothesis.


---
# Related
