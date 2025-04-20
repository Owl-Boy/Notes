---
tags:
  - Note
  - Incomplete
---
202504190304

Tags : [[Finite Model Theory]]
# $\text{LFP}^\text{simult}=\text{LFP}$
---
The proof assumes that there is a simultaneous fixed point of 2 formulas of the for $\varphi_{1}(R,S, \vec{x})$ and $\varphi_{2}(R,S,\vec{y})$.

The idea is to combine a simultaneous fixed point into 2 fixed points where the $\text{lfp}$ operators are nested.

Assume there are 2 monotone operators:
- $F_{1} = \mathcal P(U)\times \mathcal P(V) \to \mathcal P(U)$
- $F_{1} = \mathcal P(U)\times \mathcal P(V) \to \mathcal P(V)$

We define the stages of the operator as:
- $\vec{X^0} = (\emptyset, \emptyset)$
- $\vec{X}^{i+1} = (X^{i+1}_{1}, X^{i+1}_{2})=(F_{1}(\vec{X}^{i}), F_{2}(\vec{X}^i))$
- $\vec{X}^{\infty} = (X^\infty_{1}, X^\infty_{2})$

We now define 2 operators:
$$
\begin{align}
F_{2}^Y :\mathcal P(V) \to \mathcal P(V)\quad&,\quad F_{2}^Y(Z) = F_{2}(Y, Z) \\
G_{1} : \mathcal P(U) \to \mathcal P(U)\quad&,\quad G_{1}(Y) = F_{1}(Y, \text{lfp}(F_{2}^Y))
\end{align}
$$
Now we use the following lemma:
>[!lemma] Lemma: Bekic
>$X_{1}^\infty = \text{lfp}(G_{1})$

With this lemma, we can define $G_{1}$ as the least fixed point as follows:
$$
\Big[ \mathbf{lfp}_{R, \vec{x}} \varphi_{1}\big(R, [\mathbf{lfp}_{S, \vec{y}} \varphi_{2}(R, S, \vec{y})] / S, \vec{x}\big)\Big] (\vec{t})
$$

We can flip the roles of $F_{1}$ and $F_{2}$ and similarly get a definition for $X_{2}^\infty$.

---
Now for the proof of the lemma:

Notice $\mathbf{lfp}(F_{2}^{X_{1}^\infty}) \subseteq X_{2}^\infty$. This is because $F_{2}^{X_{1}^\infty}(X_{2}^\infty) = F_{2}(X_{1}^\infty, X_{2}^\infty)=X_{2}^\infty$, i.e $X_{2}$ is a fixed point, so it must contain the least fixed point.

But $X_{1}^\infty$ is a fixed point of $G_{1}$ as $G_{1}(X_{1}^\infty) = F_{1}(X_{1}^\infty, \mathbf{lfp}(F_{2}^{X_{1}^\infty})) \subseteq F_{1}(X_{1}^\infty, X_{2}^\infty) =F_{1}^\infty$, so we get that $\mathbf{lfp}(G_{1}) \subseteq X_{1}^\infty$.

For the other side of the inclusion it suffices to show that all $X_{1}^i \subseteq \mathbf{lfp}(G_{1})$ and $X_{2}^i \subseteq \mathbf{lfp}(F_{2}^S)$. Assume $\mathbf{lfp}(G_{1})=Z$/

$$
{X}_{1}^{i+1} = F_{1}(X_{1}^i, X_{2}^i) \subseteq F_{1}(Z, \mathbf{lfp}(F_{2}^Z)) = G_{1}(Z, \mathbf{lfp}(F_{2}^Z)) = \mathbf{lfp}(G_{1})=Z
$$
and
$$
X_{2}^{i+1} = F_{2}(X_{1}^i,X_{2}^i) =F_{2}^Z(X_{2}^i) \subseteq F_{2}^Z(\mathbf{lfp}(F_{2}^Z)) = \mathbf{lfp}(F_{2}^Z)
$$
>[!note]
>The second half of proof seems intuitive.
>Consider how each $X_{1}^i$ is generated, we start with $\emptyset$, but then we fix that to find the fixpoint in the second component, which is bigger than $\emptyset$, hence bt monotonicity we get that $X_{1}^1$ will be bigger with this method. The we recompute the second component, which after $i$ iteration will be bigger than $X_{2}^i$, hence at each step we get something that is bigger than $X_{1}^i$.


---
# References
