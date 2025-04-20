---
tags:
  - Note
  - Incomplete
---
202503301403

Tags : [[Intro to Martingales]]
# Radon-Nikodym Theorem for Countably Generated Sigma Field
---
>[!theorem]
>Let $\cal F$ be a countably generated $\sigma$-field on a set $\Omega$, i.e. there exists a sequence of sets $\{ B_{n} : n\geq 1 \}$ such that $\mathcal F = \sigma(\{ B_{n} : n\geq 1 \})$. Let $P, Q$ be probability measure on $(\Omega, \mathcal F)$ such that $Q \ll P$. For $n\geq 1$, let $\mathcal F_{n} = \sigma(B_{1} \dots B_{n})$ then show the following:
>1. For each $n\geq 1,\exists$ a partition $\{ C_{1}\dots C_{k_{n}} \}$ of $\Omega$ such that
>   $$
>   \mathcal F_{n} = \{ C_{1}, C_{2} \dots C_{k_{n}} \}
> $$ 
> 2. For $n\geq 1$ let 
>    $$
>    X_{n}(\omega) = \sum 1_{\{ P(C_{j}) >0 \}}  \frac{Q(C_{j})}{P_{C_{j}}} 1_{C_{j}}(\omega) 
>  $$
>    Show that $(X_{n},\mathcal F_{n})$ is a uniformly integrable martingale on $(\Omega, \mathcal F, P)$.
> 3. $X_{n}$ converges in $L_{1}(P)$ and also $P$-almost surely to $X$ satisfying
>    $$
>    \int X \, dP = Q(A)\quad \forall A\in \cal F 
>  $$
>    The random variable $X$ is called the Radon-Nikodym derivative of $Q$ w.r.t. $P$.

#### 1)
Consider all non-empty sets of the form $H_{1} \cap H_{2} \dots H_{n}$ where $H_{i}$ is either $B_{i}$ or $B_{i}^c$. There are at most $2^n$ many such sets.
- These sets are all disjoint because given any 2 different sets $C_{m}, C_{n}$, $\exists i$ such that $C_{m}\subseteq B_{i}$ and $C_{n} \subseteq B_{j}^c$ so are disjoint
- Given any point $\omega \in \Omega$ let $C_{\omega} = \bigcap H_{i}$ where $H_{i}= B_{i}$ if $\omega \in B_{i}$ else $B_{i}^c$. This shows that $\{ C_{1} \dots C_{k_{n}}\}$ is a partition of $\Omega$.
- Given a $B_{i}$ we can write it as $\bigcup_{j:C_{j}\subseteq B_{j}} C_{j}$, and since each $C_{i}$ can be written as an intersection of $B_{j}$s and $B_{j}^c$s, it is clear that $\sigma(B_{1} \dots B_{n}) = \sigma(C_{1} \dots C_{k_{n}}) = \mathcal F_{n}$.

#### 2)
We first show that each $X_{n}$ is integrable:
$$
\begin{align}
\int \sum_{j:P{(C_{j})>0}} \frac{Q(C_{j})}{P(C_{j})}1_{C_{j}}  \, dP &= \sum_{j:P(C_{j}) > 0} \int \frac{Q(C_{j})}{P(C_{j})}1_{C_{j}}  \, dP   \\
&= \sum_{j:P{(C_{j})>0}} \frac{Q(C_{j})}{P(C_{j})}  \int 1_{C_{j}}  \, dP  \\
&= \sum_{j: P(C_{j}) >0} \frac{Q(C_{j})}{P(C_{j})} \cdot P(C_{j}) \\
&= \sum_{j:P(C_{j}) > 0} Q(C_{j}) + \sum_{j:P(C_{j}) = 0} P(C_{j})  \\
&= \sum_{j:P(C_{j}) > 0} Q(C_{j}) + \sum_{j:P(C_{j}) = 0} Q(C_{j})  \\
&= Q(\Omega) = 1
\end{align}
$$
The change from $\sum_{j:P(C_{j})=0} P(C_{j})$ to $\sum_{j:P(C_{j})=0} Q(C_{j})$ is due to absolute convergence.

Now we show that $\{ X_{n}\}$ is adapted to $\cal F_{*}$ :
- For a given $n$, we have that $1_{C_{j}}$ is $\cal F_{n}$-measurable
- Hence $1_{P(C_{j}) > 0} \frac{P(C_{j})}{Q(C_{j})}1_{C_{j}}$ is measurable
- This $\{ X_{n}\}$ is adapted to $\cal F_{*}$

Now to show that $(X_{n},\mathcal F_{n})$ is a martingale: 
We show that $X_{n}$ satisfies the conditions for $E[\![X_{n+1}, \mathcal F_{N}]\!]$.

Consider $\int X_{n+1} 1_{S} \, dP$ such that $S\in \mathcal F_{n}$. $S = C_{m_{1}} \cup C_{m_{2}}\dots C_{m_{i}}$ for some $i$
Therefore $\int X_{n+1} 1_{S} \, dx = Q(C_{m_{1}}) + Q(C_{m_{2}})\dots Q(C_{m_{i}})= \int X_{n} 1_{S} \, dx$ therefore we have $E[\![X_{n+1} \mid \mathcal F]\!] = X_{n}$

Now to show that $X_{n}$ is uniformly integrable.
By the other definition of absolute convergence, we get that 
$$\forall \epsilon >0 \exists \delta <0 \forall S, [P(S)<\delta \to Q(S) < \epsilon].$$

Given an $\epsilon$ pick an appropriate $\delta$ according to the above definition. Now to show that $\{X_{n} \}$ is uniformly integrable:
Since $X_{n} > 0$, by chebyshev's inequality we get $P(X_{n} > k) \leq \frac{E[\![X_{n}]\!]}{k}=\frac{1}{k}$.

Hence 
$$
\lim_{ k \to \infty } \sup_{n\in \mathbb{N}}[E[\![X_{n}1_{X_{n}>k}]\!]]
$$
But $(X_{n} >k)$ is a set $S$ such that $S\in \mathcal F_{n}$ and $P(S) < \frac{1}{k}$, so we can write the above equation as:
$$
\lim_{ k \to \infty } \sup_{n\in \mathbb{N}}[E[\![X_{n}1_{S}]\!]]
$$
But for all $k > \frac{1}{\delta}$, $P(S)< \delta$ and $E[\![X_{n}1_{S}]\!]=Q(S)<\epsilon$, thus the limit goes to $0$.

#### 3)
By [[Doob's Martingale Convergence Theorem]], we have that $\{ X_{n} : n \geq 1 \}$ converges to a random variable $X$ in $L_{P}^1$ and $P$-almost surely. Now we just need to prove that $\int _{S}X \, dP = Q(S)$.

Since $X$ is an integrable random variable, with integral 1, it induces a probability on $(\Omega, \mathcal F)$, let that measure be $Q'$. We also know that for sets that belong to $\bigcup \mathcal F_{n}$, $Q'$ agrees with $Q$.

But we have that $\bigcup\mathcal F_{n}$ is closed under finite intersections and complements, hence is a [[Field (Measure Theory)|Field]] such that $\sigma(\{ B_{n}: n \geq 1 \}) = \sigma\left( \bigcup \mathcal F_{n} \right)=\mathcal F$, so by Caratheodory extensions theorem, we have $Q' =Q$


>[!attention] prepare
>prepare the equivalence of 2 definitions of uniform continuitiy
>And show that if 2 a sequence of functions is l1 convergent, it is also l1 convergent on each set in the sigma field.

---
# References
