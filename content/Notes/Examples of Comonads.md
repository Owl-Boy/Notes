---
tags:
  - Example
---

202507302256

tags : [[Category Theory]]

#  Examples of Comonads
---
>[!example]
>A monad on a preorder $(P, \leq)$ is given by an order preserving function $T:P\to P$ that so that $p \leq Tp$ and $T^2p \leq Tp$. If $P$ is a poset, so that isomorphic objects are equal then the condition implies $T^2p=Tp$. An order preserving function $T$ so that $p\leq Tp=T^2p$ is called a **closure operator**. Dually, a comonad on a poset category $(P, \leq)$ defines a **kernel operator**: an order preserving function so that $Kp \leq p$ and $Kp=K^2p$. 

---
# Related
- [[Monads and Comonads]]