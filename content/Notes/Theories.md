---
id: Theories
aliases:
  - Theories
tags:
  - Note
---
202601071252

Tags : [[Model Theory]] 
# Theories
---
> [!DEF] Definition
> A Theory is a set of sentences in a formal language (for our purposes [[First Order Logic]]).

A Theory $T$ is defined to be:
- Consequence-closed if, whenever $S\subseteq T$ and $S\models \phi$ then $\phi\in T$.
- Consistent if there is no proof of the contradiction $\bot$, equivalently, by [[Completeness of First Order Logic]], if there exists a [[Semantics of First Order Logic|model]] for the theory.
- Complete if it is maximally consistent, that is, if $T$ is consistent, then for all $\phi\notin T$, we have $T\cup\phi$ is inconsistent.
- $S$ is axiomatized by $T$ if $S\models T$ and $T\models S$.

---
# References
- [[First Order Logic]]
- [[Semantics of First Order Logic]]
