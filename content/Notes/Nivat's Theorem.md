---
tags:
  - Note
  - Incomplete
---
202504201604

Tags : [[Weighted Automata and Transducers]]
# Nivat's Theorem
---
>[!theorem]
>The following are equivalent:
>- $R \subseteq A^* \times B^*$ is a rational relation
>- There exists and alphabet $C$ and morphisms $H:C \to A^*$ and $G:C \to B^*$ and a regular language $K \subseteq C^*$ such that for $f : w \to (H(w), G(w))$, we have $R = f(K)$.
>	- This is called a *bimorphism*.


To go from $2 \to 1$ we have that $f$ is a morphism from the semi-rings $C^*$ to $A^* \times B^*$, hence we can write $R$ as a rational expression over $C$, this $f$ takes it to a rational relation in $A^* \times B^*$.

To go in the other direction, we can take $C$ to be  $A \sqcup B$ and we get a simple homomorphsim $f$, which just projects into both alphabets and pairs them together, we get a regular subset of $C^*$ by taking the rational expression of $R$ and treating it like a regular language over $A \sqcup B$, this is done by replacing $(a, \epsilon)$ with $a$ and $(\epsilon, b)$ with $b$.

---
# References
