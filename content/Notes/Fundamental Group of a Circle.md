---
tags:
  - Note
---
202511050011

Tags : [[Homotopy Type Theory]]
# Fundamental Group of a Circle
---
We will show that $\pi_{1}(S_{1})=\mathbb{Z}$. In order to do so, we will show a stronger statement $\Omega_{1}(S_{1})=\mathbb{Z}$, and from that we will get that $\pi_{1}(S_{1})=\|Z\|_{0}$ but since $\mathbb{Z}$ is a set, we have what we want.

Using [[Elimination Principles of Integers]], we define a function to the loop space of $S_{1}$. We define $\text{loop}^-:\mathbb{Z}\to\text{base}=\text{base}$ intuitively by
$$
\text{loop}^n = 
\begin{cases}
\underbrace{\text{loop} \bullet   \text{loop} \bullet \dots \bullet \text{loop}}_{n\text{-times}} & \text{if } n>0\\
\underbrace{\text{loop}^{-1} \bullet   \text{loop}^{-1} \bullet \dots \bullet \text{loop}^{-1}}_{-n\text{-times}} & \text{if } n<0 \\
\text{refl}_{\text{base}} & \text{if }n=0
\end{cases}
$$

To define the reverse direction, note that the successor function $\text{suc}:\mathbb{Z}\to \mathbb{Z}$ is an equivalence, hence it induces the path $\text{ua}(\text{suc}):\mathbb{Z}=\mathbb{Z}$ in the universe $\cal U$. Thus, by recursion principle of $S_{1}$ we have a map $c:S_{1}\to \mathcal U$ such that $c(\text{base})=\mathbb{Z}$ and $\text{ap}_{c}(\text{loop})=\text{ua}(\text{suc})$, thus we have $\text{ap}_{c}:(\text{base}=\text{base})\to(\mathbb{Z}=\mathbb{Z})$ and we define $g(p):\equiv\text{transport}^{X\mapsto X}(\text{ap}_{c}(p),0)$.

Using the induction principle, it is easy to show that $g(\text{loop}^n)=n$ using the induction principle of integers. The other direction, where $\text{loop}^{g(p)}=p$ is harder to prove. The standard idea of path induction does not work as both end point are fixed.

---
# References
- [[Fundamental Group]]
- [[Homotopy Group(HoTT)]]
- [[Elimination Principles of Integers]]
- [[Transport]]