---
tags:
  - Note
  - Incomplete
---
202502120202

Tags : [[Complexity Theory]]
# $\text{AC}^0$
---
A family of circuits $\mathbb{C} = \{C_{n}\}_{n\in \mathbb{N}}$ is a sequence of circuits where $C_{n}$ where each circuit has $n$ inputs.
A string of length $n$ can be thought of a boolean vector of length $n$, and it is said to be accepted by the family of circuits if $C_{n}$ outputs $1$ on it. This gives a language for the family of circuits.

>[!definition]
>We say that a language has complexity $\text{AC}^0$ if it is accepted by a family of circuits that have polynomial size and constant depth.

^b6c852
There is generally a uniformity bound required to describe the class, for example:
- It should be possible to generate circuits in logtime of the input.

Without this, we get the class $\text{nonuniform AC}^0$. Which even contains problems that are not decidable. This corresponds to being able to use different algorithms for different sized inputs.

---
# References
