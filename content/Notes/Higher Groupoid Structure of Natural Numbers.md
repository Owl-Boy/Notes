---
tags:
  - Note
---
202505072305

Tags : [[Homotopy Type Theory]]
# Higher Groupoid Structure of Natural Numbers
---
We will use the encode-decode method as was shown in [[Higher Groupoids Structure of Coproducts]] for natural number. Here, instead of fixing and endpoint we characterize all paths together
$$
\text{code}: \mathbb{N} \to \mathbb{N} \to \cal U
$$
defined by double recursion as
$$
\begin{align}
\text{code}(0,0) &:\equiv \mathbf{1} \\
\text{code}(\text{succ}(m), 0) &:\equiv \mathbf{0}\\
\text{code}(0,\text{succ}(n)) &:\equiv \mathbf{0} \\
\text{code}(\text{succ}(m), \text{succ}(n)) &:\equiv \text{code}(m, n).
\end{align}
$$
We also define a recursive dependent function $r:\prod_{n:\mathbb{N}}\text{code}(n,n)$
$$
\begin{align}
r(0) &:\equiv \star \\
r(\text{succ}(n)) &:\equiv r(n)
\end{align}
$$
We now have that for any $m, n: \mathbb{N}$ we have $(m=n) \simeq \text{code}(m, n)$.
To prove this, we define the encode and decode functions

$$
\text{encode}:\prod_{m,n:\mathbb{N}} (m=n) \to \text{code}(m, n)
$$
We can define this using transport as
$$
\text{encode}(m, n, p) :\equiv \text{transport}^{\text{code}(m, -)}(p, r(m))
$$
So take $m,n$, then $p:m=n$ and then we start with an element of $\text{code}(m,m)$ and transport it to $\text{code}(m, n)$.

Now we define 
$$
\text{decode}: \prod_{m,n:\mathbb{N}}\text{code}(m, n) \to (m=n)
$$
We do this by a double induction on $m$ and $n$, when both are $0$ we need a function $\mathbf{1} \to (0=0)$, which sets $\star \to \text{refl}_{0}$. When one of them is a successor, and the other one is $0$ we can have co-domain to be $\mathbf{0}$ too. When both of them are successors we can define it as:
$$
\begin{align}
\text{code}(\text{succ}(m), \text{succ}(n))\equiv\ &\text{code}(m, n)  \\
{}\xrightarrow{\text{decode}(m, n)}&(m=n) \\
{}\xrightarrow{\text{ap}_{\text{succ}}}&(\text{succ}(m)=\text{succ}(n))
\end{align}
$$

We now need  to show that these are quasi inverses. First by induction on $\text{p}$ we get for each $n$ we need to show.
$$
\text{decode}(n,n, \text{encode}(n,n,\text{refl}_{n}))= \text{refl}_{n}
$$
But we have that $\text{encode}(n,n,\text{refl}_{n})\equiv r(n)$ so we need to show $\text{decode}(n,n,r(n))= \text{refl}_{n}$. This can be done by induction on $n$. We have it for $n=0$ by definition. And for the induction step we apply $\text{ap}_{\text{ap}_{n}}$.

For the other direction we start by doing double induction on $m$ and $n$. If both are $0$ then $\text{decode}(0,0, c)\equiv \text{refl}_{0}$ and $\text{encode}(0,0, \text{refl}_{0})\equiv \star$. If $m=0$ and not $n$, or the other way round we get $c:\mathbf{0}$ so we are done.

In the final case we have 
$$
\begin{align}
\text{encode}&(\text{succ}(m), \text{succ}(n), \text{decode}(\text{succ}(m), \text{succ}(n), c)) \\
&=\text{encode}(\text{succ}(m), \text{succ}(n),\text{ap}_{\text{succ}}(\text{decode}(m,n,c))) \\
&= \text{transport}^{\text{code}(\text{succ}(m),-)}(\text{ap}_{\text{succ}}(\text{decode}(m,n,c)), r(\text{succ(m)})) \\
&= \text{transport}^{\text{code}(\text{succ}(m),\text{succ}(-))}(\text{decode}(m,n,c)), r(\text{succ(m)})  \\
&= \text{transport}^{\text{code}(m,-)}(\text{decode}(m,n,c)), r(m)  \\
&= \text{encode}(m,n, \text{decode}(m, n, c)) \\
&=c
\end{align}
$$


---
# References
- [[Higher Groupoids Structure of Coproducts]]
- [[Transport]]