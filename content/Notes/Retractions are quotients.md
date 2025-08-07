---
tags:
  - Note
---
202507281307

Tags : [[Homotopy Type Theory]]
# Retractions are quotients
---
>[!theorem]
>Suppose $p:A\to B$ is a [[Retracts (HoTT)|retraction]] between sets. Then $B$ is the [[Set Quotient|quotient]] of $A$ by the equivalence relation $\sim$ defined by :
>$$
>(a_{1}\sim a_{2}) :\equiv (p(a_{1})=p(a_{2})).
>$$

Suppose $s:B\to A$ is a section of $p$. Then $s\circ p:A\to A$ is an idempotent which satisfies the condition in [[Idempotent from a relation on a type]]. This induces an isomorphism from $B$ to the set of fixed points of $s\circ p$. 

---
# References
- [[Retracts (HoTT)]]
- [[Set Quotient]]
- [[Idempotent from a relation on a type]]