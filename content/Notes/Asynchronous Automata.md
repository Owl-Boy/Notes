---
id: Asynchronous Automata
aliases:
  - Asynchronous Automata
tags:
  - Note
  - Incomplete
---
202601102231

Tags : [[Concurrency Theory]]
# Asynchronous Automata
---
> [!NOTE]
> Do not have a super natural way to get to Asynchronous Automata, so I will use a specific problem.

Consider the trace language, with the distributed alphabet $\{\{a, c\},\{b, c\}\}$:
$$
c \left[
\begin{pmatrix}
a & a\!-\!a \\
b & b\!-\!b
\end{pmatrix}
c
\right]^*
$$

This language is regular:
$$
c[(ab,ba,aabb,abab,abba,baba,bbaa,baab)c]^*
$$

but is not accepted by any [[Syncho]], This is because, the projection languages are 
$$
\begin{aligned}
c[(a&, aa)c]^*\\
c[(b&, bb)c]^*\\
\end{aligned}
$$

And for each of these, a transition system would have transition $wc\square \to wc\square c$ and $wc\square\square\to wc\square\square c$. Where $\square$ can be filled with either $a$ or $b$. But since these automata don't interact with each other, there must be a transition must also be enabled in both automata for a word that is like 

$$
\begin{matrix}
&&&&a\\
&&&\diagup\\
w&-&c&\\
&&&\diagdown\\
&&&& b & - &b
\end{matrix}
$$

This problem here is that while $c$ is recognized by both processes, it is also dependent on both the processes together. There are 2 conditions $\alpha$ and $\beta$, and we should be allowed to fire $c$ if both the processes satisfy $\alpha$ or both of them satisfy $\beta$.

Thus if, for an action $c$, even if it is recognize by multiple processes, in a synchronized automata, it cannot be simultaneously dependent on states of the processes that recognize it. A formal proof for the above argument is given [[Not all regular trace languages are synchornous|here]].

We can thus update our semantics to allow such transitions, these give us **Asychronous Automata**.

> [!DEF] Definition
> An asynchronous automata is defined using a tuple contianing the following:
> - A distributed alphabet $\Sigma_\mathbb P$.
> - A set of states $Q = \prod_{p\in\mathbb P}Q_p$
> - For each letter $a\in \Sigma$, a transition function $\delta_a:2^{\text{loc}(a)}\to 2^{\mathbb P}$
> - A set of final states $F\subseteq Q$.
> - A set of start states $Q_\text{in}\subseteq Q$.

---
# References
- [[Distributed Alphabet]]
- [[Concurrency Theory]]
- [[Direct Product Automata]]
- [[Not all regular trace languages are synchornous]]
