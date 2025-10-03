---
tags:
  - Note
---
202509242309

Tags : [[Homotopy Type Theory]]
# n-connected functions induce equivalence of n-types
---
>[!lemma]
>If $f:A\to B$ is $n$-connected, then it induces an equivalence $\|A\|_{n}\simeq\|B\|_{n_{0}}$

Left-to-right side of the equivalence is simply $\|f\|_{n}:\|A\|_{n}\to\|B\|_{n}$.

We now need to construct an inverse $g:\|B\|_{n}\to\|A\|_{n}$. By universal property of truncations, we only need to construct a function of type $B\to\|A\|_{n}$.

We get the following function
$$
c\ ;\ \pi_{1}\ ;\ \|\pi_{1}\|_{n}\quad:\quad B\to\|A\|_{n}
$$
The idea being we will take an element $b:B$, we have a proof that the truncation of the fibre at $b$ is contractible ($c$). The first component of the proof is an the truncation of an element and the proof that its in the fibre of $b$ ($\pi_{1}$). And then we discard the proof that its in the fibre of $b$ to get just the element $\|A\|_{n}$.

Now we need to show that these functions are inverses of each other.

Since in both directions, the codomain is a path in $n$-type, it suffices to cover the case of the constructor.
For one direction, we have 
$$
\prod_{a:A}g(\|f\|_{n}(|a|_{n}))= |a|_{n}
$$
which simplifies to , forall $x:A$
$$
\|\pi_{1}\|_{n} (\pi_{1}(c(f(x)))) = |x|_{n}
$$
Since $c(f(x))$ states that the fiber of $f(x)$ is contractible, then it contains the unqiue element $|(x, \text{refl}_{f(x)})|_{n}$ we simply get
$$
\|\pi_{1}\|_{n}(|x,\text{refl}_{f(x)}|_{n})=|x|_{n}
$$
which gives what we want.

For the other direction, we need to show that for each $y:b$
$$
\|f\|_{n} (\|\pi_{1}\|_{n}(\pi_{1}(c(y))))=|y|_{n}
$$
$c(y)$ states that the fibre at $y$ is contractible, we first extract the fibre by $\pi_{1}$. Then we extract an element of the fibre $\|\pi_{1}\|_{n}$ and then we send the element back, which my go back to $|y|_{n}$, that is precisely the second projection of the fiber if we can prove
$$
\|f\|_{n}(|a|_{n})=|y|_{n}
$$
if we have that $f(a)=y$ but left side is just $|f(a)|_{n}$ so its just application of $|-|_{n}$ to both sides.

---
# References
- [[n-Types]]
- [[n-connected types]]
- [[Functions as Equivalences]]
- [[Universal Property (Riehl)]]