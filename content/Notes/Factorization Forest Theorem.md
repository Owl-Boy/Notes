---
tags:
  - Note
  - Incomplete
---
202411281411

Tags : [[Algebraic Automata Theory]]
# Factorization Forest Theorem
---
>[!definition] Factorization Tree
>Given a word over the alphabet $\mathcal M$ a factorization tree is a tree whose leaves are lablelled with the letters of the words in order
>- Given 2 adjacent nodes labelled $m_{1}$ and $m_{2}$ their parent can be labelled with the value of $m_{1}\cdot m_{2}$
>- Given $n$ sibling nodes that have the same idempotent label $e$, all of them can be given a single parent whose label is also $e$.

The *factorization forest theorem* gives us a bound of the height of the tree, in fact the theorem states that the height of the tree can be given a bound that is independent of the length of the word.

>[!theorem] Factorization Forest Theorem
>The Factorization Forest Theorem states that given any word $w=m_{1}m_{2}\dots m_{n}$ where $m_{i} \in \cal M$, there is a factorization tree for $w$ of height less than or equal to $4 * |\cal M|$

We prove the theorem by proving a stronger statement:
given $m_{1}m_{2}\dots m_{n}=m$, where $m$ is the product of all the letters in the word, there is factorization tree for the word of height $4|J_{\leq}(M)|$, where 
$$
J_{\leq}(m) = \bigcup_{n\geq m}J(n).
$$

#### Proof 
The proof is by induction on the size of $J_{\leq}(m)$, hence the base case is clearly when $J(m)=J(1)$ or $m\ J\ 1$. 

##### Proof for base case:
Note that all $m_{i} : i\in[1..n]$ are in $J(1)$ as each $m_{i}\leq_{J}1$. And so in every subword of $m_{1}\dots m_{n}$. This means that the word is $J$-smooth.

Now from the [[Lemma for J-smooth words]] we get a tree of height $3|J(m)|-1 \leq 4|J_{\geq}(m)|$ and we are done.

### Proof for induction step

We start by partitioning the word greedily from left to right into runs that evaluate to an element in $J(m)$. i.e we find $a_{i}$ such that $m_{a_{i-1}+1}\dots m_{a_{i}}\ J\ m$. We do this as follows:

Since we greedily make the partition, no subset of any $w_{i}$ evaluates to an element in $J(m)$. 
- So for each $w_{i}$ we can construct a factorization tree whose height is at most $4[|J_{\geq}(m)|- |J(m)|]$ 
- We can add one more layer to pair each $w_{i}$ with $m_{a_{i}}$
- The roots of all $w_{i}m_{a_{i}}$ for a sequence of elements that is $J$-smooth by construction, so a tree can be built of top of them of height at most $3|J(m)|-1$ by the [[Lemma for J-smooth words]] again.
- We now add one more later to attach $w_{k}$ to the tree.

In the end we get a tree of height
$$
4|J_{\geq}(m)| - |J(m)| + 1
$$
---
# References
[[Lemma for J-smooth words]]
[[Lemma for R-smooth words]]
[[Lemma for H-smooth words]]