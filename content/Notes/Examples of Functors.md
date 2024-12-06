---
tags:
  - Note
  - Incomplete
---
202411121911

Tags : [[Category Theory]]
# Examples of Functors
---
A Functor consists of a mapping of objects and a mapping of morphisms that preserves all of the structure of categories. namely domain, codomain, composition and identities.

## Covariant Functors

- There is an *endofunctor* $P: Set \to Set$ that sends a set $A$ to its power set and a function $f: A \to B$ to its direct-image function $f_{*}:PA \to PB$
- Most Algebraic (and other) object that are sets with other operations and restrictions on it have a *forgetful functor* from their category to the category of sets, where each element is mapped to its base set.
- The *fundamental group* is a functor from category of Topological spaces to the category of groups, that sends continuous functions to group homomorphisms.

## Contravariant Functor

- The functor $(-)^\text{op}: \text{CAT} \to \text{CAT}$ defines a non-trivial automorphism of categories of categories.
- For any topological space $X$, there is a contravariant functor isomorphism of poset categories $O(X) \cong C(X)^\text{op}$ that associates an open subset of $X$ to its closeed complement.

---
# References
