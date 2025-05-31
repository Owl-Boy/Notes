---
tags:
  - Note
---
202505300005

Tags : [[Homotopy Type Theory]]
# Univalence Implies Weak Function Extensionality
---
>[!Theorem]
>Suppose $P:A \to\cal U$ is a family of contractible types and let $\alpha$ be function from the corollary defined in [[Functions types to isomorphic types are isomorphic]]. Then $\prod_{x:A}P(x)$ is a retract of $\text{fib}_{\alpha}(\text{id}_{A})$, thus $\prod_{x:A} P(x)$ is contractible. Thus univalence implies weak function extensionality.

To prove that $\prod_{x:A}P(x)$ is a retract of $\text{fib}_{\alpha}(\text{id}_{A})$, to prove so, define the function;
$$
\begin{align}
\varphi&:\left( \prod_{x:A} P(x) \right) \to \text{fib}_{\alpha}(\text{id}_{A}), \\
\varphi(f) &:\equiv (\lambda x. (x, f(x)), \text{refl}_{\text{id}_{A}})
\end{align}
$$
and 
$$
\begin{align} 
\psi &: \text{fib}_{\alpha}(\text{id}_{A}) \to \prod_{x:A}P(x) \\
\psi(g, p) &:\equiv \lambda x.\text{happly}(p, x)_{*}(\text{pr}_{2}(g, x))
\end{align}
$$
And we have $\psi(\varphi(f)) = \lambda x.f(x)\equiv f$, so we are done.

---
# References
- [[Univalence]]
- [[Weak Function Extensionality]]
- [[Functions types to isomorphic types are isomorphic]]
- [[Higher Groupoid Structure of Pi Type|Function Extensionality]]
