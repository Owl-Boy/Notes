---
tags:
  - Note
---
202507221607

Tags : [[Homotopy Type Theory]]
# Making Spheres using suspension
---
>[!theorem]
>$$
>\Sigma2 \simeq \mathbb S^1
>$$

We first define $f:\Sigma 2\to\mathbb S^1$ by recursion such that
- $f(N):\equiv\text{base}$
- $f(S):\equiv\text{base}$
- $f(\text{merid}(0_{2})):\equiv\text{loop}$
- $f(\text{merid}(1_{2})):\equiv\text{refl}_{\text{base}}$

Now we need to define its inverse, for that we have $g:\mathbb S^1\to \Sigma2$ such that 
- $g(\text{base}):\equiv N$ 
- $g(\text{loop}):\equiv\text{merid}(0_{2})\cdot\text{merid}(1_{2})^{-1}$. 

We now show that $f$ and $g$ are quasi inverses.

It is easy to show that $g(f(x))=x$ by induction
- if $x\equiv N$ we have $g(f(N))\equiv N$ so we can just use $\text{refl}_{N}$
- if $x\equiv S$ we have $g(f(S))\equiv N$ so we can use $\text{merid}(1_{2}):g(f(S))=S$.

And we are now left to show that for all $x:\mathbf 2$ we have 
$$
\text{refl}_{N}=_{\text{merid}(x)}^P\text{merid}(1)
$$
which because of [[Transports in a Family of Paths]] becomes 
$$
g(f(\text{merid}(x)))^{-1}\cdot\text{refl}_{N}\cdot\text{merid}(x) = \text{merid}(1)
$$
We now do induction of $\mathbf{2}$
When $x\equiv 0_{2}$
$$
\begin{align}
g(f(\text{merid}(0_{2})))^{-1}&\cdot\text{refl}_{N}\cdot\text{merid}(0) \\
&=g(\text{loop})^{-1}\cdot\text{merid}(0) \\
&= (\text{merid}(0_{2})\cdot\text{merid}(1)^{-1})^{-1} \cdot\text{merid}(0) \\
&= \text{merid}(1)
\end{align}
$$
And when $x\equiv 1$ we have
$$
\begin{align}
g(f(\text{merid}(1_{2})))^{-1}&\cdot\text{refl}_{\text{N}}\cdot\text{merid}(1_{2}) \\
&= \text{refl}_{N}^{-1} \cdot \text{merid}(1_{2}) \\
&= \text{merid}(1_{2})
\end{align}
$$
Now we need to show that $f(g(x))=x$. We can show that $f(g(\text{base}))\equiv\text{base}$, so we can map $\text{base}$ to $\text{refl}_{\text{base}}$. For $\text{loop}$ to show that:
$$
f(g(\text{loop})) \cdot \text{refl}_{\text{base}} \cdot \text{loop} = \text{refl}_{\text{base}}
$$
But we have that $f(g(\text{loop}))=\text{loop} \cdot\text{refl}_{\text{base}}$ so its straightforward.

---
# References
- [[Suspensions (HoTT)|Suspensions]]
- [[Circle (HoTT)|Circle]]
- [[Transports in a Family of Paths]]