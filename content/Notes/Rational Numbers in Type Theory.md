---
id: Rational Numbers in Type Theory
aliases:
  - Rational Numbers in Type Theory
tags:
  - Note
  - Incomplete
---
202602172048

Tags : [[Homotopy Type Theory]]
# Rational Numbers in Type Theory
---
The rational numbers can be constructed as the field of fractions of the [[Integers in HoTT|Integers]] $\mathbb Z$, which can be constructed as the following. 

Consider the equivalence relation $\approx$ on the set $\mathbb {Z \times N}$ given as follows:
$$
(u, a)\approx (v, b) :\equiv u(b+1) = v(a+1)
$$

Here, the pair $(u, a)$ represents the fraction $\frac u {a+1}$

So we can define the set of rational numbers as follows :
$$
\mathbb{Q :\equiv ( Z \times  N) / \approx}
$$

For each rational number $\mathbb Q$ we can pick a canonical representation of it, in the form of its simplest form (no common divisors between numerator and denominator). This makes equality and ordering decidable. It can also be classified as an initial ordered field.

We now define 
$$
\mathbb Q_+ :\equiv \{ q : \mathbb Q \mid q > 0\}
$$

It can also be constructed as the free ring over 1 element.

---
# References
- [[Natural Numbers in Type Theory]]
- [[Integers in HoTT]]
