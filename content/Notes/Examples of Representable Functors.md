---
tags:
  - Example
---
202505051905

Tags : [[Category Theory]]
# Examples of Representable Functors
---
>[!example] Covariant Functors
>- A set $X$ with an endomorphism $f:X \to X$ and a distinguished element $x_{0}$ (so, can think of pointed sets and a function) is called a discrete dynamical system. This information allows one to look at repeated application of $f$ onto the set as evolution of the point $x_{0}$ discretely with time. Here $\mathbb{N}$ with the function $\text{suc}$ and element $0$ is an intial object of the category. And represents the functor $F$ which applies the function $f$ once on the set.
>- The Identity Functor on the category of sets is represented by the singleton set
>- The forgetful functor $U: \text{Grp}\to \text{Set}$ is represented by $\mathbb{Z}$. So given any set $U(G)\cong \text{Grp}(\mathbb{Z}, G)$, which sends the generator of $Z$ to any element of $G$.
>- For any [[Ring]] $R$, the forgetful functor $U: \text{Mod}_{R} \to \text{Set}$ is represented by by $R$-module $R$.
>- The forgetful functor from $\text{Top}$ to set is represented by the singleton.

---

>[!example] Contravariant Functors
>- The powerset functor $\text{Set}^\text{op} \to \text{Set}$ is represented by $\{ \top,\bot \}$. Where the natural isomorphism is defined by preimage of $\top$.
>- The functor $\mathcal O:\text{Top}^\text{op}\to \text{Set}$ which sends a topolotical space to its set of open sets is represented by the sierpinsky space. A 2-point space with one singleton set being open and the other being close.

---
# References
- [[Representable Functors]]