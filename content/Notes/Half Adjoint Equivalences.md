---
tags:
  - Note
---
202505231505

Tags : [[Homotopy Type Theory]]
# Half Adjoint Equivalences
---
>[!definition]
>A function $f:A \to B$ is a **half-adjoint equivalence** if there is a $g:B \to A$ and homotopies $\eta:g \circ f \sim \text{id}_{A}$ and $\epsilon: f \circ g \sim\text{id}_{B}$ such that there exists a homotopy
>$$
>\tau:\prod_{a:A} f(\eta x) = \epsilon (f x)
>$$

Hence we have the type $\text{ishae}(f)$ defined as:
$$
\sum_{(g:B \to A)} \sum_{(\eta: g\circ f\sim \text{id}_{A})} \sum_{(\epsilon: f \circ g \sim \text{id}_{B})} \prod_{(x:A)} f(\eta x)=\epsilon(f x)
$$

>[!tip] Unpacking the definition
>If we look at the type of the equality, we notice that both elements are equality between term of the form $x=_{B}y$, what this is saying is, consider an element $a:A$, and its output $f(a):B$, we first have that on $f(a), f\circ g$ is homotopic to $\text{id}_{B}$. But on $x$ we have that  there is a homotopy between identity and $g\circ f$ and we it to be equal to the previous homotopy if we move it to the type $B$ using $f$.

Note that the above definition is very asymmetrical in terms of $f$ and $g$, so one can write a version that emphasises on $g$ but turns out [[Both Directions of Half Adjoints are Logically Equivalent]].

It is important to not include the other direction though, hence the name half-adjoint equivalence.

And it is starightforward that $\text{ishae}(f)\to \text{qinv}(f)$, the other direction also holds:
>[!lemma]
>For any $f:A \to B$ we have $\text{qinv}(f)=\text{ishae}(f)$.

Suppose $(g, \eta, \epsilon)$ is a quasi inverse, we need to provide $(g', \eta', \epsilon', \tau)$ which is a half-ajoint equiavlence. We simply define $g' :\equiv g$ and $\eta' :\equiv \eta$, and now need to start worrying about $\tau$.
$$
\epsilon'(b)= \epsilon(f(g(b)))^{-1} \cdot f(\eta(g(b))) \cdot \epsilon(b)
$$
Because we need to find
$$
\tau(a): f(\eta(a))=\epsilon(f(g(f(a))))^{-1} \cdot f(\eta(g(f(a)))) \cdot \epsilon(f(a))
$$
And now its just symbol manipulation as follows:
$$
\begin{align}
f(\eta(g(f(a)))) \cdot \epsilon(f(a)) &= f(g(f(\eta(a)))) \cdot \epsilon(f(a)) \\
&=\epsilon(f(g(f(a)))) \cdot f(\eta(a))
\end{align}
$$
And this completes the proof.

---
# References
- [[Both Directions of Half Adjoints are Logically Equivalent]]
- [[Functions as Equivalences]]
