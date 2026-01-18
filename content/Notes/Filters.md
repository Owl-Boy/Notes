---
id: Filters
aliases:
  - Filters
tags:
  - Note
---
202601172250

Tags : [[Order Theory]]
# Filters
---
Given a partial order $P$, a filter $F$ on it is a subset of $P$ such that its members are 'large enough' to satisfy some property.

> [!DEF] Definition
> A filter $F$ on a partially ordered set $P=(|P|, \le)$ is a subset of $|P|$ such that:
> - It is upwards closed, that is, if $x\in F$ and $y\ge x$ then $y\in F$.
> - Given any 2 elements, their greatest lower bound is in the set.


> [!EXAMPLE]
> Consider the powerset of any infinite set ordered by inclusion. The collection of all cofinite sets give a filter. This is called the **Frechet Filter**.

---
# References
- [[Model Theory]]
