---
tags:
  - Note
---
202507271807

Tags : [[Homotopy Type Theory]]
# Integers
---
There are many ways to define a integers, but most of then are [[Set Quotient]]s. Some of the ways to define it are:

$$\mathbb{Z} :\equiv (\mathbb{N} \times \mathbb{N}) / \sim$$
where $\sim$ is the equivalence relation defined by 
$$
(a, b)\sim (c, d) :\equiv (a+d = b+c)
$$

Another way is to define the equivalence relation of the disjoint union
$$
\mathbb{Z} :\equiv \mathbb{N} + \mathbb{N} / \sim
$$
where the equivalence relation is trivial except for the two zeroes. 

---
# References
- [[Set Quotient]]
- [[Natural Numbers in Type Theory]]