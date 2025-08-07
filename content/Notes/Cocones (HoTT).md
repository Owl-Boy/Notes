---
tags:
  - Note
---
202507231607

Tags : [[Homotopy Type Theory]]
# Cocones
---
Given a span $\mathcal D=A\xleftarrow f C \xrightarrow g B$ and a type $D$, a **cocone under $\mathcal D$ with nadir $D$** consists of functions $i:A\to D$ and $j:B\to D$ and a homotopy $h:\prod_{c:C}(i(f(c))=j(g(c))):$
![[Pasted image 20250723162352.png|200]]

And we denote $\text{cocone}_{\cal D}(D)$ to be the type of all such cocones:
$$
\text{cocone}_{\cal D}(D):\equiv \sum_{(i:A\to D)}\sum_{(j:B\to D)} \prod_{(c:C)}i(f(c))=j(g(c))
$$

---
# References
- [[Cones and Cocones]]
- [[Identity Type]]