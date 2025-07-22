---
tags:
  - Note
---
202505102305

Tags : [[Category Theory]]
# Equivalence of Definitions of Universal Property
---
The 2 definitions of **Universal Property** one by [[Universal Property (Riehl)|Riehl]] and the other by [[Universal Property (Mac Lane)|Mac Lane]]:

I think the rough idea is, whatever Mac Lane is trying to capture using the morphisms in the category $D$, Riehl is trying to capture that using objects. The notion of **Universal Morphism** in the Mac lane definition behaves the same way as the **Universal Element** as described by Riehl.

So consider categories $C,D$, a functor $F:C \to D$ and an object $X:D$ such that one can give a **Universal Morphism** which is the pair $(A, u: X\to FA)$. which has the **Universal Property**.

For the above example, Riehl would ask you to consider the categories $C, \text{Set}$ and $G:\equiv X \to F(-)$ for some set $X$. The first component of the **Universal Morphism** corresponds to the object $c:C$ that represents the functor $G$. 

[[Yoneda Lemma]] tells us that there is a bijection between the set $Gc$ and the set $\text{Hom}_{\text{Cat}}(\text{Hom}_{C}(A, -), G)$ In particular it sends the isomorphism $\alpha$ between the 2 functors (given by the fact that $c$ represents $G$) to the element $u$ in $G(A)$ which Riehl calls the **Universal Element**, which corresponds to the the second component of the **Universal Morphism**. (This is computed by $\alpha_{A}1_{A}$).

Now given any element $u'\in G(A')\in \text{Set}$, we have a bijection to $\text{Hom}(A, A')$ which gives $\alpha_{A'}^{-1}(u')$, but $G$ is a functor so we have $G(\alpha^{-1}(u')): G(A) \to G(A')$, this corresponds to the morphism $Ff$ which was induced in case of Mac Lane.

And so Riehl gives the definition of a **Universal Property** as the tuple $(A, u)$. 


---
# References
- [[Universal Property (Riehl)]]
- [[Universal Property (Mac Lane)]]