---
tags:
  - Example
---

202503272130

tags :  [[Homotopy Type Theory]]

#  Type Theoretic Axiom of Choice
---
Consider the following when $A, B:\cal U$ and $R : A \to B \to \cal U$.
$$
\text{ac}:\left( \prod_{x:A} \sum_{y:B}R(x, y) \right) \to \left( \sum_{f:A\to B} \prod_{x:A}R(x, f(x)) \right)
$$
Here $R$ can be thought of as a relation between the types $A, B$ and an element $p:R(a, b)$ is a proof that $a, b$ are related.
The statement $\text{ac}$ states that if we have a function $g$ that takes an element of type $A$ and returns an element of type $B$ such that they are related, then there is a function $g$ such that for each element $x:A$, it will give the corresponding element $g(x)$ which is related. This statement seems rather tautological and sure enough, it is very easy to prove:

$$
ac(g) :\equiv (\lambda x.\text{pr}_{1}(g(x)), \lambda x. \text{pr}_{2}(g(x)))
$$

This statement can now also be thought of as the following:
- $A$ is a family of sets whose union is $B$, each set is $R(x, -)$.
- The input to $\text{ac}$ states that each of these sets is non-empty
- The output of $\text{ac}$ is a function that picks an element $y$ from each of the sets $R(x, -)$.
This looks very similar to the statement of axiom of choice and is hence called **Type Theoretic Axiom of Choice**.

---
# Related
[[Axiom of Choice and its Variants]]
[[A better Axiom of Choice for Type Theory]]
