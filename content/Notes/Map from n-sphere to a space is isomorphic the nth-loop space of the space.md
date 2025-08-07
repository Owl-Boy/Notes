---
tags:
  - Note
---
202507221707

Tags : [[Homotopy Type Theory]]
# $\text{Map}_{*}(\mathbb S^n, B) \simeq \Omega^n B$
---
From the definition of [[Sphere (HoTT)|Sphere]] and from [[Suspensions (HoTT)|Suspensions]], we can state the following claim
$$
\mathbb S^0 :\equiv \mathbf{2}\quad\quad\text{and}\quad\quad\mathbb S^{n+1}:\equiv \Sigma\mathbb S^n
$$
We also have that [[Maps from Suspension to a space are isomorphic to maps from space to loop space]] so we get the following:
Given a pointed space $(B,b)$
$$
\text{Map}_{*}(\mathbb S^n, B) \simeq\text{Map}_{*}(\mathbb S^{n-1}, \Omega B) \simeq\dots \simeq\text{Map}_{*}(\mathbf{2}, \Omega^n B) \simeq (\mathbf{1}\to \Omega^n B) \simeq \Omega^n B
$$

---
# References
- [[Sphere (HoTT)|Sphere]]
- [[Suspensions (HoTT)|Suspensions]]
- [[Maps from Suspension to a space are isomorphic to maps from space to loop space]]