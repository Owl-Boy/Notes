---
tags:
  - Example
---

202502132155

tags : [[Finite Model Theory]]

#  BIT is expressible in $\text{FO}(\{ +, \times \})$
---
The relation $\text{BIT}$ is defined as follows:
$$
\text{BIT}(x, y) := y^\text{th}\text{ bit of the binary representation of $x$ is }1
$$
This is proved using a lot of steps:
1. First we show that it is possible to check if $x$ is a power of $2$
    $$\text{pow}_{2}(x) \equiv \forall u,v ((x = u \cdot v) \land (v\neq 1)) \to \exists z(v =  z + z)$$
2. Now we define the predicate
    $$\text{BIT}'(x, y) = (\lfloor x / y \rfloor \mod 2)=1$$
    if $y = 2^u$ this exactly describes $\text{BIT}$
3. So we now define $y=2^u$, this will be done with the help of multiple other terms
	  1. The first of those is $\text{extract}(a, b)= \lfloor a / b \rfloor \mod b$.
	  2. Checking if a number is a power of $4$: $\text{pow}_{4}(x) =\text{pow}_{2} \land x= 1 \mod 4$
	  3. Checking if a number $u$ is of the form $\sum_{i=1}^s 2^{2^i}$ in the from of $P_{1}(u)$
	     $$\forall v\Big(2 < v \leq u \to \big(\text{BIT}'(u, v) \leftrightarrow (\text{pow}_{4}(v) \land \exists w [(w \cdot w = v) \land \text{BIT}'(u, w)])\big)\Big)$$
	     Along with $\lnot \text{BIT}'(u, 1)\land \text{BIT}'(u, 2)$
	 4. Using this we can define if a number is of the form $2^{2^i}$ as 
	     $$\text{ppow}_{2}(u) \equiv \text{pow}_{2}(u) \land \exists w P_{1}(w)\land \text{BIT}'(w, u)$$
	1. Using the above, we can finally define  $P_{2}(x, u) \equiv y=2^x \land x^4 \leq n-1$ by defining a sequence of powers if 2 as 
	$$P \equiv \text{extract}(P,2)=1 \land \forall u(\text{ppow}_{2}(u) \to (\text{extract}(P, u^2) = 2 \cdot \text{extract}(P, u)))$$
	This using that to define a number and its power of 2 as sequences, 1 representing a number, and the other its power of 2
	![[Pasted image 20250214002915.png]] 
	SO here we define $P_{2}(x, y) = \exists a, b, u$ such that $a, b$ satisfy the above definition and $\text{extract}(a, u)=x$ and $\text{extract}(b, u)=y$. The extra fluff around the number (sequence) stop us from computing exponent for big numbers, if we want length of representation of $y$ to be $k$ then $y \geq 2^{k-1}$, so $x \geq 2^{2^{k-1}}$ and $x^4 \geq 2^{2^{k+1}}$. For such a $y$, we need to go to at least $k$ terms so length of $\vec{p}$ will be at most $2^{k+1}-1$ so size of $p$ would be $2^{2^{k+1}-1}-1$, which is bounded by the size of the universe, and by the size of $x^4$, so if $x^4$ does not exceed the amount then nether will the sequence.
4. And now we define $y=2^x$ as
	![[Pasted image 20250214005235.png]]
5.With that $\text{BIT}(x, y) = \exists u (u=2^y \;\; \land \text{BIT}'(x, u))$. 

---
# Related
