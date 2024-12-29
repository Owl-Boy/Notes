---
tags:
  - Note
  - Incomplete
---
202412151112

Tags : [[Field Theory]], [[Order Theory]]
# Ordered Fields
---
An *Ordered Field* is a [[Fields|Field]] together with a total ordering on it which is compatible with the field operations.

The [[Syntax of First Order Logic|Syntax]] of Ordered fields contains the following
- Constants = $\{ 0, 1 \}$
- Functions = $\{ \cdot, + \}$ where both operations have parity $2$
- Relations = $\{ =, \leq \}$

And the following axioms also hold:
- Addition
	- $x + 0 = 0 + x = x$
	- $\exists \hat{x}, x + \hat{x}=\hat{x}+x=0$
	- $x+(y+z)=(x+y)+z$
	- $x+y = y+x$
- Multiplication
	- $x \cdot 1 = 1  \cdot x = x$
	- $\exists \hat{x}, x \cdot \hat{x}=\hat{x}\cdot x=0$
	- $x\cdot(y\cdot z)=(x\cdot y)\cdot z$
	- $x\cdot y = y\cdot x$
	- $x \cdot(y+z)=x \cdot y + x \cdot z$
- Ordering
	- $x \leq x$
	- $x \leq y\; \land\; y \leq x \implies x =y$
	- $x \leq y \land y \leq z \implies x \leq z$
	- $a \leq b \implies a+c \leq b + c$
	- $0 \leq a \land 0\leq b \implies {0} \leq a \cdot b$

>[!example]
> - The field $\mathbb Q$ with standard ordering
> - The field $\mathbb{R}$ with standard odering


---
# References
