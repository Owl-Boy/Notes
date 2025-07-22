---
tags:
  - Note
---
202507031607

Tags : [[Homology Theory]]
# Snake Lemma
---
Consider 3 [[Short Exact Sequences]] liked together by homomorphisms as follows:
![[Pasted image 20250703164014.png|350]]
Then we get the following:
>[!lemma]
>There is an exact sequence as follows:
>$$
>0 \rightarrow \text{ker }\lambda \rightarrow \text{ker }\mu\rightarrow \text{ker }\nu\xrightarrow{\delta}\text{coker }\lambda \rightarrow \text{coker }\mu \rightarrow \text{coker }\nu\rightarrow 0
>$$

This lemma is proving using the construction of the following diagram:
![[Pasted image 20250703165014.png|400]]
this makes it straightforward to see the non-$\delta$ transitions. We now need to define the homomorphism $\delta$.

To do so, consider an element $a:\text{ker }\nu$, and now consider the following:
![[Pasted image 20250703165727.png|400]]
- $a$ maps to a unique element in $N_{1}$.
- $\beta_{1}$ is surjective, so there $\exists c:M_{1}$ which maps to $b$.
- We defien $d=\mu(c)$
- Note that $b$ maps to $0$ under $\nu$ as it belongs to its kernel. That would mean that $d$ maps to $0$ under $\beta_{0}$ and hence would lie in the kernel of $\beta_{0}$ and hence in the image of $\alpha_{0}$. But $\alpha_{0}$ is a monomorphism hence we can uniquely pick $e$.
- We can now set $f$ to be the image of $e$

We now show that the choice of $c$ does not matter. Suppose we pick a different $c'$ then consider the element $c'-c$ in $M_{1}$. Since the image of $c'-c$ is $b-b=0$, there is an inverse of $c'-c$ in $\alpha_{1}$, which is later mapped to $0$ is $\text{coker}\ \lambda$.

as in the following diagram;
![[Pasted image 20250703170936.png|350]]
So we get  that even for a different choice of $c$ our $f$ if the same. So $\delta$ is well defined!

---
# References
- [[Short Exact Sequences]]
- [[Monomorphisms and Epimorphisms]]