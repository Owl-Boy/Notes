---
tags:
  - Note
  - Incomplete
---
202505172105

Tags : [[Homotopy Type Theory]]
# Decidability
---
With the notion of [[Mere Propositions]] in HoTT, one can consider types for which law of excluded middle holds in constructivist logic too:

>[!definition]
>- A type is called **decidable** if $A + \lnot A$
>- A type family $B:A \to\cal U$ is called **decidable** if $\prod_{a:A}B(a)+\lnot B(a)$
>- In particular, a type has **decidable equality** if $\prod_{a,b:A}(a=b + a\neq b)$

The following version of law of excluded middle can now be phrased as stating taht all mere propositions are **decidable**:


>[!definition] Law of Excluded Middle
>$$
>\text{LEM} :\equiv \prod_{A:\cal U} \text{isProp}(A) \to (A+ \lnot A) 
>$$

This version of $\text{LEM}$ avoid the proof in [[Double Negation Does Not Cancel]], because $\mathbf{2}$ is not a mere proposition. The more general version of $\text{LEM}$ which contradicts univalence can be written as follows:
$$
\text{LEM}_{\infty} :\equiv \prod_{A:\cal U} A+\lnot A
$$



---
# References
