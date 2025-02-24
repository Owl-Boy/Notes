---
tags:
  - Note
  - Incomplete
---
202502140902

Tags : [[Weighted Automata and Transducers]]
# Kleene Shutzenberger Theorem
---
>[!theorem]
>$$
>S^\text{Rat}\langle\!\langle A^* \rangle \!\rangle = 
>S^\text{Reg}\langle\!\langle A^* \rangle \!\rangle
>$$

[[Closure Properties of Recognizable functions]] already shows that $S^\text{Rat}\langle\!\langle A^* \rangle \!\rangle \subseteq S^\text{Rec}\langle\!\langle A^* \rangle \!\rangle$.

To show the other way, we need to create a rational expression for a series given by a weighted automata.

Let $\langle I, M, F\rangle$ be a weighted automata over some semi-ring, where $M$ is the transition matrix. If we can find $M^*=\sum_{n\in \mathbb{N}}M^n$ we can get the regular expression as $I \cdot M^* \cdot F$.

We start with defining $M^* = MM^*+1$
So We can do the following
$$
\begin{bmatrix}
x_{1,1}   & \dots  & x_{1,n} \\
\vdots  & \ddots & \vdots \\
x_{n,1}   & \dots  & x_{n,n} \\
\end{bmatrix}
=
\begin{bmatrix}
a_{1,1}   & \dots  & a_{1,n} \\
\vdots  & \ddots & \vdots \\
a_{n,1}   & \dots  & a_{n,n} \\
\end{bmatrix}
\begin{bmatrix}
x_{1,1} & \dots  & x_{1,n} \\
\vdots & \ddots & \vdots \\
x_{n,1} & \dots  & x_{n,n} \\
\end{bmatrix}
+
\begin{bmatrix}
1 & \dots  & 0 \\
\vdots & \ddots & \vdots\\
0 & \dots  & 1 \\
\end{bmatrix}
$$
Now we manually expand the entire equation into $n^2$ equations (point wise equality) and use [[Arden's Lemma]] to solve them (deleting variables 1 at a time).

This gives us a [[Rational Series]] for the automata and we are done.

---
# References
