---
tags:
  - Note
---
202412071812

Tags : [[Topology via Logic]], [[Logic]]
# Geometric Propositional Logic
---
>[!tip] Motivation
>The trivial examples in [[Affirmative and Refutative Assertions]] were a matter of interpretation of statement. Once the interpretation is done, one would want a logical framework around the idea of "affirmative" and "refutative" so one can talk about complicated assertions built from simpler assertions.

- Negation ($\lnot$)
	- if $P$ is affirmative, then we can say that $\lnot P$ is refutative and vice versa.
- Conjunction ($\land$)
	- If $P$ and $Q$ are affirmative, then $P \land Q$ is also affirmative, same with refutative statements. This can be extended to finite conjunctions.
	- If $Q_{i}$  where $i\in \mathbb{N}$ are all refutative then $\bigwedge Q_{i}$ is refutative.
- Disjunctions ($\lor$)
	- If $P$ and $Q$ are affirmative, then $P \lor Q$ are also affirmative, same with refutative statements. This can be extended to finite disjunctions.
	- If $P_{i}$ where $i\in \mathbb{N}$ are all affirmative, then $\bigvee P_{i}$ is also affirmative.
- Implications ($\to$)
	- If we want $P \to Q$ to be affirmative, and we have that $Q$ is affirmative, we are forced to make $P$ refutative, as if $Q$ is not true, then we are forced to check if $P$ is false too, to check if $P\to Q$ is true. 
- Distributivity
	- We have that conjunctions distribute over arbitrary disjunctions of affirmative statements
	- We have that disjunctions distribute over finite conjunctions.

---

The l logic of affirmative assertions gives us *Geometric Propositional Logic*:
- Arbitrary disjunctions are allowed, *false* can be written as the empty disjunctions
- Finite conjunctions are allowed, *true* can be written as the empty conjunction
- conjunctions distribute over arbitrary disjunctions and disjunctions distribute over finite conjunctions.
- We do not have implications, negation and infinite conjunctions.


>[!info] Hmmmm
> This idea definitely feels like topology.

---
# References
[[Affirmative and Refutative Assertions]]