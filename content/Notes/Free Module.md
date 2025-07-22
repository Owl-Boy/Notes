---
tags:
  - Note
---
202506211706

Tags : [[Module Theory]]
# Free Module
---
Given a ring $R$, the free module over a set $A$ defines 'the' module that contains $A$. We pick a module as 'the' representative of the set $A$ when it would have as little structure as possible, that is, only what is forced by the axioms of modules. 

Thus we want to find the shape $f:A \to R$ which fulfills our requirement for 'containing $A$', and we impose the require for least structure by having maps to any other shape that looks like this.

That is, we find the [[Initial, Terminal and Zero Objects|initial]] object in the category whose objects are such shapes, and whose morphisms are commutative squares. Thus having the following property:
![[Pasted image 20250621175018.png|200]]
For any $f:A\to M$, it factors through $F^R(A)$.

This is given by the ring, that has an independent copy of $R$ for each element of $A$, hence we can write:
$$
F^R(A) :\equiv \bigoplus_{A}R \equiv R^{\oplus A}
$$
It is fairly straightforward to see that, this does form an $R$ module along with the map that sends an element of $A$ to the $1$ of a component and that satisfies the [[Universal Property (Riehl)]] of the free object.

---
# References
[[Free Group]]
[[Free Module]]
[[Free Abelian Group]]
[[Initial, Terminal and Zero Objects]]
[[Universal Property (Riehl)]]
