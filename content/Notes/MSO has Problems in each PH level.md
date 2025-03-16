---
tags:
  - Note
---
202503142003

Tags : [[Finite Model Theory]], [[Complexity Theory]]
# MSO has Problems in each PH level
---
>[!theorem]
>For each level $\Sigma_{i}^p$ and $\Pi_{i}^p$ of the [[Polynomial-Time Hierarchy]], there exists a problem complete for that level which is expressible in [[Monadic Second Order Logic|MSO]].

We prove this showing that [[Sigma-i 3SAT]] is expressible in $\text{MSO}$. A similar argument works for [[Pi-i 3SAT]]. Since we know that $\Sigma_{i}^p 3\text{SAT}$ is $\Sigma_{i}^p$-complete.

Given a formula of such a problem we convert it to a structure such that there is a formula which is satisfied by the structure iff the SAT formula is true.

We also assume for each clause, all the negated terms are written after the non-negated terms

***Structure:***
- We define the universe to be the set of variables of $\Phi$.
- We have a unary predicate for each strata of quantifier, so for $\Sigma_{i}^p$ would be $E_{1}, A_{2}, E_{3}\dots E_{k}$
- 4 ternary predicates $R_{FFF},R_{TFF}, R_{TTF}, R_{TTT}$
	- $R_{FFF}$ is for clauses where all 3 terms are negated.
	- $R_{TFF}$ is for clauses where last 2 terms are negated
	- $R_{TFF}$ is for clauses where last term is negated
	- $R_{TFF}$ is for clauses where no terms are negated

***Formula:***
We use the following formula
$$
\exists Y_{1} \subseteq E_{1}, \forall Y_{2}\subseteq A_{2}\dots \exists Y_{k} \subseteq E_{k} (\varphi')
$$
where we define $\varphi'$ as:
- $Y = \bigcup Y_{i}$
- $\forall x,y,z(R_{FFF}(x, y, z) \to x \not\in Y \land y \not\in Y \land z \not\in Y)$
- $\forall x,y,z(R_{TFF}(x, y, z) \to x \in Y \land y \not\in Y \land z \not\in Y)$
- $\forall x,y,z(R_{TTF}(x, y, z) \to x \in Y \land y \in Y \land z \not\in Y)$
- $\forall x,y,z(R_{TTT}(x, y, z) \to x \in Y \land y \in Y \land z \in Y)$

---
# References
