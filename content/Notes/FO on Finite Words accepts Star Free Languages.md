---
tags:
  - Note
  - Incomplete
---
202503080403

Tags : [[Finite Model Theory]], [[Logic]], [[Automata Theory]]
# FO on Finite Words accepts Star Free Languages
---
>[!theorem]
>A language is definable in [[First Order Logic|FO]] iff it is [[Star Free Languages|Star Free]] 

---
## Every Star Free language is FO definable
For this we use induction on the shape of the star free expression representing the language.
$$
\begin{matrix}
[\![\emptyset]\!] &:&\exists x, x\neq x\\
[\![\{\epsilon\}]\!] &:& \forall x, x\neq x\\
[\![\{a\}]\!] & :& \exists!x, x=x \land P_{a}(x) \\
[\![\bar{e}]\!] & : & \lnot [\![e]\!] \\
[\![e_{1}+e_{1}]\!] & : & [\![e_{1}]\!] \lor [\![e_{2}]\!] \\
[\![e_{1} \cdot e_{2}]\!] & : & \exists x ([\![e_{1}]\!]_{x} \land [\![e_{2}]\!]^{x})
\end{matrix}
$$

For the concatenation, we assume that $x$ is not a free variable and the notation $\phi_{x}$ here means any quantification $\exists y\ \varphi$ is replaced by $\exists y, (y\leq x) \land\varphi$ and $\phi^x$ means $\exists y\ \varphi$ is replaced by $\exists y\ (y> x) \land \varphi$.

---
## Every FO definable language is Star Free
We will be assuming the constant $\text{max}$ is the largest element of the universe, this is fine as it is definable in FO.

The proof is by induction on the quantifier rank.

Boolean combination of star free languages are clearly star free.

**Base Case:** $k=0$
For this case, the atomic formulas are $P_{a}(\max)$ along with $\text{true}$ and $\text{false}$. These can be written as $\bar{\emptyset}a$, $\bar{\emptyset}, \emptyset$ respectively.

**Induction Step:**
Because of the closure under boolean operations, it is enough to show this for formulas that are of the form $\exists x\ \varphi(x)$.

Let $\tau_{1} \dots \tau_{m}$ be the enumeration of all rank $k$-types. We define
$$
S_{\Phi} = \left\{ (\tau_{i},\tau_{j}) \mid \quad
\begin{align}
& \text{for some }s \text{ and a position }p, M_{s}\vDash \phi(p)\\
&\text{tp}_{k}(M_{s}^{\leq p})=\tau_{i} \text{ and } \text{tp}_{k}(M_{s}^{> p})=\tau_{j}
\end{align}
\right\}
$$

Now we show that for every $M_{s}$ there exists a $p$ in $u$ such that for some $(\tau_{i}, \tau_{j})$ we have 
$$
\text{tp}_{k}(M_{s}^{\leq p}) =\tau_{i}\quad \text{and} \quad \text{tp}_{k}(M_{s}^{> p}) = \tau_{j}
$$
First we notice that the claim implies that $L(\Phi)$ is star-free. This is because Given $\tau_{i}, \tau_{j}$ for which the above holds, we get that $s\in L(\Psi_{i}) \cdot L(\Psi_{j})$ and $L(\Phi)$ can be written as a finite union of such languages so is hence definable.

If $M_{u} \vDash \Phi$, then the existence of a $p$ and a pair $(\tau_{i}, \tau_{j})$ follows from the definition of $S_{\Phi}$. For the converse, suppose we have a string $u$ and a position $p$ for which this holds, then we write $u=u_{1}u_{2}$. We have some $s_{1}\in L(\Psi_{1})$ and some $s_{2}\in L(\Psi_{2})$ with $M_{u_{1}} \equiv_{k}^\text{MSO} M_{s_{1}}$ and  $M_{u_{2}} \equiv_{k}^\text{MSO} M_{s_{2}}$. so we get $M_u \equiv_{k}^\text{MSO} M_{s}$.

And we are done.

---
# References
