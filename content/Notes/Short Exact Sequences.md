---
tags:
  - Note
---
202507031507

Tags : [[Homology Theory]]
# Short Exact Sequences
---
>[!definition]
>A **short exact sequence** is an [[Exact Sequences]] of the following shape:
>$$
>0\longrightarrow L\xrightarrow{\;\alpha\;}M\xrightarrow{\;\beta\;} N\longrightarrow 0
>$$

From [[Epimorphisms and Monomorphisms of Exact Sequences]] we can tell that $\alpha$ must be a [[Monomorphisms and Epimorphisms|Monomorphism]] and $\beta$ must be an [[Monomorphisms and Epimorphisms|Epimorphism]], this from the first isomorphism theorem, we can get that the above exact sequence has the following form:
$$
0\longrightarrow \text{ker}\ \beta\xrightarrow{\;\alpha\;}M\xrightarrow{\;\beta\;} \text{im }\beta\longrightarrow 0
$$
This is because the final homomorphism forces $N$ to be the image of $\beta$, and the first homomorphism forces $\alpha$ to be a monomorphism making $L$ isomorphic to its image, which is equal to the kernel of $\beta$.

In fact every exact sequence can be written as a collection of short exact sequences as follows:
![[Pasted image 20250703153513.png]]
crazy diagram.

---
# References
- [[Exact Sequences]]
- [[Epimorphisms and Monomorphisms of Exact Sequences]]
- [[Split Exact Sequences]]