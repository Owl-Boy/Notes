---
tags:
  - Example
---
202508122308

Tags : [[Category Theory]], [[Linear Algebra]]
# Affine Spaces as Monads
---
>[!definition]
>Given a vector space $V$ over a $\mathbb k$, an **affine space** is a non-empty set $A$ together with a _translation_ function $V\times A \xrightarrow+A$. so that.
>- $\vec{0}+a=a$ for all $a:\text{A}$;
>- $(\vec{v}+\vec{w})+a=\vec{v}+(\vec{w}+a)$
>- for any $a\in A$ the function $- + a:V\to A$ is a bijection.

The following is a way to describe **affine spaces** without having to define an ambient vector space. If one temporarily fixes an origin $o:A$ then for any pair of elements $a,b:A$ and any scalar $k:\mathbb k$, we can use the bijection $- +o$ and we get that there is a unique $c:A$ such that
$$
c-o = k(a-o) +(1-k)(b-o)
$$
and we can now denote this element $c$ as $ka + (1-k)b$ independent of the choice of $o$. We can analogously define **affine linear combinations** of $\lambda_{1}a_{1}+\lambda_{2}a_{2}\dots \lambda_{n}a_{n}$ if $\sum\lambda_{i}=1$. This leads to the following equivalent definition.

>[!definition]
>An **affine space** is a non-empty set $A$ in which linear combinations can be evaluated.

To formalise this in the category of sets, we can do the following procedure:
- Given a set $A$ we consider the set $\text{Aff}_{\mathbb k}(A)$ to be the set of all formal affine linear combinations of elements of $A$.
- A function $\text{ev}_{A}:\text{Aff}_{\mathbb k}(A) \to A$ which evaluates an affine linear combination using the above definition.
- A function $\eta_{A}:A \to\text{Aff}_{\mathbb k}(A)$ which is the singleton function.
- A function $\mu_{A}:\text{Aff}_{\mathbb k}(\text{Aff}_{\mathbb k}(A))\to \text{Aff}_{\mathbb k}(A)$ which is the distribution function such that the following laws are satisfied.
- ![[Pasted image 20250813014020.png|500]]
Where the first diagram says that $\eta_{A}:a\mapsto 1 \cdot a$. and the second diagram distributes affine linear combinations of affine linear combinations to a single affine linear combination. This we get that:
>[!definition]
>An **affine space** is an **algebra** for the affine linear combination [[Monads and Comonads|monad]].

---
# References
- [[Monads and Comonads]]