---
id: Exponential Objects
aliases: []
tags:
  - Note
  - Incomplete
---

202606291425

Tags : [[Category Theory]]

# Exponential Objects

> [!INFO]
> The idea of a exponential object is the capture the hom-set between objects of a category as an object itself.

Consider a category $\cal C$ with objects $A, B, C$ in it, and consider a function $f : C \times A \to B$. Such a function can be curried to $C \to (A \to B)$, where $A \to B$ is precisely the object we want to capture, Using this, we can get the following universal property.

![[exp2.svg]]

This construction simultaneously defines the  object $B^A$ along with the map $ev$ which takes $f : A -> B$ and $a : A$ and returns $f a : B$.

If given any objects $x, y$ in a category, the object $x^y$ exists, then we say the category has exponentiation.

# References
- [[Universal Property (Riehl)]]

