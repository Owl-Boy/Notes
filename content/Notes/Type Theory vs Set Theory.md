---
tags:
  - Note
  - Incomplete
---
202503220503

Tags : [[Homotopy Type Theory]]
# Type Theory vs Set Theory
---
Type Theory is an alternative to [[Set Theory]]. While being another "theory of collections" it different from set theory in a bunch of different ways.

### Layers

Set theory is 2 layered:
- First Order Logic
- Inside First Order Logic, there are the Set theory axioms and everything that can be derived using those
So Set theory is not just the theory of sets, but also about the other primitive: propositions, and how they are used to work with sets.

Type Theory is its own deductive system and does not require an ambient logic to work in. It has 1 basic notion: type. Propositions are identified with types, this is shown [[Correspondence between Types and Sets and Homotopies]], the activity of finding a proof becomes equivalent to constructing an element of the set.

### Types give structure to elements

Another difference is that in set theory, membership is a relation that may or may not hold between 2 objects, while in type theory, one cannot talk about an object in isolation, in a sense, all quantifiers need to be bounded by a type. This restriction is useful because types function as specification of the objects, if $p:A \times B$, then we know that $p$ is a tuple of 2 types $A$ and $B$ and exactly how to decompose $p$.

### Equality
In set theory, equality between 2 sets is a proposition, which means that both the terms being talked about in the proposition correspond to the same set in any model for the logic.

In type theory, equality, like all other propositions is a type, so consider $a, b:A$, we have a type $a=_{A} b$. When this type in inhabited, we say $a, b$ are (propositionally equal).

There is also a need for judgmental equality, or definitional equality and is written as $a \equiv b:A$. This is not a type, this is the judgement that the two elements $a, b$ are by definition the same

---
# References
