---
id: Dedekind Reals are a Field
aliases:
  - Dedekind Reals are a Field
tags:
  - Note
---
202602172149

Tags : [[Homotopy Type Theory]]
# Dedekind Reals are a Field
---
We can start by describing the dedekind reals as an abelian group under addition:
$$
\begin{aligned}
L_{x+y}(q) :\equiv \exists(r\ s:\mathbb Q).L_x(r)\land L_y(s) \land q=r+s\\
U_{x+y}(q) :\equiv \exists(r\ s:\mathbb Q).U_x(r)\land U_y(s) \land q=r+s
\end{aligned}
$$

And for the additive inverse we can define 
$$
\begin{aligned}
L_{-x}(q) :\equiv \exists(r:\mathbb Q) U_x(r)\land q=-r\\
U_{-x}(q) :\equiv \exists(r:\mathbb Q) L_x(r)\land q=-r\\
\end{aligned}
$$

Now we can give it a commutative ring structure by defining multiplication as:
$$
\begin{aligned}
L_{x\cdot y}(q):\equiv \exists(a\ b\ c\ d:\mathbb Q). L_x(a)\land U_x(b)\land L_y(c)\land U_y(d)\land\\
q < \min(a,b,c,d)\\
U_{x\cdot y}(q):\equiv \exists(a\ b\ c\ d:\mathbb Q). L_x(a)\land U_x(b)\land L_y(c)\land U_y(d)\land\\
q > \max(a,b,c,d)\\
\end{aligned}
$$

For defining division we need concepts form [[Dedekind Reals are weakly linearly ordered]].

In particular we have that $x$ has a multiplicative inverse iff $x\#0$.

Also be definition of $<$ we trivially get that $\mathbb R_d$ satisfies the Archimedean principle.

It is also easy to show that the reals form an archimedean ordered field.

---
# References
- [[Dedekind Reals (HoTT)]]
- [[Dedekind Reals are weakly linearly ordered]]
