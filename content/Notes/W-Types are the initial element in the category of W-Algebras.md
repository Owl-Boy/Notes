---
tags:
  - Note
---
202506171606

Tags : [[Homotopy Type Theory]]
# W-Types are the initial element in the category of W-Algebras
---
Given $A:\cal U$ and $B:A \to\cal U$, let $P(X):\equiv \sum_{a:A}B(a)\to X$ be the associated polynomial functor. Let $W=W_{a:A}B(a)$, then from the construction rule of [[W-Types]] we have $s_{W}:\equiv\text{sup}:PW\to W$.

We now want to show that $(W, s_{W})$ is initial, so consider another $W$-Algebra $(C, s_{C})$ and we show that the hom-type is contractible. First to show that it is inhabited we prove the existence of $(f, s_{f})$

The induction principle of $W$-types let us easily define such a homomorphism. 
Consider $h:B(a)\to W$ which picks out the arguments to the constructor, if we apply $f$ on $h(b)$ for each $b$ we will get that $f(\text{sup}(a, h))=s_{D}(a, f\circ h)$.

Now we need to show that this is a unique isomorphism, that is for any $(g, s_{g}):(W, s_{W})\to (C, s_{C})$ we have 
$$
p:(f, s_{f})=(g,s_{g})
$$
this element $p$ itself will be an element of form $(e, s_{e})$ where $e:f= g$ which is something we get from [[Uniqueness of functions created using induction principle]].

Apparently some [[Pasting Diagram]] bs:
![[Pasted image 20250617162039.png|300]]

---
# References
- [[W-Types]]
- [[Uniqueness of functions created using induction principle]]
- [[Contractible Types]]
- [[Type of W-Algebras]]
- [[Inductive Types are Initial Algebras]]
- [[Pasting Diagram]]
- [[Polynomial Functor]]