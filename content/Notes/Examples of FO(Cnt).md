---
tags:
  - Note
  - Incomplete
---
202504272004

Tags : [[Finite Model Theory]]
# Examples of $\text{FO(Cnt)}$
---
>[!example]
>One can compare cardinalities between sets $\varphi$ and $\psi$.
>$$
>\exists i \Big[\exists ix \varphi(x) \land \lnot \exists ix \psi(x)\Big]
>$$

>[!example]
>One can also test if majority of elements of the model satisfy the predicate:
>$$
>\exists i \Big[\exists ix\ \varphi(x) \land \lnot \exists ix\ (\lnot \varphi(x))\Big]
>$$

>[!example]
>One can also express $\text{even}$ as follows:
>$$
>\exists i,j \Big[(i=j+j) \land \exists ix\varphi(x) \land \big(\forall k,  k>i \to \lnot\exists kx\varphi(x)\big) \Big]
>$$
---
# References
