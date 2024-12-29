---
tags:
  - Note
  - Incomplete
---
202412270312

Tags : [[Set Theory]], [[Measure Theory]]
# Failure of CH in a suitable Model
---
Any probability space leads to a model for axioms in the boolean valued sense.

We now construct a space is very big:
- Let $\Omega=[0,1]^I$ where $I$ is a set with cardinality strictly greater than $2^{\aleph_{0}}$.
- We use ordinary lebesgue measure on $[0,1]$ and the product measure on $\sigma$ field of baire subsets of $\Omega$.
- For each $i\in I$ let $\xi_{i}$ be the projection onto the $i^\text{th}$ coordinate. There are measurable functions, hence random reals.

We will now construct a set that is nether countable, nor can map onto the entire set.
- Let $J$ be an uncountable subset of $I$ with smaller cardinality. 

We want to construct a functions $\chi$ which is $0$ on $J$ and $1$ outside. We do this in the following way, Given a $\xi\in \cal R$, let $\Lambda_{\xi}$ be the set such that:
- $\bigcup_{j\in J}[\![\xi=\xi_{j}]\!]=\Lambda_{\xi} / [P=0]$
	- This reads as, $\Lambda_{\xi}$ is equivalent to the set where $\xi$ behaves like one o the projection functions from $J$
- Let $\chi(\xi)$ be the characteristic function of $\Lambda_{\xi}^C$.
	- This is very clearly a random function
	- It has the property that $[\![\chi(\xi)=0]\!]= \bigcup_{j\in j}[\![\xi=\xi_{j}]\!]$

We will now show that $\Big[\!\!\Big[\exists g \forall y \exists x[\chi(x)=0 \land y=g(x)]\Big]\!\!\Big]=\mathbb0$
- This statement reads as for almost any $g$ there is most likely some $y$ that is not in the image of $\chi(x)$ for almost all $x$.

Assume contrary and choose the function $\psi$ and let the valuation be $E$ then
For each $i$ we have 
$$
\begin{align}
E &\subseteq [\![\exists x, \chi(x)=0 \land \chi_{i}=\psi(x)]\!] \\
&= \bigcup_{\xi\in \mathcal R} \bigcup_{j\in J} [\![\xi=\xi_{j} \land \xi_{i}=\psi(\xi)]\!] \\
&= \bigcup_{j\in J}[\![\xi_{i}=\psi(\xi_{j})]\!] 
\end{align}
$$

So for each $i$, there is a $j_{i}$ such that $E\cap [\![\xi_{i}=\psi(\xi_{j_{i}})]\!]\ne 0$. But $J$ has a smaller cardinality than uncountable$I$ so there must be a fixed $k$ such that $K=\{ i\in I : j_{i}=k \}$.

now for $i\in k$ we define $D_{i}= E \cap [\![\xi_{i}=\psi(\xi_{k})]\!]$. All $D_{i}$ are pairwise disjoint because $[\![\chi_{i} = \chi_{j} ]\!]=0$ when $i\ne j$. So we get uncountably many disjoint sets, which breaks the countable chain condition, hence $E$ must be $0$.



Finally:
$$
[\![\exists f \forall y, \chi(y)=0 \to \exists x[N(x) \land y=f(x)]]\!]=0
$$
Is very similar to check.

--- 
## Natural number definition
$$
N(y) \leftrightarrow \forall f[f(0)=0 \land \forall x[0\leq x \to f(x)=f(x+1)] \to f(y)=0]
$$

Consider the measurable function $g(x)=0$ if $x\in \mathbb{N}$ otherwise it is $1$ and $f(y)=g \circ y$

- then $f(y)=0$ whenever $y=n$ for some $n$.

so we get : 
$$
[\![N(y)]\!] = \bigcup_{n\in \mathbb{N}}[\![y=n]\!]
$$

---
## $\{ y:\chi(y)=0 \}$ is too big

$$
\exists f \forall y[\chi(y)=0 \to \exists x[N(x) \land y=f(n)]]=0
$$

We want to prove this so assume false and let $g$ be the witness. So we get.

$$
\forall y[\chi(y)=0 \to \exists x[N(x) \land y=g(n)]]=E \ne 0
$$

So we have to take intersection over all values of $y$. 

Now for each $j\in J$
$$
\begin{align}
E \subseteq [\chi(\xi_{j})=0 \to \exists x[N(x) \land y=g(x)]]
\end{align}
$$

But $\chi(\xi_{j})=0$ so that part evaluates to $\top$, hence we get 

$$
\begin{align}
E&\subseteq \bigcup_{n\in \mathbb{N}} \exists x[x=n \land \xi_{j}=g(x)]  \\
&\bigcup_{n\in N}\xi_{j}=g(n)
\end{align}
$$
So for each $\xi_{j}$ there is some $n_{j}$ such that $E\cap[\![\xi_{j}=g(n_{j})]\!]\ne \emptyset$ 

And there is some $m$ such that $K=\{ j : n_{j} =m , j\in J\}$ which is uncountable.

Now let $D_{k}= E \cap [\![\xi_{k}=g(m)]\!]$ for each $k\in K$.




---
# References
[[Continuum Hypothesis]]