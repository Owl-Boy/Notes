---
tags:
  - Note
---
202402121002

Tags : [[Linear Programming]]
# Primal - Dual LP
---
Given a [[Linear Programming|Linear Program]], with some objection function $c^Tx$, one can ask about the range of values that can be taken by the cost function, for example to compute the lower bound, of the following linear program:
- Goal: minimize $5x_{1} + 4x_{2} + x_{3}$
- Constraint:
	- $4x_{1} + 2x_{2} \leq 5$
	- $x_{2} + x_{3} \leq 2$
	- $x_{1}+x_{2}+x_{3} \leq 3$
	- $x_{i}\geq 0$

From the constraints themselves, we can get that we can get a lower bound of $5$, as the first constraint is less than the goal. with the first and third one together, one can show that $8$ is a better lower bound. 

One can try to find better lower bounds by taking linear combinations of the constraints, this can be done by treating the constraints of above linear program as variables and make the following new linear program:
- Let variables be $y_{1}, y_{2}$ and $y_{3}$ 
	- One for each constraint
- Goal: maximize $5y_{1}+2y_{2}+3y_{3}$
	- Each constraints contributes at least the value in the inequality
- Constraints
	- $4y_{1}+y_{3} \geq 5$
	- $2y_{1}+y_{2}+y_{3} \geq 4$
	- $y_{2}+y_{3} \geq 1$ 
		- The minimzation of the previous goal is the target, no point in giving lower bound for a function that is bigger than the goal.

The final definition of *Primal Dual* is as follows:
>[!definition]
>*Primal-Dual* is a pair of linear programs with the following form:
>- Primal:
>	- Maximize $c^T x$
>	- Constraints : $Ax \leq b$
>- Dual:
>	- Minimize $b^T y$
>	- Constraints : $A^Ty \geq c$

---
# References
[[Duality Theorems for LP]]