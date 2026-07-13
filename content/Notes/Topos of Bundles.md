---
id: Topos of Bundles
aliases: []
tags:
  - Note
  - Incomplete
---

202607131414

Tags : [[Topos Theory]]

# Topos of Bundles

Consider a set $I$ and a collection of disjoint sets indexed by $I$, $\mathcal{A} = \{A_i \mid i \in I\}$. Since of of these sets are disjoint, a nice visualization for this is imagining $I$ as the ground and for each element $i$ of $I$ there is a set $A_i$ "sitting over it".

We can define $A = \bigcup \mathcal{A}$, so we can define a function $p: A -> I$ that sends elements from $A_i$ to $i$. Thus $A_i$ can also be thought of as $p^{-1}(\{i\})$.

The set $A_i$ is called the *stalk* or *fibre* over $i$ and the members of $A_i$ are called the *germs* at $i$. We call $\mathcal A$ the *bundle* of sets over $I$ and $A$ the *stalk space* of the bundle.

To define a map between bundles $\mathcal{A}$ and $\mathcal{B}$, for each $i$, one needs to define a map between $A_i$ and $B_i$, but another way to look at it is, to define a map between $p_A$ and $p_B$, we need a map $f : A \to B$ such that $p_A = f \triangleright p_B$. And so we see that the category of bundles is equivalent to $\text{Set} \downarrow I$

The *terminal object* in the category of bundles is the identity map $I \to I$.

Pullbacks in the category of bundles correspond to pullbacks in the category of sets.

The sub-object classifier is the map $\pi_2 : \{0, 1\} \times I \to I$. Note that the truth values form the powerset of $I$.

Note that a function from $I$ to $A$ will pick out 1 element from each stalk in $A$, and is called a section. These correspond to the  elements of a set.

Products in this category correspond to pullbacks in the category of sets.

The bundle interpretation makes it easy to define a lot of other construction, for example the exponential objects can be described fibre-wise too.

# References

- [[Set is a topos]]

