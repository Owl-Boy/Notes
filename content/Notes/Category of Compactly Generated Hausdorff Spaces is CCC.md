---
tags:
  - Example
---

202507081231

tags : [[Category Theory]], [[Topology]]

#  Category of Compactly Generated Hausdorff Spaces is CCC
---
let $\text{Top}$ denote the category of [[Compactness|Compactly generated]] [[Separation Axioms|Hasudorff Spaces]] with continuous functions. Here the [[Two Variable Adjunction]] specializes to form the following adjunction
![[Pasted image 20250708123431.png|200]]
where $S^{1}$ is the unit circle. The space $\text{Map}(S_{1},X)$ is the space of loops in $X$.

The slice category of $\text{Top}$ defines a convenient category $\text{Top}_{*}$ of based compactly generated hausdorff spaces and it admits the following 2 variable adjunction:
$$
\begin{align}
\text{Top}_{*}\times \text{Top}_{*}&\xrightarrow{\wedge}\text{Top}_{*} \\
\text{Top}_{*}^\text{op}\times\text{Top}_{*}&\xrightarrow{\text{Map}_{*}} \text{Top}_{*} \\
\text{Top}_{*}^\text{op}\times\text{Top}_{*}&\xrightarrow{\text{Map}_{*}} \text{Top}_{*}
\end{align}
$$
Where $\text{Map}_{*}((X, x),(Y,y))$ denote the basepoint-preserving continuous functions $(X,x)\to(Y,y)$ and the bifunctor $\wedge$ is called the [[Smash Product]].

The space 
$$
\Omega X:= \text{Map}_{*}(S^1,(X, x))
$$
is called the [[Loop Space|based loop space]] on $(X,x)$. The left adjoint of this functor $\Sigma X:= S_{1} \land X$ constructs the reduced suspension of based space $(X,x)$. This defines the $\text{loops}\dashv\text{suspension}$ [[Adjunctions|adjunction]].
![[Pasted image 20250708124702.png|400]]


---
# Related
- [[Separation Axioms]]
- [[Compactness]]
- [[Smash Product]]
- [[Loop Space]]
- [[Adjunctions]]