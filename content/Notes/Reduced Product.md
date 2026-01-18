---
id: Reduced Product
aliases:
  - Reduced Product
  - Ultraproducts
tags:
  - Note
---
202601172258

Tags : [[Model Theory]]
# Reduced Product
---
Just as how [[Product of Models]], models statements modelled by all component models, there is an alternate construction that statisfies those statements that are modelled by "almost all" models.

This idea is captured using [[Filters]].

Given any set $S$, a filter on $S$ let us define a weak version of a measure, something like:

$$
m(A) = 
\begin{cases}
1 & \text{if }A\in F \\
0 & \text{if } S\setminus A \in F \\
\text{is undefined } & \text{otherwise}
\end{cases}
$$

This works because A filter along with collection of sets whose complement is in the filter form a [[Field (Measure Theory)|field]], and hence, some notion of probability can be defined on them. This will be used to define statements that hold almost everywhere.

Thus consider the [[Product of Models]]. Given a formula $\varphi$. We define the boolean extension of $\varphi(\bar a)$ as the set $\|\varphi(\bar a)\| = \{i\in I: \mathcal M_i \models \varphi(\bar a_i)\}$ and we get the following:
- $\|\varphi \lor \psi\| = \|\varphi\|\cup\|\psi\|$
- $\|\varphi \land \psi\| = \|\varphi\|\cap\|\psi\|$
- $\|\lnot \varphi\|$ = $I\setminus \|\varphi\|$
- For all $n-1$ tuples $\bar a$ and element $b$ we have $\|\varphi(\bar a, b)\|\subseteq \|\exists b\varphi(\bar a, b)\|$, and there exists a $b$ where the equality holds.

This lets us phrase the statement about 2 elements of $a$ and $b$ being almost equal if $\|a=b\|\in F$, which is an equivalence relation, thus we quotient over this relation to get $\prod_{i\in I}\mathcal M_i / F$ which is called the **reduced product**. 

- Thus universe is defined as $M/F$
- A constant $c^{\mathcal M / F} = [c^\mathcal M]$ is the equivalence class.
- For functions $f^{\mathcal M / F}(\bar a / F) = (f^{\mathcal M}(\bar a))/F$
- Given an $n$ place relation symbol $r$ we get that the set $r^{\mathcal M /F}(\bar a / F)$ if $\|r^{\mathcal M}(\bar a)\|\in F$.


If all components of the product are the same, then this construction is called the **reduced power**.

If the filter used for this construction is an **ultrafilter** then it is called **ultraproduct** (or **ultrapower**).

---
# References
- [[Product of Models]]
- [[Field (Measure Theory)]]
- [[Filters]]
