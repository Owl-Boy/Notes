---
tags:
  - Note
  - Incomplete
---
202505221405

Tags : [[Category Theory]]
# Limits in the Category of Sets
---
>[!example]
>Consider a product of a set of sets indexed by $J$. This corresponds to the set of cones over the image with apex $\mathbf{1}$. This is simply one element from each set. Hence aligns with the usual notion.

>[!example]
>Given a parallel pair of functions $f, g:X \rightrightarrows Y$, then their equalizer is the set of maps $1\to X$ which simply picks an element from $X$ such that $f(x)=g(x)$, this also nicely corresponds to
>$$
>\{ x:X \mid f(x)=g(x) \}
>$$

>[!Example]
>Given a diagram of shape $\omega^\text{op}\to \text{Set}$ the cones are a sequence of elements $(x_{n}\in F_{n})$ which makes each triangle commute.:
>![[Pasted image 20250522144642.png]]
>This the limit cone is:
>$$
>\left\{(x_{n})_{n} \in \prod_{n}F_{n} \mid f_{n, n-1}(x_{n})=x_{n-1}  \right\}
>$$

>[!example]
>Elements of the pullback are the cones over the diagram $B \xrightarrow f A \xleftarrow g C$ with apex $\mathbf{1}$, that is the following diagram commutes:
>![[Pasted image 20250522145105.png|200]]
>Hence the apex can be described as:
>$$
>B \times_{A} C = \{ (b, c) \in B \times C \mid f(b) = g(c) \}
>$$

>[!example]
>Given a left G-set $X: \text{B}G \to\text{Set}$ is the set of cones with summit $\mathbf{1}$. A map $x:\mathbf{1} \to X$ defines a cone over $X$ iff the following diagram commutes:
>![[Pasted image 20250522223001.png|200]]
>Which gives exactly the set of fixed points under $g_*$ for all $g$ in $G$


---
# References
