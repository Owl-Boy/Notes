---
tags:
  - Note
---
202509041609

Tags : [[Category Theory]]
# Monadicity Theorem
---
>[!theorem]
>A [[Adjunctions|Right Adjoint Functor]] $U:D\to C$ is [[Monadic Functors|monadic]] iff it [[Preservation, Reflection and Creation of Limits|creates]] [[U-split Coequalizer|coequalizers of u-split pairs]].

And  by [[Monadic forgetful functors strictly create coequalizers of Usplit pairs]], we get the following way of phrasing the theorem:
The following are equivalent:
1. $K$ is an equivalence of categories
2. $U$ creates coequalizer of $U$-split pairs.
with respect to the following diagram:
![[Pasted image 20250904164335.png|250]]

---
Where  [[Monadic forgetful functors strictly create coequalizers of Usplit pairs]] is precisely the part 1 $\to$ 2.

Now we assume 2. and use it to construct an inverse equivalence $L$ to $K$. Note that $U^TK=U$ and $KF=F^T$ so to define an inverse to $K$ we would want $UL\cong U^T$ and $LF^T\cong F$.

We define $L(TA, \mu_{A}):= FA$. and define $L$ to carry the free maps across to the free maps. Now we need to define it for non-free Algebras. 

Since an [[Equivalences Reflect, Preserve and Create Colimits|equivalence preserves limits and colimits]], For any algebra, we can define $L(A, \alpha)$ to be the following equalizer:
$$
FUFA \underset{\epsilon_{FA}}{\overset{F{\alpha}}\rightrightarrows}FA \twoheadrightarrow L(A, \alpha)
$$
We have that $FUFA\rightrightarrows FA$ form a split coequalizer, so by hypothesis the coequalizer exists, and we also have the image of maps between $(A, \alpha)$ and $(B, \beta)$. And by [[Choosing Limits of diagrams in Functorial]], we get that this definition is functorial. 

Since $U^T$ strictly creates coequalizer of $U^T$-split pairs we have that $KL\cong 1_{C^T}$. Now we need to prove that $LK\cong 1_{D}$.

Given an object $D$, we define $LKD$ to be the coequalizer of the pair 
$$
FUFUD \underset{\epsilon_{FUD}}{\overset{FU\epsilon_{D}}\rightrightarrows}FUD
$$
And so it must be isomorphic to the coequalizer in [[Left Adjoint in a monadic adjunction create coequalizers]], thus we get the natural isomorphism. 

---
# References
- [[Adjunctions]]
- [[Monadic Functors]]
- [[U-split Coequalizer]]
- [[Equivalences Reflect, Preserve and Create Colimits]]
- [[Choosing Limits of diagrams in Functorial]]
- [[Left Adjoint in a monadic adjunction create coequalizers]]