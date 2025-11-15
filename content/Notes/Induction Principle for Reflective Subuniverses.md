---
tags:
  - Note
---
202510091910

Tags : [[Homotopy Type Theory]]
# Induction Principle for Reflective Subuniverses
---
>[!theorem]
>For a [[Reflective Subuniverses]] $\mathcal U_{P}$, the following are logically equivalent:
>- If $A:\mathcal U_{P}$ and $B:A\to\mathcal U_{P}$ then $\sum_{a:A}B(a)$ is in $\mathcal U_{P}$
>- For every $A:\mathcal U$, type family $B:\bigcirc A\to\mathcal U_{P}$  and a map $g:\prod_{a:A}B(\eta_{A}(a))$, there is a function $f:\prod_{z:\bigcirc A}B(z)$ such that $f(\eta(a))=g(a)$.

First, we prove the forward direction. Since $\eta_{A}$ is an equivalence, we have that $\sum_{z:\bigcirc A}B(z)$ lies in $\mathcal U_{P}$ and we have $g':A\to \sum_{z:\bigcirc A}B(z)$ given by $g'(a)=(\eta(a),g(a))$. 
Since $\pi_{1}\circ \text{rec}_{\circ}g'=\pi_{1}\circ\text{id}_{\bigcirc A}$ by universal property of reflective subuniverses we get $\text{rec}_{\circ}g'=\text{id}_{\bigcirc A}$, therfiore we have $p_{z}:p_{1}(\text{rec}_{\circ}(g')(z))=z$. Thus we have $f(z):\equiv p_{z*}(\pi_{2}(\text{rec}_{\circ}(g')(z)))$ but since $\circ\eta_{A}$ is an equivalence you get that $p_{z*}$ is the same as $p_{\eta(a)}$ if $z=\eta(a)$, thus the second component yields $f(\eta(a))=g(a)$.

For the converse, let $h$ be the composite
$$
\bigcirc\left( \sum_{a:A}B(a) \right)\xrightarrow{\bigcirc(\pi_{1})}\bigcirc A\xrightarrow{\eta^{-1}}A
$$

Then for $z:\sum_{x:A}B(x)$ we have
$$
\begin{align}
h(\eta(z))&\equiv\eta^{-1}(\bigcirc(\pi_{1})(\eta(z))) \\
&=\eta^{-1}(\eta(\pi_{1}(z))) \\
&=\pi_{1}(z)
\end{align}
$$
Denote that path by $p_{z}$. Now if we have $C:\bigcirc\left( \sum_{z:A}B(z) \right) \to\mathcal U$ by $C(w):\equiv B(h(w))$ we have 
$$
g:\equiv \lambda z.p_{z*}(\pi_{2}(z))\quad:\quad\prod_{z:\sum_{x:A}B(x)}C(\eta(z))
$$
This helps us define $f(\eta(z))=g(z)$. Together $h$ and $f$ give a function $k:\bigcirc\left( \sum_{x:A}B(x) \right) \to \sum_{x:A}B(x)$ defined by $k(w)=(h(w),f(w))$ while $p_{z}$ gives the equality $f(\eta(z))=g(z)$ show that $k$ is a retraction of $\eta_{\sum_{(x:A)}B(x)}$. Therefore $\sum_{x:A}B(x)$ is in $\mathcal U_{p}$.

>[!note]
>The second part of the theorem is like an induction principle. The universal property of the reflective subuniverses are its recursion principle. The first part of the theorem shows the connect.
 
---
# References
