---
tags:
  - Example
---
202507211607

Tags : [[Category Theory]]
# Constructing the Left Adjoint of Inclusion Functor from Ring to Rng
---
The categories $\text{Ring}$ and $\text{Rng}$ are locally presentable and the inclusion is accessible. So by [[Adjoint Functor Theorem for locally presentable categories]] the left adjoint to the inclusion $\text{Ring}\hookrightarrow\text{Rng}$ exists.

The inclusoin $\text{Ring}\hookrightarrow\text{Rng}$ commutes with the underlying abelian group functor.
![[Pasted image 20250721162615.png|350]]

Thus, by [[Composition of Adjunctions]], we have that the left adjoint must also commute with the corresponding free functors upto natural isomorphism.

A seen in [[Examples of Free-Forgetful Adjoint Pairs]], the free unital ring on abelian groups is the graded ring $\bigoplus_{n\geq 0}A^{\otimes n}$. Similarly the non-unital ring on $A$ is $\bigoplus_{n>0}A^{\otimes n}$. Commutativity of left adjoint tells us that the free unital ring is constructed by adjoining a copy of $A^{\otimes 0}:=\mathbb{Z}$ and using the componentwise addition and graded multiplication in the graded ring to define the ring structure.

Since any non-unital ring is a coequalizer of a pair fo maps between free non-unital rings. By [[RAPL|LAPC]], we can see that $R^*$ is coequalizer is the images of those maps between the corresponding free unital rings. Thus $R^*\cong \mathbb{Z} \oplus R$ and its easy to verify that addition is component wise, while multiplicatoin is defined as follows :
$$
(n,r)\cdot(n',r')= (nn', n'r + nr' + rr')
$$


---
# References
- [[Adjoints of Inclusion functor from Ring to Rng]]
- [[Adjoint Functor Theorem for locally presentable categories]]
- [[Composition of Adjunctions]]
- [[Examples of Free-Forgetful Adjoint Pairs]]
- [[RAPL]]