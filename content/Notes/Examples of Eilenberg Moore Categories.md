---
tags:
  - Example
---
202508131208

Tags : [[Category Theory]]
# Examples of Eilenberg Moore Categories
---
>[!example]
>Consider the [[Maybe Monad|Free Pointed Set Monad]], an algebra is a set $A$ along with a map $a:A_{+}\to A$ such that the diagrams in [[Eilenberg Moore Category]] commute. The square imposes no additional constraint but the triangle asserts that the map $a$ restricts to the identity on the $A$ component of $A\sqcup \{ * \}$. Thus the data of an algebra is a set with a specified basepoint $a\in A$, the image of extra point $*$ under the map. Morphisms make the obvious diagrams commute. This category is isomorphic to the category of pointed sets.

>[!example]
>Consider the free-forgetful monad between the catgory $\text{Ab}$ of abelian groups and the category $\text{Mod}_{R}$ of modules over a ring $R$. An algebra equips an abelian group with a homomorphism $R \otimes_{\mathbb{Z}}A\to A$ satisfying the axioms in [[Eilenberg Moore Category]]. By the universal property of tensor product, this homomorphism defines a $\mathbb{Z}$-bilinear map $(r, a)\mapsto r\cdot a:R\times A \to A$ which is called the *scalar map* and the commutative diagrams ensure that $1\cdot a=a$ and $r\cdot(r'\cdot a)=(rr')\cdot a$, this an algebra of this monad is precisely an $R$-module.

>[!example]
>An algebra of the [[Free Monoid]] [[List Monad|Monad]] is a set $A$ equipped with a map $\alpha:\coprod_{n\geq{0}}A^n$ whose component function describe an $n$-ary operations on $A^n$ specifying the axioms in the [[Eilenberg Moore Category]].
>- The triangle describes the unary operation as identity.
>- The commutative square denotes that the operator is associative.
>
>The operatory $\alpha_{0}$ picks out an element, which will be the unit. The binary $\alpha_{2}$ defines the monoid product and associativity forces all other $\alpha_{n}$. And also the morphisms in this category correspond to monoid homomorphisms.

---
# References
