---
tags:
  - Note
---
202510050210

Tags : [[Homotopy Type Theory]]
# $n$-truncated functions
---
>[!definition]
>A function $f:A\to B$ is called $n$-truncated if every fiber of $f$ is an [[n-Types]], that is
>$$
>\text{is-n-truncated}(f:A\to B) :\equiv \prod_{b:B} \text{is-n-type}(\text{fib}_{f}(b))
>$$

In particular $-2$-truncated functions are [[Functions as Equivalences|Equivalences]]. This also gives a way to define these using recursion:

>[!definition]
>A function $f:A\to B$ is said to be $(n+1)$-truncated if the function $\text{ap}_{f}$ is $n$-truncated for all $x=y$, that is:
>$$
>\text{is-(n+1)-truncated}(f):\equiv \prod_{x,y:A}\text{is-n-truncated}(\text{ap}_{f,x,y})
>$$
>where $\text{ap}_{f,x,y}$ is $\text{ap}_{f}$ with the domain being $x=y$.

These 2 definitions happen to be equivalent, as stated below

>[!lemma]
>The above 2 definitions are equivalent

To show that, first consider $(x,p),(y, q):\text{fib}_{f}(b)$ for some $b:B$. 
$$
\begin{align}
((x,p)=(y,q)) &= \sum_{r:x=y}p=\text{ap}_{f}(r)\cdot q \\
 & = \sum_{r:x=y}\text{ap}_{f}(r)=p \cdot q^{-1} \\
 & =\text{fib}_{\text{ap}_{f}}(p \cdot q^{-1})
\end{align}
$$
assuming $\text{fib}_{\text{ap}_{f}}$ is an $n$-type for every path in $B$, we get that $\text{fib}_{f}$ is an $(n+1)$-type for every $b:B$. To show it in the other direction, choose $b:\equiv f(y)$ and $q:\equiv\text{refl}_{b}$.

With these 2 statements, we get that the path space of fibre-space(total space) is the fibre-space(total space) of the paths space, proving the equivalence of the two definitons.


---
# References
- [[n-Types]]
- [[Fibers (HoTT)]]
- [[Functions as Equivalences]]