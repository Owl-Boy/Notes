---
tags:
  - Note
  - Incomplete
---
202504210104

Tags : [[Finite Model Theory]]
# Stage Comparisons
---
**Stage Comparisons** are relations, which are meant to be interpreted as partial orders where $x \prec y$ is a statement which is true in a model if the stage of $x$ is less than the stage of $y$.

>[!attention] Notation
>These comparisons must happen, in context of a relation defined by some formula $\varphi$, usually mentioned in the superscript, I will be skipping because writing it again and again is painful.

We would like the define the following relations for this:
$$
\begin{align}
\vec{x} \prec \vec{y} &\equiv |\vec{x}|_{\varphi}^\mathfrak A < |\vec{y}|_{\varphi}^\mathfrak A\\
\vec{x} \preceq \vec{y} &\equiv |\vec{x}|_{\varphi}^\mathfrak A \leq |\vec{y}|_{\varphi}^\mathfrak A \text{ and } |\vec{x}|_{\varphi}^\mathfrak A \leq |\varphi|^\mathfrak A
\end{align}
$$
to define these, we will be defining some auxiliary relations, such that we will be able to construct all of them as a simultaneous fixed point.

$$
\begin{align}
\vec{x} \not\prec \vec{y} &\equiv |\vec{x}|_{\varphi}^\mathfrak A \geq |\vec{y}|_{\varphi}^\mathfrak A\\
\vec{x} \not\preceq \vec{y} &\equiv |\vec{x}|_{\varphi}^\mathfrak A > |\vec{y}|_{\varphi}^\mathfrak A \text{ or } |\vec{x}|_{\varphi}^\mathfrak A = |\varphi|^\mathfrak A + 1
\end{align}
$$
These versions will let us 
and 
$$
\vec{x} \triangleleft \vec{y} \equiv |\vec{x}|_{\varphi}^\mathfrak A + 1 = |\vec{y}|_{\varphi}^\mathfrak A
$$

We now define the following tuple of relations as a least fixed point : 
$$
(\prec,\preceq,\triangleleft, \not\prec,\not\preceq)
$$
We define these with formula that are of the form, $\psi_{i}(\prec,\preceq,\triangleleft,\not\prec, \not\preceq, \vec{x}, \vec{y})$ where $i = [1..5]$, defined as follows:
- For $\prec$, we say $x\prec y$ is there is some $z$ for which $|x| \leq |z|$ and $|z|+1 = |y|$. This is described with the formula
	$$\psi_{1} \equiv \exists \vec{z}(\vec{x}\preceq \vec{z} \land \vec{z} \triangleleft \vec{y} )$$

- For $\preceq$ we say $x\preceq y$ by
	- First defining the unary relation $(-\prec y)$.
	- If $|y|=i$ the relation perfect describes $X_{i-1}$, hence applying $F_{\varphi}$ would give $X_{i}$, which is precisely the set in which $x$ needs to be in. 
	- We can apply $F_{\varphi}$ to a set $X$ and check membership of $\vec{x}$ in the result by $\varphi(X / R, \vec{x})$.
	$$\psi_{2} \equiv \varphi\Big((-\prec \vec{y}) ,\; \vec{x}\Big)$$

