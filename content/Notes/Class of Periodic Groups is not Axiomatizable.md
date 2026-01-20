---
id: Class of Periodic Groups is not Axiomatizable
aliases:
  - Class of Periodic Groups is not Axiomatizable
tags:
  - Note
---
202601201234

Tags : [[Model Theory]]
# Class of Periodic Groups is not Axiomatizable
---
> [!THM] Theorem 
> Let $\Sigma$ be a set of sentences containing the [[Monoids|monoid axioms]].
> If $\Sigma$ has, for any $n$, a model containing an element of **order** at least $n$. Then $\Sigma$ has a model containing an element with infinite order.

Let $L$ be the language containing the monoid symbols. Let $L'$ be $L$ with a new constant symbol $c$. Define $\Sigma'= \Sigma \cup \{c^n\ne 1 : n \in \mathbb N\}$.

Any model of $\Sigma'$ is a model of $\Sigma$, thus fining a model for that theory is sufficient.

By finiteness theorem, we need to find a model for all finite subsets of $\Sigma'$.

For every finite subset, consider the equations in the subset $\{c^n\ne 1 : n \in \mathbb N\}$, any finite subset of these equations, will have a largest $n$ used. Let $p$ be a prime number bigger than $n$. Then $\mathbb Z / p\mathbb Z$ is a group where the generator has order at least $n$.

Thus, by [[Finiteness Theorem]], we can get a model for $\Sigma'$.

> [!COR] Corollary 
> The class of periodic groups is not axiomatizable.

---
# References
- [[Monoids]]
- [[Semi-Groups]]
- [[Finiteness Theorem]]]]
