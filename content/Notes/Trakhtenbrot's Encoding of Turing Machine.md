---
tags:
  - Example
---

202504060659

tags : [[Finite Model Theory]]

#  Trakhtenbrot's Encoding of Turing Machine
---
The sentences that were mentioned in [[Trakhtenbrot's Theorem]] are described here:
- We have 1 formula that states $\leq$ is an ordering relation
	- $\forall x, y, x\leq y \lor y \leq x$
	- $\forall x, x \leq x$
	- $\forall x, y,z, x\leq y \land y\leq z \implies x\leq z$
	- $\forall x, y, x\leq y \land y \leq x \implies x = y$
- We define $\text{min}$ to be the smallest element in the model
	- $\min :\equiv x : \forall y, x\geq y$
- For all the other relations, we treat the first argument as the configuration step of the machine and the second argument as the position in the configuration
	- We first have a formula to state that the first configuration is the start configuration
		- $H_{q_{0}}(\min, \min) \land \forall p,T_{0}(\min, p)$
	- Then we have a formula to state that there is some final configuration
		- $\exists t ,p, H_{q_{a}}(t, p) \lor H_{q_{r}}(t, p)$
	- A formula encoding transitions
		- One for transitions that move the pointer to right ![[Pasted image 20250406071350.png]]
		- One for the transition that moves the pointer to left ![[Pasted image 20250406071421.png]]
- And we also have the following formulas ensuring the following:
	- each node is labelled either 0 or 1 and not both
		- $\forall t, p, T_{0}(t, p) \otimes T_{1}(t,p)$
	- each configuration has exactly 1 position labelled with a vertex
	 $$\forall t, \exists!p, \bigvee_{q\in Q}H_{q}(t, p) \quad \land\quad \lnot\exists t, p, \bigvee_{q, q' \in Q\quad q\neq q'}H_{q}(t, p) \land H_{q'}(t, p)$$

---
# Related
