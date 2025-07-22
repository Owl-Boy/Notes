---
tags:
  - Example
---
202506171406

Tags : [[Homotopy Type Theory]]
# Type of Natural Number Algebra
---
>[!definition]
>A $\mathbb{N}$-Algebra is a type $C$ with two specified element $c_{0}:C$ and $c_{s}:C \to C$, which is written as:
>$$
>\mathbb{N}\text{Alg} :\equiv \sum_{C:\cal U}C \times (C \to C)
>$$

A morphism here would be a function that respects the specified element and the $c_{s}$ operator.

>[!definition]
>A $\mathbb{N}$-homomorphism between $\mathbb{N}$-algebras $\mathcal C :\equiv(C,c_{0}, c_{s})$ and $\mathcal D:\equiv(D, d_{0}, d_{s})$ is a function  $h$ such that $h\ c_{0}= d_{0}$ and $h(c_{s}\ c)=d_{s}(h\ c)$, so the type of homomorphisms is:
>$$
>\mathbb{N}\text{Hom}(\mathcal C, \mathcal D):\equiv \sum_{h:C\to D} (h\ c_{0}= d_{0}) \times \prod_{c:C}h(c_{s}\ c)=d_{s}(h\ c)
>$$

In this category of $\mathbb{N}$-algebras, we see that [[N is the initial object in the category of N-Algebras]].

We define an Initial obejct to be as follows:
>[!definition]
>$$
>\text{is-H-init}_{\mathbb{N}}(I) :\equiv \prod_{C:\mathbb{N}\text{Alg}} \text{is-contra}(\mathbb{N}\text{Hom}(I, C))
>$$

Which says, the type of functions from $I$ to any other $\mathbb{N}$-algbra is contractibe.

---
# References
