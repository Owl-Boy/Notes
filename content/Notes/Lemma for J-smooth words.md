---
tags:
  - Note
  - Incomplete
---
202412020212

Tags : [[Algebraic Automata Theory]]
# Lemma for J-smooth words
---
>[!theorem] 
>Given a $J$-smooth word $m_{1}\dots m_{n}=m$, one can construct a factorization tree of the word of height at most $3|J(m)| -1$.

We prove the theorem by proving a stronger claim:
Given a $J$-smooth word, $m_{1}\dots m_{n}=m$, one can construct a factorization tree of the word of height at most $3 \cdot |R(m)|\cdot C_{r}(m_{1}\dots m_{n})- 1$, where $C_{r}(m_{1}\dots m_{n})$ is the number of $R$-classes that prefixes of the word visit.

The proof will be an induction on the $C_{r}$ of subwords.
We first find all $a_{i}$ such that $m_{a_{i}}$ is in the same $R$-class as $m$, and we split the word into subwords starting at those parts as follows:
![[Pasted image 20241202031310.png]]

We make a tree for each $m_{a_{i}}w_{i}$ by making a tree for $w_{i}$ and making a parent of the root and that of $m_{a_{i}}$. The roots of all the above trees form a $R$-smooth sequence by constriction so by [[Lemma for R-smooth Words]], one can find a tree for height $3|R(m)|-1$ on top of it.

*Claim:* For each $w_{i}$, we have $C_{R}(w_{i})<C_{R}(m_{1}\dots m_{n})$ 
*Proof:* Since the entire sequence is $J$-smooth, we can apply [[Location Lemma]] and get that the $R$-classes visited are exactly those of the words in the sequence, since $w_{i}$ does not contain any element which has the same $R$-class as $m$ we get at least one class that is not in $C_{R}(w_{i})$.

By induction we can construct a sub-tree for each $w_{i}$ of height at most 
$$3 \cdot |R(m)| \cdot (C_{r}(m_{1}\dots m_{n})-1)-1$$. 

So for the entire word we can construct a tree of height
$$
\begin{align}
3 \cdot |R(m)| \cdot &(C_{r}(m_{1}\dots m_{n})-1)-1 + 1 + 3|R(m)|-1  \\
&= 3 \cdot |R(m)| \cdot C_{R}(m_{1}\dots m_{n})-1
\end{align}
$$

**Note:** Existence of at least $1$ equivalence class is guaranteed because $m_{1} R m$.

---
# References
[[Factorization Forest Theorem]]
[[Lemma for R-smooth Words]]