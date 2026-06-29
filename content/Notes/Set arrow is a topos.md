---
id: Set arrow is a topos
aliases: []
tags:
  - Example
---

202606291734

tags : [[Topos Theory]]

#  $\text{Set}^\to$ is a topos

---

Objects in $\text{Set}^\to$ are arrows in set, and given maps $f, g$ as objects, morphism between them are given by a pair of set-morphisms $\langle i, j \rangle$ that make the following diagram commute.

![[set-arr-mor.svg]]

The terminal object in this category is the identity on $*$.

A pullback between objects $f,g,h$ (all coming out of the screen) is given using the cube:

![[set-arr-pullback.svg]]

We define sub-objects of functions by restricting their domain and codomain. This results in 3 cases that need to be dealt with:
- Elements that go from withing the restriction in domain to codomain.
- Elements that go from outside retriction in domain to restriction in codomain
- Elements that go from outside the restriction in domain to outside th restriction in codomain

Note that we always want elements in the restriction of domain to map to restriction of codomain, otherwise the function won't be defined, we put that as a restriction on sub-objects.

So given $f:A \to B$ and $g : C\to D$, we get the sub-object classifier diagram as:

![[set-arr-subobj.svg]]

Here the base of the cube is the sub-object classifier.

To define **exponentiation** between objects $f:A \to B$ and $g : C\to D$ we get $g^f : E\to F$ where $F : D^B$ and $E$ is the $\text{Hom}(f, g)$, where $g^f(h, k) = k$

We define the evaluation arrow $g^f \times f \to g$ as  the pair $\langle u, v$

![[set-arr-exp.svg]]

Where $v$ is the usual evaulation arrow and $u$ takes input $((h, k), x)$ and returns $h(x)$.

---

# Related
[[Elementary Topos]]
