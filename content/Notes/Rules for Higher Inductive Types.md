---
tags:
  - Note
---
202507041207

Tags : [[Homotopy Type Theory]]
# Rules for Higher Inductive Types
---
The introduction rules are specified by the constructors themselves.

For the elimination rule, we take inspiration from simple [[Inductive Types]] and see that when a potential output type satisfies the structure given to the higher inductive type by the constructors, a function can be formed.

For the Induction principle (dependent eliminator), mapping points is straightforward, the paths tho need to connect elements of different types. This can be done using [[Transport]]. We will be calling these **dependent paths**.

We give the following new notation:
$$
u=_{p}^Pv :\equiv (\text{transport}^P(p, u)=v)
$$

---
# References
- [[Inductive Types]]
- [[Transport]]
- [[Loop Space]]
- [[Higher Inductive Types]]