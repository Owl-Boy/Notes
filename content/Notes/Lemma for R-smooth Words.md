---
tags:
  - Note
  - Incomplete
---
202412020312

Tags : [[Algebraic Automata Theory]]
# Lemma for R-smooth Words
---
The proof is very similar to that of [[Lemma for J-smooth words]]

>[!theorem] 
>Given a $R$-smooth word $m_{1}\dots m_{n}=m$, one can construct a factorization tree of the word of height at most $3|R(m)| -1$.

We prove the theorem by proving a stronger claim:
Given a $R$-smooth word, $m_{1}\dots m_{n}=m$, one can construct a factorization tree of the word of height at most $3 \cdot C_{H}(m_{1}\dots m_{n})- 1$, where $C_{H}(m_{1}\dots m_{n})$ is the number of $H$-classes that prefixes of the word visit.

The proof will be an induction on the $C_{H}$ of subwords.
We first find all $a_{i}$ such that $m_{a_{i}}$ is in the same $H$-class as $m$, and we split the word into subwords starting at those parts as follows:
![[Pasted image 20241202033739.png]]

We make a tree for each $w_{i}m_{a_{i}}$ by making a tree for $w_{i}$ and making a parent of the root and that of $m_{a_{i}}$. The roots of all the above trees form a $R$-smooth sequence by constriction so by [[Lemma for H-smooth Words]], one can find a tree for height $3|H(m)|-1$ on top of it.

*Claim:* For each $w_{i}$, we have $C_{H}(w_{i})<C_{H}(m_{1}\dots m_{n})$ 
*Proof:* Since the entire sequence is $J$-smooth, we can apply [[Location Lemma]] and get that the $H$-classes visited are exactly those of the words in the sequence, since $w_{i}$ does not contain any element which has the same $H$-class as $m$ we get at least one class that is not in $C_{H}(w_{i})$.

By induction we can construct a sub-tree for each $w_{i}$ of height at most 
$$3 \cdot (C_{H}(m_{1}\dots m_{n})-1)-1$$. 

So for the entire word we can construct a tree of height
$$
\begin{align}
3 \cdot &(C_{H}(m_{1}\dots m_{n})-1)-1 + 1 + 3|H(m)|-1  \\
&= 3 \cdot C_{H}(m_{1}\dots m_{n})-1
\end{align}
$$

**Note:** We are guaranteed to have at least $1$ such subword well defined because $m_{n}\ H\ m$.

---
# References
[[Lemma for J-smooth words]]
[[Lemma for H-smooth Words]]
[[Factorization Forest Theorem]]