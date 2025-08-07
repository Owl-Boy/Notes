---
tags:
  - Note
---
202507281307

Tags : [[Homotopy Type Theory]]
# Idempotent from a relation on a type
---
>[!theorem]
>Suppose $\sim$ is a relation on a set $A$, and there exists an idempotent $r:A\to A$ such that $(r(x)=r(y))\simeq (x\sim y)$  for all $x, y:A$. Then the type 
>$$
>(A /\sim) :\equiv\left( \sum_{x:A} r(x)=x \right)
>$$
>satisfies the universal property of the set quotient of $A$ by $\sim$, and hence is equivalent to it. In other words, there is a map $q:A\to (A / \sim)$ such that for every set $B$, precomposition with $q$ induces an equivalence
>$$
>\left( (A / \sim)\to B \right) \simeq \left( \sum_{(g:A\to B)} \prod_{(x,y:A)} (x\sim y)\to g(x)=g(y) \right)
>$$

Let $i:\prod_{x:A}r(r(x))=r(x)$ be the proof for idempotence. The map $q:A\to A /\sim$ is defined by $q(x):\equiv(r(x),i(x))$. Since $A$ is a set, we have that $q(x)=q(y)$ iff $r(x)=r(y)$ hence by assumption iff $x\sim y$. We define a map $e$ from left to right in the above equivalence by
$$
e(f):\equiv (f\circ q,\_)
$$
where $\_$ denotes teh following proof: if $x,y:A$ and $x\sim y$ then $q(x)=q(y)$ as observed above, hence $f(q(x))=f(q(y))$. We now need to prove that $e$ is an equivalence. Consider the following map in the opposite direction:
$$
e'(g, s)(x, p) :\equiv g(x)
$$
Given any $f:(A /\sim)\to B$
$$
e(e'(f))(x, p)\equiv f(q(x)) \equiv f(r(x), i(x)) = f(x, p)
$$
Similarly for the other direction
$$
e(e'(g, s))\equiv e(g\circ \text{pr}_{1})\equiv(g\circ \text{pr}_{1}\circ q, \_)
$$
But since $B$ is a set, we don't need to worry about the second part, while for the first component we have
$$
g(\text{pr}_{1}(q(x)))\equiv g(r(x))=g(x)
$$
The last equation holds because $r(x)\sim x$

---
# References
- [[Set Quotient]]
- [[Predicate (HoTT)]]
- [[Truncation]]