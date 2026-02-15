---
id: Tarski-Vaught test
aliases:
  - Tarski-Vaught test
tags:
  - Note
  - Incomplete
---
202602102316

Tags : [[Model Theory]]
# Tarski-Vaught test
---
> [!THM]
> Let $\cal M, N$ be $\cal L$-structures such that $\cal M$ is a sub-structure of $\cal N$. Then $\cal M$ is an [[Elementary Equivalence of Models|elementary substructure]] of $\cal N$ 
>
>iff
>
>for every $\mathcal L$-formular $\varphi(x,\bar v)$ and for every $\bar a$ in $\mathcal M$, if there exists $n$ such that $\mathcal N\models \varphi(n, \bar a)$ then there exists an $m\in \mathcal M$ such that $\mathcal N\models \varphi(m, \bar a)$.

## Sufficient Condition
Let $\mathcal M$ be an elementary sub-structure of $\mathcal N$ then if $\mathcal N \models \exists : \varphi(x, \bar a)$ then we have $\mathcal M \models \exists \varphi(x, \bar a)$

passing back up to $\mathcal N$ yields the result.

## Necessary Condition
Consider a formula $\psi(\bar v)$ and for every $\bar a \in \mathcal M$:
$$
(\mathcal M \model \varphi(\bar a)) \iff (\mathcal N \models \varphi(\bar a))
$$

Note: Quantifier free-formulas are preserved by superstructures.

We can close them under boolean operators trivially.

We now show that it holds formulas with quantifiers by inducting on quantifier depth, the base case is proven above.

Now consider a formula $\exists x,\psi(x, \bar a)$, by induction hypothesis, if this holds in $\mathcal M$, then it would hold for $\mathcal N$.

But if it holds for $\mathcal N$, it trivially holds for $\mathcal M$.

---
# References
- [[Elementary Equivalence of Models]]
- [[Downward Löwenheim–Skolem Theorem]]
