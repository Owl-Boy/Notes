---
tags:
  - Note
  - Incomplete
---
202412081712

Tags : [[Algebra]], [[Logic]]
# Frames(Algebra)
---
To construct equivalent classes of formulas in [[Geometric Propositional Logic]], we construct a [[Lindenbaum-Tarski Algebra]] for it. This happens to be a *Frame*.

>[!definition]
>A partially ordered set $A$ is a frame iff
>- Every subset has a join.
>- Every finite subset has a meet.
>- Binary meets distributes over join
>
>A homomorphism of frames is a function that preserves the above operations.

>[!note] Equivalences
>Frames are equivalent to [[Heyting Algebra|Complete Heyting Algebras]] which follows from the following propositions.

>[!theorem]
>If $L$ is a [[Lattice]], and every subset of $L$ has a join, then every subset of $L$ also has a meet.
>>[!example] Proof
>>Let $S\subseteq L$ and let $A$ be the set of its lower bounds. A join for $A$ becomes a meet for $S$

The proof shows that every *Frame* is a complete lattice. But existence of joins also implies the presence of relative inverses making it a [[Heyting Algebra]]. 

>[!example] Examples
>- Any finite distributive lattices are frames.
>- If $U$ is a set then $\mathcal P(U)$ is a frame. 
>- $\mathbb 1= \{ \circ \}$ is the inconsistent frame: true = false
>- $\mathbb 2 = \{ \text{false} \leq \text{true} \}$ is called the Sierpinski frame.

---
# References
[[Topological Spaces as Frames]]