---
tags:
  - Note
  - Incomplete
---
202504210004

Tags : [[Finite Model Theory]]
# Stages 
---
[[Fixed Point Logics]] compute sets by using a formula to describe an operator on the collection of subsets of the universe, which is applied on the  empty set repeatedly until a fixed point is reached.

We now define a way to compare when different points of the universe enter the set defined using the fixed point operator, more specifically.

Consider a formula $\varphi(R, \vec{x})$ such that all occurrences of $R$ are positive in $\varphi$, hence it defines a monotone operator. Since we are working with finite models, $F_{\varphi}$ reaches its fixed point after finitely many steps which we define to be $|\varphi|$.

We now define a stage of a point as follows:
>[!definition]
>The *stage* of a point $x$ is the number $i$ such that $x\in X_{i}$ and $x\not\in X_{i-1}$. This is generally written as $|x|$ 
>
>Since $F_{\varphi}$ reaches its fixed point after $|\varphi|$ steps, for each point $x$ in the fixed point, we have that $|x| \leq |\varphi|$, hence for all points $y$ outside the fixed point we define the stage $|y| = |\varphi| +1$.

We now define the operators $\prec$ and $\preceq$ that compare the stages of points:
$$
\begin{align}
\vec{x} \prec \vec{y} &\equiv |\vec{x}|_{\varphi}^\mathfrak A < |\vec{y}|_{\varphi}^\mathfrak A\\
\vec{x} \preceq \vec{y} &\equiv |\vec{x}|_{\varphi}^\mathfrak A \leq |\vec{y}|_{\varphi}^\mathfrak A \text{ and } |\vec{x}|_{\varphi}^\mathfrak A \leq |\varphi|^\mathfrak A
\end{align}
$$

The following extra operators need to be defined that will all be constructed simultaneously
$$
\begin{align}
\vec{x} \not\prec \vec{y} &\equiv |\vec{x}|_{\varphi}^\mathfrak A \geq |\vec{y}|_{\varphi}^\mathfrak A\\
\vec{x} \not\preceq \vec{y} &\equiv |\vec{x}|_{\varphi}^\mathfrak A > |\vec{y}|_{\varphi}^\mathfrak A \text{ or } |\vec{x}|_{\varphi}^\mathfrak A = |\varphi|^\mathfrak A + 1
\end{align}
$$

and 
$$
\vec{x} \triangleleft \vec{y} \equiv |\vec{x}|_{\varphi}^\mathfrak A + 1 = |\vec{y}|_{\varphi}^\mathfrak A
$$

---
# References
