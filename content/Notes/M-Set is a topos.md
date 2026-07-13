---
id: M-Set is a topos
aliases: []
tags:
  - Note
  - Incomplete
---

202607131642

Tags : [[Topos Theory]]

# M-Set is a topos

The category $\text{M-Set}$ is the category of sets equipped with a monoid action, where all morphisms respect the monoid action, that is $f(m* a) = m*f(a)$.

Terminal object is the unique monoid action on the singleton set $(1, \text{id}_1)$.

Products can be defined by taking the product of the underlying sets and applying the action component-wise.

Pullbacks can be defined by defining it on the underlying set, and the monoid action can again be defined componentwise.

Elements of objects in this category are given by left-ideals. Subsets that are closed under the monoid action. We define $\Omega = \{L_M, \omega\}$ where $\omega(m, B)$ is the subset of $M$ that when left multiplied to $m$, takes it to $B$, that is:
$
\omega(m,B) = \{n \mid n * m \in B\}
$

And the function $\top : * \mapsto M$.

To illustrate the working of the sub-object classifier, say we have $(X , \mu) \hookrightarrow (Y, \nu)$, where $x$ is a subset, and the map is inclusion. The character $\chi:(Y, \nu) \to \Omega$ is defined by:
$
\chi(y) = \{m \mid \nu(m, y) \in  X\}
$

To define the exponential object $(Y, \mu)^{(X, \lambda)}$ we consider the set of equivariant maps $f : M \times X -> Y$ (the extra $M$ is precisely to define a monoid action on it.) We define the monoid action as follows $k * f = g : (m, x) |-> f(n * k, x)$. And the evaluation maps sends $(f, x) |-> f(e, x)$.

# References

