---
tags:
  - Note
---
202510200010

Tags : [[Category Theory]]
# The category Group is cocomplete
---
Consider the monadic forgetful functor $U:\text{Group}\to\text{Set}$, both of which admit coproducts, in set the coproducts are disjoint unions while in $\text{Group}$ it is the free product. The functor $U$ does not respect coproducts.

A first approximation to the free product is the set $F(UG\sqcup UH)$, the free group on the disjoint union of elements of $G$ and $H$. Now we need to impose relation on the group which we get from words in $G$ and words in $H$. The words in $G$ are $UFUG$ and the words in $H$ are $UFUH$. Free group on this set is given by $F(UFUG \sqcup UFUH)$, which is the group of all words that exclusively contains elements of $H$ or elements of $G$.

To encode the relation, we define a natural pair of group homomorphisms:
![[Pasted image 20251020005926.png]]

$G$ and $H$ being groups is encoded by the pair of homomorphism $\epsilon_{G}:FUG\to G$ and $\epsilon_{G}:FUH\to H$. The top map sends a word to the group element that it represents. 

The map $\kappa:(UFA+UFB)\to UF(A + B)$ where $A,B:\text{Set}$ is defined to the canonical map, defined using the universal property of coproducts.

The bottom composite takes a word of subwords, from $G$ or $H$ exclusively, and concatenates them together. Thus, the coequalizer precisely describes the free product of $H$ and $G$.


---
# References
- [[Coproducts in Category Theory]]
- [[Monads and Comonads]]
- [[Complete and Cocomplete Categories]]
- [[Category of Models for an Algebraic Theory]]