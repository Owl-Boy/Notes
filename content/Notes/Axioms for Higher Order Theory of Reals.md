---
tags:
  - Note
  - Incomplete
---
202412270212

Tags : [[Set Theory]], [[Logic]]
# Axioms for Higher Order Theory of Reals
---
## Syntax

The following will be used as the syntax for for our language:
- Relations: $\leq, =$
- Functions: $\cdot, +$
- Constants: $\mathbb{0, 1}$
The following convention will be used for variables:
- Real variables : $x, y, z$
- Function variables : $f, g, h$
- Functional variables : $F, G, H$ 
- We also premit equality between 2 functions and 2 variables

Terms will be represented using the following : $t, u, v$

We have Functionals so that we will be allowed to write functions that take more than 1 argument with very few axioms to deal with, it is done by equating a tuple of $n$ numbers with a function that is $0$ on everything except $0..n-1$ and on those numbers it takes obvious values. Then functions on functions like these act like functions with 3 argument.
## Axioms
### Propositional Logic (PL)
Some good enough bunch of tautologies like [[Hilbert Style Proofs]].

### Quantifier Logic (QL)
- $\forall v, A(v) = A(t)$
- $A(t) \implies \exists v,A(v)$

### Equality Logic (EL)
- $t=t$
- $t=u \to A(t)=A(u)$

### Inference  Rules (imagine proof trees)
- (D) $A$ and $A \to B$ prove $B$
- (U) $A \to B(v)$ proves $A \to \forall v, B(v)$
- (E) $B(v) \to A$ proves $\exists v B(v) \to A$

### Ordred Fields (OF)
- We will use the axioms defined in [[Ordered Fields]]

### Total Order (CO)
- $\exists y \forall x [f(x) \leq y] \to \exists z \forall y[z \leq y \leftrightarrow \forall x[f(x)\leq y]]$
	- This statement reads as, for every bounded function, there is a least upper bound.

### Equality of Functions and Functionals (EF)
- (1) $f=g \leftrightarrow \forall x, f(x)=g(x)$
- (2) $F=G \leftrightarrow \forall f, F(f)=G(f)$

### Choice (AC)
- (1) $\forall x \exists y, A(x, y) \to \exists f\forall x, A(x, f(x))$
- (2) $\forall f \exists g, A(f, g) \to \exists F\forall f, A(f, F(f))$

---
# References
[[Failure of CH in a suitable Model]]