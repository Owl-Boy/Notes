---
tags:
  - Example
---
202508161608
 
Tags : [[Category Theory]]
# Examples of Kliesli Category
---
>[!example]
>Consider the [[Maybe Monad]] on $\text{Set}$. A map $A\rightsquigarrow B$ in the Kleisli category is a function $A\to B_{+}$, which may be thought of as a partial function from $A$ to $B$. The elements of $A$ that are sent to the free basepoint have undefined output. The composite of two partial functions is the maximal partially defined function. Thus the Kleisli category is the category $\text{Set}^\partial$ of sets and partially defined functions.

>[!example]
>For a fixed set $S$ of states, the adjunction $S \times- \dashv (-)^S$ induces a monad $(S \times-)^S$ on $\text{Set}$. A map $A\rightsquigarrow B$ is a function $f:A\times S \to B \times S$ that takes an input $a$ together with the current state $s$ and returns the output $f_{s}(a)$, dependent on both the input and the state, together with a new updates state $s'$. This is called the **state monad** in haskell.

---
# References
- [[Kleisli Category]]
- [[Maybe Monad]]
- [[List Monad]]
- [[State Monad]]