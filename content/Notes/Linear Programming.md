---
tags:
  - Note
---

Tags : [[Advanced Algorithms]], [[Linear Programming]]
# Linear Programming
---
Linear programming trying solve the optimal solution for a given target function, which is a linear combination of a set op variables $x_{1}\dots x_{n}$ under linear constraints.

A linear constraint is an expression of the form $a_{1}x_{1} + \dots a_{n}x_{n} \geq b_{i}$. Such a constraint, if an equality represents a hyperplane in $\mathbb{R}^n$, and if it is an inequality then it represents a half-space, and the goal is to find the optimal solution for the target, in the intersection of all of these half-spaces

>[!definition]
>A *Linear Program* is an objective function, like 
>Minimise $c^Tx := c_1x_1 + \dots + c_nx_n$ subject to
>linear constraints of the form:
 >   $a_{11}x_1 + \dots a_{1n}x_n \geq b_1$
>   .
>   .
>   .
>    $a_{m1}x_1 + \dots a_{mn}x_n \geq b_m$
>    $x_i \geq 0$

Since the constrains form intersection of half-spaces, they form polyhedra which define a *feasible region* in which all points that satisfy the constraints lie. Since all half-spaces are convex, so is the feasible region.

Since the goal is a linear function, but not an equality, it is a hyper plane, but its location is not fixed and hence can take multiple values, finding the optimal solution is the same as moving the plane to the best location and finding solution there.

---
# References
-> [[(Weighted) Vertex Cover using LP]]
-> [[Equational form of LP]]
-> [[Solution of an LP]]
-> [[Integrality Gap]]