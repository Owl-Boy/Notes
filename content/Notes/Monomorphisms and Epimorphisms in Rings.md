---
tags:
  - Note
  - Incomplete
---
202505161205

Tags : [[Ring Theory]]
# Monomorphisms and Epimorphisms in Rings
---
>[!lemma]
>For a Ring homomorphisms $\varphi: R \to S$, the following are equiavalent:
>1. $\varphi$ is a monomorphism
>2. $\text{ker}(\varphi) = \{ 0 \}$
>3. $\varphi$ is an injection (as a set function)

$3 \Leftrightarrow 2$ is trivial, also $3 \Rightarrow 1$.
For $1 \Rightarrow 2$, assume $\varphi$ is a monomorphism and let $r\in \text{ker}(\varphi)$.
Now consider the homomorphisms $\text{ev}_{r}, \text{ev}_{0}:\mathbb{Z}[x] \to R$ such that $\text{ev}_{r}(x)=r$ and $\text{ev}_{0}(r)=0$ and consider the following;
$$
\mathbb{Z}[x]\underset{\text{ev}_{0}}{\overset{\text{ev}_{r}}\rightrightarrows} R\xrightarrow{\varphi} S
$$
If $\text{ev}_{r} \neq \text{ev}_{0}$, we should have that $\varphi \circ \text{ev}_{r}\neq\varphi \circ \text{ev}_{0}$, But that does not hold as $\text{ev}_{r}(r)=\text{ev}_{0}(r)$, which is a contradiction, hence $r=0$.

>[!lemma]
>There are epimorphisms which are not surjections

Consider the map $\iota:\mathbb{Z} \hookrightarrow \mathbb Q$, which is inclusion homomorphism.

And consider the pair of parallel homomorphisms:
$$
\mathbb{Z} \overset \iota\hookrightarrow \mathbb Q \underset{\alpha_{2}}{\overset{\alpha_{1}}\rightrightarrows} R
$$
such that $\alpha_{1}$ and $\alpha_{2}$ agree on $\mathbb{Z}$. Then they must agree on $\mathbb Q$ becuase:
$$
\alpha_{i}\left( \frac{p}{q} \right) = \alpha_{i}(p)\alpha_{i}(q)^{-1}=\alpha(p)\alpha(q)^{-1}
$$

>[!theorem]
>A morphism in $\text{Ring}$ can be both a monomorphism and an epimorphism without being an isomorphism.

---
# References
[[Monomorphisms and Epimorphisms]]
