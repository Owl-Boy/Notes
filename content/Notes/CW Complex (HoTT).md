---
tags:
  - Note
aliases:
  - Torus (HoTT)
  - Torus
---
202507230007

Tags : [[Homotopy Type Theory]]
# CW Complex
---
A finite $CW$ complex can be presented as a higher inductive type, by turning $n$-dimensional discs into n-dimensional [[Identity Type|paths]] and partitioning the image of the map into source and target.

The construction of [[Torus (HoTT)|Torus]] is discussed here.

Here the 2nd order constructor might by between concatenation of paths (as in the torus), for that we would need to define composition of dependent path, and that seems easy. 

We can define  composition of dependent paths as follows: Given $p':a=^P_{p}b$ and $q':b=^P_{q}c$ then we can define $p'\cdot q'$ as  as follows:
$$
p'\cdot q' \equiv {q_{*}}(p') \cdot q'
$$
Now to extend the definition of $\text{apd}^2$ so that paths will work here. 

Given dependent path $p':a=^P_{p_{1}\cdot p_{2}\cdots p_{n}}b$ and $q':a=^P_{q_{1}\cdot q_{2}\cdots q_{m}}b$ and $r:(p_{1}\cdot p_{2} \cdots p_{n}=q_{1}\cdot q_{2}\cdots q_{m})$ then we can define $\text{apd}^2(r)$ as follows:
consider $a_{1}=(p_{1}\cdot p_{2} \cdots p_{n})_{*}(a)$ and $a_{2}=(q_{1} \cdot q_{2}\cdots q_{m})$ and we have paths $p':a_{1}=b$ and $q':a_{2}=b$. We now need a path $a_{1}=a_{2}$.

To descrive this, consider the path $p' \cdot q'^{-1}:a=a$. For this path, consider the dependent path,  now we simply push this path by taking $q_{*}(p'\cdot q'^{-1})$ and that gives us a path $a_{2}=a_{1}$. So we are done.

---
# References
- [[CW Complex]]
- [[Torus (HoTT)]]
- [[Functions as Functors]]
- [[Functions as Functors of 2 Category]]
- [[Transport]]
- [[Identity Type]]