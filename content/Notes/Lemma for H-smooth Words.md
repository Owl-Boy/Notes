---
tags:
  - Note
  - Incomplete
---
202412020312

Tags : [[Algebraic Automata Theory]]
# Lemma for H-smooth Words
---
>[!theorem] 
>Given a $H$-smooth word $m_{1}\dots m_{n}=m$, one can construct a factorization tree of the word of height at most $3|H(m)| -1$.

If $n=1$, then we get a tree of height $0$ and we are done.

If all elements are the same idempotent element, then we can construct a tree of height $1$ and we are done.

We proceed by proving a stronger claim: Given an $H$-smooth word, $m_{1}\dots m_{n}=m$ one can construct a factorization tree of the word of height at most $3 \cdot C_{H}(m_{1}\dots m_{n})-1$ where $C_{H}(w)$ is the number of elements $H$-class visited by all prefixes of $w$.

Otherwise, $H(m)$ contains multiple elements and forms a group. Consider all $a_{i}$ such that $m_{1} \cdot m_2 \dots m_{a_{i}} \ =\ m$. Once we have all such $a_{i}$ we can split the word into subword each starting at a different $m_{a_{i}}$ for all $i$ as follows:

![[Pasted image 20241202040319.png]]

*Claim:* $C_{H}(w_{i})<C_{H}(m_{1}\dots m_{n})$
*Proof:* Claim is true for $w_{1}$ by construction, for $w_{i}$ the set of elements its prefixes visit is in bijection with the set of elements that prefixes of $m_{1}\dots m_{a_{i-1}}w_{i}$ that end inside $w_{i}$ visit as $H(m)$ is a group. But that set does not contain $m$ by construction and hence the claim is proved.

Since $m_{1}\dots m_{\alpha_{i}}=m$ and $m_{1}\dots m_{\alpha_{i}}w_{i+1}m_{\alpha_{i+1}}=m$, we get that $w_{i+1}m_{\alpha_{i+1}}=1$ forall $i\geq 2$. 
- So for each $w_{i}$ we can construct a tree of height at most $3 \cdot (C_{H}(m_{1}\dots m_{n})-1)-1$
- For each $w_{i}m_{\alpha_{i}}$ we can construct a tree of height $3 \cdot (C_{H}(m_{1}\dots m_{n})-1)$
- For $w_{2}\dots m_{n}$ one can construct a tree of height $3\cdot C_{H}(m_{1}\dots m_{n})-2$ as all of them have $1$ as its root
- For the entire word, one can construct a tree of height $3 \cdot C_{H}(m_{1}\dots m_{n})-1$

And we are done.

---
# References
[[Lemma for R-smooth Words]]
[[Lemma for J-smooth words]]
[[Factorization Forest Theorem]]