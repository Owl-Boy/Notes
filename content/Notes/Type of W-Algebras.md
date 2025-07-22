---
tags:
  - Example
---

202506171540
tags : [[Homotopy Type Theory]]
#  Type of W-Algebras
---
We define the type or $W$-algebras using the [[Polynomial Functor]]:
$$
P(X) = \sum_{x:A}(B(x)\to X)
$$
A $P$-algebra is a type $C$ equipped with a function $s_{C}:PC \to C$. By the [[Universal Property (Riehl)]] of [[Dependent Pair Types|Sigma Types]], this is equivalent to 
$$
\prod_{a:A}(B(a)\to C) \to C
$$
we call such objectrs $W$-Algebras for $A$ and $B$ and write it as:
$$
W\text{Alg}(A, B) :\equiv \sum_{C:\cal U}\prod_{a:A}(B(a)\to C)\to C
$$
To define a morphism between $P$-algebras $(C,s_{C})$ and $(D,s_{D})$ $(f, s_{f})$ consists of $f:C\to D$ and  $s_{f}$ which is a homotopy between maps $PC\to D$ stating $s_{f}:f\circ s_{C} = s_{D}\circ Pf$, that we have the following diagram.
![[Pasted image 20250617155334.png|200]]
Thus we get the type of $W$-homormophism between $W$-algebras $\mathcal C :\equiv (C, s_{C})$ and $\mathcal D:\equiv(D, s_{D})$ is:
$$
W\text{Hom}_{A, B}(\mathcal C, \mathcal D) :\equiv \sum_{f:C\to D} \prod_{(a:A)} \prod_{h:B(a)\to C} f(s_{C}(a, h))=s_{D}(a, f\circ h)
$$
Just like Natural Numbers, we have that [[W-Types are the initial element in the category of W-Algebras]].

---
# Related
- [[Polynomial Functor]]
- [[Dependent Pair Types]]
- [[Universal Property (Riehl)]]
- [[W-Types]]
- [[Initial, Terminal and Zero Objects]]
- [[W-Types are the initial element in the category of W-Algebras]]