- For $\triangleleft$, we describe it as follows:
	- $\vec{x}$ must be in the fixed point
		- $\varphi\Big((-\prec \vec{x}),\; \vec{x}\Big)$
	- $\vec{y}$ must be strictly greater stage than $\vec{x}$, to describe that, I take the set where points are less than or equal to $\vec{x}$ and claim that $\vec{y}$ does not belong it, to make the statement positive, we use $\varphi$ to talk about membership, so we start 1 stage lower. This shows $|y|> |x|$
		- $\lnot \varphi\Big(\lnot(-\not\prec\vec{x}),\;\vec{y}\Big)$
	- Now we need to show that, either $|x| = |\varphi|$, in which case we are done, or that $|x| < |\varphi| \land |y| = |x|+1$
		- We can make the first claim by stating that if $|x| = i$ then $\overline {F_{\varphi}(X_{i})} \cup X_{i}$ is the entire space
			- $\forall \vec{z}, \lnot \varphi\Big(\lnot(- \not\preceq \vec{x}), \; \vec{z}\Big) \lor \vec{z}\preceq \vec{x}$
		- We can make the second claim by stating $|y| \leq |x| + 1$
			- $\varphi\Big((-\preceq \vec{x}), \; \vec{y}\Big)$
	$$\begin{align}\psi_{3} \equiv\; &\varphi\big((-\prec \vec{x}),\; \vec{x}\big) \land\lnot \varphi\big(\lnot(-\not\prec\vec{x}),\;\vec{y}\big) \\ &\land \Big[\Big( \forall \vec{z}, \lnot \varphi\big(\lnot(- \not\preceq \vec{x}), \; \vec{z}\big) \lor \vec{z}\preceq \vec{x}\Big) \lor \varphi\Big((-\preceq \vec{x}), \; \vec{y}\Big)\Big]\end{align}$$

- For $\not\prec$, we say $x\not\prec y$ by
	- $|y|=|z|+1$ where $|z| < |x|$, or
		- $\exists \vec{z}[\vec{x} \not\preceq \vec{z} \land \vec{z} \triangleleft\vec{y}]$
	- $|y| = 1$ which is the least possible if fixed point is non-empty, or
		- $\varphi(\emptyset, \vec{y})$
	- Fixed point is empty,
		- $\forall \vec{z} \lnot \varphi(\emptyset, \vec{z})$
	$$\psi_{4} \equiv \exists \vec{z}[\vec{x} \not\preceq \vec{z} \land \vec{z} \triangleleft\vec{y}] \lor \varphi(\emptyset, \vec{y})\lor \forall \vec{z} \lnot \varphi(\emptyset, \vec{z})$$

- For $\not\preceq$, we say $x\not\preceq y$ by 
	- Construct the set $(-\preceq y)$, take its complement, and let $x$ belong to it. 
	- Complementation makes the relation not positive, Hence we describe membership using $\varphi$
	- This forces us to allow points that are one stage higher, so we start with $(-\prec y)$, include 1 extra stage, and then show that $x$ does not belong to it.
		- $\psi_{5}' \equiv \lnot \varphi\Big((-\prec y),\;\vec{x}\Big)$
	- We now make slight changes to make it positive.
	$$\psi_{5} \equiv \lnot \varphi\Big(\lnot(-\not\prec y),\;\vec{x}\Big)$$
---
All together they are defined as:
>[!definition]
>$$
>\begin{align}
>\psi_{1} &\equiv \exists \vec{z}(\vec{x}\preceq \vec{z} \land \vec{z} \triangleleft \vec{y} ) \\
 >\\
>\psi_{2} &\equiv \varphi\Big((-\prec \vec{y}) ,\; \vec{x}\Big) \\
 >\\  
      >\psi_{3} &\equiv\; \varphi\big((-\prec \vec{x}),\; \vec{x}\big) \land\lnot \varphi\big(\lnot(-\not\prec\vec{x}),\;\vec{y}\big) \\
      >&\quad\;\ \land \Big[\Big( \forall \vec{z}, \lnot \varphi\big(\lnot(- \not\preceq \vec{x}), \; \vec{z}\big) \lor \vec{z}\preceq \vec{x}\Big) \lor \varphi\Big((-\preceq \vec{x}), \; \vec{y}\Big)\Big]
 >\\ \\
>
>\psi_{4} &\equiv \exists \vec{z},[\vec{x} \not\preceq \vec{z} \land \vec{z} \triangleleft\vec{y}] \lor \varphi(\emptyset, \vec{y})\lor \forall \vec{z}, \lnot \varphi(\emptyset, \vec{z}) \\
 >\\
>\psi_{5} &\equiv \lnot \varphi\Big(\lnot(-\not\prec y),\;\vec{x}\Big)
>\end{align}
>$$



---
# References
