---
tags:
  - Note
---
202503202103

Tags : [[Weighted Automata and Transducers]]
# Normalizing a Transducer
---
Given a [[Sequential Transducers]], consider the following situation:
- After reading a word $w$ the transducer has produced the string $s$. 
- On reading a further $a$ the tranducer continues with the string $c\cdot c'$
- If instead it read a $b$ it would have continued with $c \cdot c''$
- If the word would have ended reading there it would have appeneded another $c$ to the output.

We see that in all of these scenarios the string $c$ is guaranteed to be produced by the transducer after reading $w$, so we might as well modify the automata to make sure that this happens. The process of doing this is called normalizing the transducer.

Given a transducer $\mathcal T = (Q, A, B,q_{0}, m_{0}, \delta, \phi ,\rho)$, the following will be its normalized version:
- $(Q', A', B', q_{0}', \delta') = (Q, A, B, q_{0}, \delta)$
- $m_{0}' = m_{0} \cdot m_{q_{0}}$
- $\phi'(q_{1},a) = m_{q_{1}}^{-1} \cdot \phi(q_{1}, a) \cdot m_{q_{2}}$
	- where $q_{2} = \delta(q_{1}, a)$
- $\rho'(q) = m_{q}^{-1}\cdot \rho(q)$

For all of these construction $m_{q}$ for some state $q$ is the string that one is guaranteed to output irrespective of the input. It can be defined as the longest common prefix of all possible string that can be generated from $q$.

The correctness for $m_{0}'$ and $\rho'$ are fairly trivial. For the correctness of $\phi'$:
- If $m_{q_{1}} \preceq\phi(q_{1}, a)$ then we are done as before this transition our normalized automata had already read $m_{q_{1}}$ so we can remove it from $\phi(q_{1}, a)$. Also after reading $\phi(q_{1}, a)$ one can safely read $m_{q_{2}}$.
- If $\phi(q_{1}, a) \prec m_{q_{1}}$ Then we have that whatever was going to be produced by the given transition was already covered in $m_{q_{1}}$, which means parts of $m_{q_{2}}$ were also covered. So what we would want in our reduced automata are specifically of $m_{q_{2}}$ that is not read, hence we are done.

---
# References
