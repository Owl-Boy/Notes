---
tags:
  - Note
---
202508181208

Tags : [[Homotopy Type Theory]]
# Free Group
---
The [[Free Monoid]] can be defined as a simple [[Inductive Types|inductive type]] because every element of a fee monoid has a computable canonical representation, this is not true for groups, in fact the equality of words is [[Proof for the Undecidability of the Word Problem|undecidable]]. The group axioms can be encoded in higher inductive types to create a free group construction:


>[!definition]
>Given a type $A$, the higher inductive type $F(A)$ is defined using the following generators:
>- A function $\eta:A\to F(A)$
>- A function $m:F(A)\times F(A)\to F(A)$
>- An element $e:F(A)$
>- A function $i:F(A)\to F(A)$
>- For each $x,y,z:F(A)$, an equality $m(x,m(y,z))$
>- For each $x:F(A)$ equalities $m(x,e)=x$ and $m(e,x)=x$
>- For each $x:F(A)$ equalities $m(x, i(x))=e$ and $m(i(x),x)=e$
>- The $0$-truncation constructor: for any $x, y:F(A)$ and $p,q:x=y$ we have $p=q$.

It is now straightforward to prove that
>[!theorem]
>Given a set $A$, the type $F(A)$ defines the [[Free Group]] on $A$, that is we have the equivalence
>$$
>F(A)\to_{\text{Grp}}G\cong (A\to G)
>$$
>where $\to_{\text{Grp}}$ denotes the type of group homomorphism.

Given an function $f:A\to G$ we construct $\bar{f}:F(A)\to G$, where the rule is $\bar{f} \circ \eta \equiv f$ and $\bar{f}$ is a group homomorphism. Thus from left to right we have $(-\circ\eta):(F(A)\to_{\text{Grp}}G)\to(A\to G)$, the previous statement also says that this has a left inverse, and it is easy to show that the left inverse is also the right inverse.

---
# References
- [[Free Group]]
- [[Proof for the Undecidability of the Word Problem]]
- [[Inductive Types]]
- [[Higher Inductive Types]]
- [[Functions as Equivalences]]